[Coding is social activity](./Programming-Is-For-People.md), hence your code needs to be clear enough so that it takes least amount of time for a new person to get up and running with your project.

Variable declaration is an activity that happens at such a high frequency in your coding activity, that even tiny improvements in this area can significantly impact quality of your code. There are a few aspects that need to be kept in mind when declaring variables.

# Context

Variables need to be declare ONLY if you intend to re-use result of a computation. If result of a computation is getting used only at one instance, you better skip declaring the variable.

```
// bad use of variable
data = getLatestData()
print(data)

//a better approach
print(getLatestData())
// assuming data is not used anywhere later in the code
```

# Scope

Root of most evils in programming is having values of different variables changed at non-obvious places. Hence, hence the rule should be to declare every variable as a constant first (in JavaScript/ES6, you can use `const`). It can be changed to a variable only when it's value is explicitly required to be changed (in JavaScript/ES6, you can use `let` for it). This simple practice can significantly reduces chances of errors in your code.

# Naming

Variable names should be succinct enough so people can understand your code clearly. Name of a variable needs to convey the purpose of its existence. E.g `let age = 0` is better than `let a = 0`. Read more about [naming variables here](./How-To-Name-Your-Resources.md).

# Comments

If you think your variable name doesn't clearly communicate its purpose, you should write a comment on top of variable declaration. Remember the goal: your code needs to be understandable as easily as possible by your teammates.
