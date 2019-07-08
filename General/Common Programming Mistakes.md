# Common Programming Mistakes
Over time we have observed a set of typical mistakes beginners make while creating software. This section discusses those to mistakes.

Table of Content
*  [If Followed By An Unnecessary Else](#if-followed-by-an-unnecessary-else)
*  [Repeating The Code](#repeating-the-code)
*Note: code in this section might be oversimplified to convey a point, do not use this code in actual implementation.*

## If Followed By An Unnecessary Else
Here is a function that registers a new user using required information, returns error in case a user with provided email already exists, and sends the latest newsletter in case user chose to do so.
```
def register_user(user_data):
    if User.findOne(user_data.email):
        return "user with this email already exists"
    else:
        new_user = User.create(user_data)
        if new_user.newsletter_signup:
        new_user.send_newsletter()
        ...
```
The function above works fine but we can improve it's readability by reducing the nesting caused by unecessary `else` block.
```
def register_user(user_data):
    if User.findOne(user_data.email):
        return "user already exists"

    new_user = User.create(user_data)
    if new_user.newsletter_signup:
        new_user.send_latest_newsletter()
    ...
```
## Repeating The Code
Here is a function that registers a new user and returns error in case the password is weak in strength.
```
def register_user(user_data):
    ...
    //must have at least 8 chars, and limit special chars to @#$%^&+=
    if not re.match(r'[A-Za-z0-9@#$%^&+=]{8,}', user_data.password):
        return "password must be at least 8 chars long and special chars are limited to @#$%^&+="
    ...
```
Here is a function that changes the password
```
def change_password(new_password):
    ...
    //must have at least 8 chars, and limit special chars to @#$%^&+=
    if not re.match(r'[A-Za-z0-9@#$%^&+=]{8,}', new_password):
        return "password must be at least 8 chars long and special chars are limited to @#$%^&+="
    ...
```
Both functions work fine but imagine there is a new requirement to change minimum password length from 8 chars to 10. In current implementation you will need to make changes at two places. In other words you are **repeating the code**. A better approach is to create a separate function that verifies password strength and use it in both functions.
```
//must have at least 8 chars, and limit special chars to @#$%^&+=
def has_required_strength(password):
    return re.match(r'[A-Za-z0-9@#$%^&+=]{8,}', password)

def register_user(user_data):
    ...
    if not has_required_strength, user_data.password):
        return "password must be at least 8 chars long and special chars are limited to @#$%^&+="
    ...
def change_password(new_password):
    ...
    if not has_required_strength(new_password):
        return "password must be at least 8 chars long and special chars are limited to @#$%^&+="
    ...
```
Did you notice there is still a problem? (if you didn't, please don't read any further, try to notice what's wrong with our improved implementation). Problem is that we are still repeating the error string. Just like function `has_required_strength` we can and should define the error string at a single place and reuse it.
