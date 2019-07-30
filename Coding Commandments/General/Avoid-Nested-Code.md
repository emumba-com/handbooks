Nested code blocks, also known as pyramid of doom, are enemies of readability. Following are common situations which may cause pyramid of doom:

# If-Conditions

If-Conditions, particularly when nested in one another, may create crazy pyramids. Consider this example:

```
function register( req, res ) {
    let msg = ''
    if ( Object.keys(req.param).length > 0 ) {
        if ( req.param.user_name ) {
            if ( req.param.user_password_new ) {
                if ( req.param.user_password_new === req.param.user_password_repeat ) {
                    if ( req.param.user_password_new.length > 5 ) {
                        if ( req.param.user_name.length < 65 && req.param.user_name.length > 1) {
                            if ( /^[a-z\d]{2,64}$/.exec(req.param.user_name) ) {
                                return createUser(req.param.user_name, req.param.user_password_new)
                            } else {
                                msg = 'user_name can only contain lower case letters or digits'
                            }
                        } else {
                            msg = 'user_name needs to be between 2 and 64 characters'
                        }
                    } else {
                        msg = 'Password needs to be at least 6 characters'
                    }
                } else {
                    msg = 'Passwords do not match'
                }
            } else {
                msg = 'Empty password'
            }
        } else {
            msg = 'Empty user_name'
        }
    } else {
        msg = 'Empty values'
    }

    return reject(msg, res)
}
```

You can avoid pyramids of doom by avoiding nesting and doing early returns:

```
function register(req, res) {
    if ( Object.keys(req.params).length < 1 ) {
        return reject('Empty values', res)
    }

    const { user_name, user_password_new, user_password_repeat } = req.params

    if ( !user_name ) {
        return reject('Empty user_name', res)
    }

    if ( !user_password_new ) {
        return reject('Empty password', res)
    }

    if ( user_password_new !== user_password_repeat ) {
        return reject('Passwords do not match', res)
    }

    if ( user_password_new.length < 6 ) {
        return reject('Password needs to be at least 6 characters')
    }

    if ( user_name.length < 2 || user_name.length > 64 ) {
        return reject('user_name needs to be between 2 and 64 characters')
    }

    if ( !/^[a-z\d]{2,64}$/.exec(req.param.user_name) ) {
        return reject('user_name can contain only lower case alphabets and digits')
    }

    return createUser(user_name, user_password_new)
}
```

# Callbacks

Following code is an example of `pyramid of doom` which should be avoided at all costs.

```
ms.async.eachSeries(arrWords, function (key, asyncCallback) {
    pg.connect(pgconn.dbserver('galaxy'), function (err, pgClient, pgCB) {
        statement = "SELECT * FROM localization_strings WHERE local_id = 10 AND string_key = '" + key[0] + "'";
        pgClient.query(statement, function (err, result) {
            if (pgconn.handleError(err, pgCB, pgClient)) return;
            // if key doesn't exist go ahead and insert it
            if (result.rows.length == 0) {
                statement = "SELECT nextval('last_resource_bundle_string_id')";
                pgClient.query(statement, function (err, result) {
                    if (pgconn.handleError(err, pgCB, pgClient)) return;
                    var insertIdOffset = parseInt(result.rows[0].nextval);
                    statement = "INSERT INTO localization_strings (resource_bundle_string_id, string_key, string_revision, string_text,modified_date,local_id, bundle_id) VALUES ";
                    statement += "  (" + insertIdOffset + ",'" + key[0] + "'," + 0 + ",'" + englishDictionary[key[0]] + "'," + 0 + ",10,20)";
                    ms.log(statement);
                    pgClient.query(statement, function (err, result) {
                        if (pgconn.handleError(err, pgCB, pgClient)) return;
                        pgCB();
                        asyncCallback();
                    });
                });
            }
            pgCB();
            asyncCallback();
        });
    });
});
```

In JavaScript, this situation can be avoided using promises, or better, async/await. `Google`, there are plenty of articles available on this.

# Iterative Code

Below are two code snippets doing same thing

```
// snippet 1
my_input_numbers = [1,2,3,4,5,6,7,8]
my_odd_numbers = []
for number in my_input_numbers:
    if number % 2 != 0:
        my_odd_numbers.append(number)
print(my_odd_numbers)
```

```
//snippet 2
my_input_numbers = [1,2,3,4,5,6,7,8]
my_odd_numbers = [x for x in my_input_numbers if x%2 != 0]
print (my_odd_numbers)
```

You should avoid iterative code when possible using features provided by the language. E.g in case of python and Javascript you can use functions like `map`, `reduce`, `filter`, etc. You can read more on this under [Loops](./Loops.md).
