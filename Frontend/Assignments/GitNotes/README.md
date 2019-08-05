# GitNotes!

Everyone takes notes and sometimes people want to share it with other people, especially in open source community which is why gists are so popular. In this assignment you are going to provide a better solution for keeping notes and sharing them.

## Screens Flow

### The Landing Page

- As you open the app, you see landing screen with a list of Notebooks in it.
- List will contain paginated `public Notebooks` from github.
- Page will contain a header with
  - `Login` menu for login with github
  - `Search` for searching a Note using ID

![Grid View](https://user-images.githubusercontent.com/15946354/62457522-7b1c3600-b794-11e9-9fc1-82e1c5b68828.png)

![List view](https://user-images.githubusercontent.com/15946354/62457567-9129f680-b794-11e9-9b2e-24d9c6216be6.png)

### Login Page

- Once you click `login` menu, it will allow the user to login using github.
  - Maintain user session
- Once logged in, header will contain `profile` menu with picture of user.

### Notebook Page

- Once you click any Notebook from landing page, it will redirect to Notebook page
- For a Public Notebook page will
  - Contain the information of the Notebook with owner's informations
  - Allow user to give `star`
  - Allow user to `fork` that Notebook
- For User's Notebook user will be able to
  - `Edit` Notebook
  - `Remove` Notebook

![Notebook](https://user-images.githubusercontent.com/15946354/62457649-b28ae280-b794-11e9-92cd-3d368a28568a.png)

![Notebook – 2](https://user-images.githubusercontent.com/15946354/62457674-be76a480-b794-11e9-973e-e90c51e291df.png)


### Profile Menu/Page

- From profile menu will have
  - `Create` Submenu for creating a Notebook
  - `Logout` Submenu for Singing out of Github
  - `Profile` Submenu for User Profile & `user's Notebooks`

![Notebook – 3](https://user-images.githubusercontent.com/15946354/62457769-e36b1780-b794-11e9-8506-4d4aa9a0c681.png)

### Search Menu

- Search Menu will allow
  - Searching a Notebook using ID
  - Show Results of Query using Notebook Page

## Tech Stack

- React
- Redux
- NodeJS
- Types using Typescript or Flow

Rest of the tools are your own choice. You can use Create React App to get started.

## Concept Coverage

### HTML/CSS

- Use `HTML5` semantic elements
- Use `CSS3` with
  - Flexbox
  - Grid Layout

### React JS

- `ES6`
- `Function Components` for Parts Responsible for Markup & Rendering
- `Class Components` for Parts with Business Logic
- `Redux` Integration for
  - State Management
  - APIs Response
- `Higher Order Functions/Components` for atleast two components
- `React Hooks` with Function Components, if required

### NodeJS

- API Designing
- API Routes
- Server Mounting Scripts/Configurations

## Coding Guidelines

Integrate `eslint` with code guidelines from
[airbnb](https://github.com/airbnb/javascript)

## Submission

The result of this assignment should be a project source code, uploaded at GitHub. Please forward GitHub repo link to your mentor.
