
# GitNotes!
Everyone takes notes and sometimes people want to share it with other people, especially in open source community which is why gists are so popular. In this assignment you are going to provide a better solution for keeping notes and sharing them.

## Screens Flow
### The Landing Page
- As you open the app, you see landing screen with a list of gists in it.
- List will contain paginated `public gists` from github.
- Page will contain a header with `Login` menu for login with github.

### Login Page
- Once you click `login` menu, it will allow the user to login using github.
  * Maintain user session
- Once logged in, header will contain `profile` menu with picture of user.

### Gist Page
- Once you click any gist from landing page, it will redirect to gist page
- For a Public Gist page will
  * Contain the information of the gist with owner's informations
  * Allow user to give `star`
  * Allow user to `fork` that gist
- For User's Gists user will be able to
  * `Edit` gist
  * `Remove` gist

### Profile Menu
- From profile menu will have
  * `List` Submenu for `user's gists` Page
  * `Create` Submenu for creating a Gist
  * `Logout` Submenu for Singing out of Github

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
  * Flexbox
  * Grid Layout

### React JS
- `ES6`
- `Function Components` for Parts Responsible for Markup & Rendering
- `Class Components` for Parts with Business Logic
- `Redux` Integration for
  * State Management
  * APIs Response
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