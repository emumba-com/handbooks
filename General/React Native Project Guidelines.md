<center> <h1>React Native Project Guidelines</h1> </center>

## Version Control:
---

**Branches:**

- `master`: Will have the stable code from the dev branch.
- `dev`: Main development branch. All builds will be released from this branch. Also, all the working branches will originate from dev. In the end, working branches will be merged in dev.

**Naming Conventions for branches**:

- `feat/<name>` : for adding a new functionality or feature
- `chore/<name>`: for usual tasks
- `refactor/<name>` : for code refactoring
- `fix/<name>` : for a fix in functionality
- `hotfix/<name>` : for a fix of a bug that causes a crash
- `docs/<name>` : for adding a documentation

**Pull Requests (PRs):**
All branches will be made from the main development branch (dev). So, all PRs will be made against the base branch.

**PR Reviews:**
PR will be reviewed by peers. Peers will review, comment and request changes in the PR if required. If a branch has conflicts with the base branch **reviewer** will ask the peer to resolve the conflicts first and then review the PR. If reviewer left the comments on PR, they will be resolved or discussed in the PR thread.

<br>

## Commit Guidelines:

---

We will use [husky’s](https://github.com/typicode/husky) commit guidelines. We’ll add husky to our project and it will check the rules before every commit.

If we want to run linting or tests before every commit, husky will help us with that.

The general rules to be followed in writing a commit message are as follows:

- The first line of the commit message should be a short description (50 characters is the soft limit), and should skip the full stop
- The body should provide a meaningful commit message, which:
  - uses the imperative, present tense: “change” not “changed” or “changes”.
  - includes motivation for the change, and contrasts its implementation with previous behaviour.

<br>

## Typings:

---

Typescript will be followed throughout the whole project. Typescript helps you catch type errors during compile time so they won’t bug you during runtime.

Strict typings will be enforced on the following:

- Component’s Props and State
- Functions input types and return types
- Response data from API calls
- Redux state
- Action Creators

<br>

## React Guide:

---
Project will follow the react-hooks. React-hooks lets you use React features without using class syntax.

<br>

## Testing:

---
**Jest**
Use jest javascript testing library for writing test cases for react native application. Test cases for all Redux actions and functions that determine the functionality of the application are necessary to be written and jest provides a lot of help in this regard like mocking simple functions, manual module Mocks and Timer Mocks. It also supports Typescript which we will be using in this project. We can ignore UI Test cases as we can manually test this by playing around with UI elements.

<br>

## Documentation:

---
`Code will be documented by using JSDocs`
JSDocs improve code readability by using annotations like

- @method method_name
- @returns {return_types}
- @param {Parameter_Type} param_name
  above every method.

`README will be maintained for instructions to install and run the app`

<br>

## Storage:

---
The selection of storage libraries and tools is totally project specific. There are multiple databases available to use with React-Native or JS e.g

- Async Storage
- Realm
- Watermelon Db

<br>

## Debugging:

---

**Reactotron**
[Reactotron](https://github.com/infinitered/reactotron) Requires a configuration file to be put in the project root folder

- Logs XHR requests
- Outputs warning and logs using `console.tron.log` or `console.tron.warn`

**React Native Remote Debugging**
This is a built in option in all react-native projects uses `chrome developer tools` for debugging XHR requests and console.logs are displayed in dev-tools.

<br>

## Project Structure:

---
Following is the suggested code structure based on hands on experiences and opinions

```
App
    Components (contains re-usable components e.g a TextField)
    Containers (contains components that will be used to render child components)
    Navigation
    Redux or Sagas (for state of the application and for handling side-effects)
    Utils
    Constants
    Themes
    Store
```

<br>

## State Management:

---

**Redux**

- We will use Redux to manage data flow of Application.
- As a middleware, use Redux Saga because it makes handling of side effects in app nice and easier.
  <br>

## Navigation:

---

**React Navigation**
Use [React Navigation](https://reactnavigation.org/docs/en/getting-started.html) for routing. Which is full JavaScript library for routing. For highly complex and Large apps we can use react native navigation, which is native implementation of routing.

<br>

## Data Transformations:

---

**Lodash**
Use lodash for iterating and reducing data. As lodash makes javascript easier by taking the hassle out of working with arrays, numbers, objects, string etc.
