- Do not create a super class. A super class is a class which does too many things. A class should only be specific to what it's name suggests. 

- Code Comments 
    - Do not write comment if something is obvious 
    - Write comments as a tool to communicate with other developer reading your code for the first time and trying to understand what or why you did certain things
    - Always write comments above the line

```
//this is a good comment
theAboveCommentIsAbout(me)

theCommentOnRightIsAbout(me) //this is a bad comment
```

- If you are following OOP paradigm in your project, understand and practise SOLID principles. 

- Actions (Front end)
    - Keep all of your business logic in actions

- Architecture (Front end)
    - Keeping data strictly separate from views

- Keep only those imports and dependencies in the project which are actually needed and used.

- Always strive for KISS i.e. to Keep It Stupid and Simple

- If you are kicking off a new project or starting work on a major new feature/module, do consult the design/architecture with team lead or with an architect within the organization. 

- Actively design solutions in a way, that they can be easily removed from current project, and packaged as an independent solution

- Install real time coding feedback tools in your development environment such as linters. Unless there is a good reason, follow the recommendations given by such tools. 

- Define reusable constants clearly on top of file or within a class in CAPS

- Mention the specific version of a dependency in your `package.json/pom.xml/requirements.txt`.

- DRY: Understand and follow `DRY` principle. In computer science DRY stands for Don't Repeat Yourself. By following this principle you can avoid duplicate code. 
> When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements. Additionally, elements that are logically related all change predictably and uniformly, and are thus kept in sync. 