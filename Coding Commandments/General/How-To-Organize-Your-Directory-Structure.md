[Coding is social activity](./Programming-Is-For-People.md), hence your code needs to be clear enough so that it takes least amount of time for a new person to get up and running with your project.

Your directory structure is the very first thing your new teammates will encounter when they join your project. Hence, a clear structure makes a significant positive impact during on-boarding experience for them.

_Please note that directory structure of a project is hugely impacted by type of project, programming language, and sometimes even the framework being used. Hence the structure given below might not fit 100% on your project. The purpose of directory structure guideline is to emphasise on its importance and to ensure that a proper thought has been given on this at start of the project._

At the root level, your directory structure needs to contain highest level resource groups:

- `src` for your source code
- `build` for your compiled code
- `tests` for your tests. Some test environments keep your tests within your `src` directory, that's fine as well.
- `config` to contain all of your config files. In some cases it might be more appropriate to move this inside `src` directory.

Deeper level directories should be named in a way that whenever your teammate needs to create a new file, there is no confusion where to place that file.

When you're working in an IDE, you quickly open files using keyboard shortcuts. Make sure your filenames are sufficiently unique globally so opening files using shortcuts is easier. For example, if all of your LESS files are named as `style.less`, it'd be difficult to jump to a specific file using shortcuts. Instead, more specific names like `Header.less` (for a component named `Header`) or `Navigation.less` would make better names.

In case you think your directory structure is inherently not communicative enough, you should create a `README.md` file to explain your intentions. You can create this file not just at root level, but also in deeper directories.
