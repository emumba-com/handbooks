# GitNotes!

Why Gists are so popular? In open source community you want to create content & share it with people. With Gists you can create public content, code fragment, configuration files & files. You can share it with people, search it on Github, save it to your profile & much more. In this assignment you are going to provide a better solution for Managing Gists

## Screens Flow

### The Landing Page

- As you open the app, you see landing screen with a list of Gists in it.
- List will contain paginated `public gists` from github.
- Page will have two layouts to view the gists
  - List Layout
  ![List view](https://user-images.githubusercontent.com/15946354/62457567-9129f680-b794-11e9-9b2e-24d9c6216be6.png)
  - Grid Layout
  ![Grid View](https://user-images.githubusercontent.com/15946354/62457522-7b1c3600-b794-11e9-9fc1-82e1c5b68828.png)
- Use the toggle to Switch Between the Layouts
- Page will also contain a header with
  - `Login` menu for login with github
  - `Search` for searching a Gist using ID
  ![62457649-b28ae280-b794-11e9-92cd-3d368a28568a](https://user-images.githubusercontent.com/15946354/62517510-f76c5300-b840-11e9-9c92-a9ac23e2ec75.png)





### Login Page

- Once you click `login` menu, it will allow the user to login using github.
  - Maintain user session
- Once logged in, header will contain `profile` menu with picture of user.

### Gist Page

- Once you click any Gist from landing page, it will redirect to Gist page
- For a Public Gist page will
  - Contain the information of the Gist with owner's informations
  - Allow user to give `star`
  - Allow user to `fork` that Gist

  ![Notebook](https://user-images.githubusercontent.com/15946354/62457649-b28ae280-b794-11e9-92cd-3d368a28568a.png)

- For User's Gist user will be able to
  - `Edit` Gist
  - `Remove` Gist

  ![Notebook – 2](https://user-images.githubusercontent.com/15946354/62457674-be76a480-b794-11e9-973e-e90c51e291df.png)





### Profile Menu/Page

- Profile menu will have
  - `Create` Submenu for creating a Gist
  - `Logout` Submenu for Singing out of Github
  - `User Profile` Submenu for User Profile & `user's Gists`

![Notebook – 3](https://user-images.githubusercontent.com/15946354/62457769-e36b1780-b794-11e9-8506-4d4aa9a0c681.png)

### Search
- Search Bar will allow
  - Searching a Gist using ID
  - Show Results of Query using Gist Page

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
