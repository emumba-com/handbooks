# Attendant

A simple management system for mantaining employees' attendance and working hours in a workplace.

## Roles

### Users

- Punch form with fields for inputting employee ID and PIN code
- On successful validation:
  - in case of first login, user will be asked to change his/her PIN code and login again
  - in case this is not the first login, user will be able to see his/her punch card:
    - containing an avatar with his/her initials
    - a button for punch in/out
    - a button for applying for leave (user can avail this option only once at the start of day)
    - a button/icon for viewing previous records in a drawer/modal
    - drawer/modal contains a tabular view of all records
    - also, there will be a date based search field at the top of the table
- On validation failure, user will be shown an error
- Below the punch form, there'll be a link leading to admin login form

### Admin

- Login form with fields for inputting employee ID and PIN code
- On successful login, the admin will be routed to the dashboard:
  - contains 2 widgets for insights and a floating button for accessing settings
  - Widgets' description:
    1. Today's Availability: a 3-tabbed view containing list of available, unavailable and on-leave employees; contains a global search
    2. Overall Stats: a searchable, sortable list of all employees containing their total working hours and average working hours, consolidated over a period of 1, 3, 6 or 12 months; user should be able to sort list based on either name or total working hours. User should be able to select time period using a button group or dropdown at the top of the widget.
  - Settings view should contain the following stuff:
    - a searchable list of all employees; this list enables user to edit, delete or add an employee's info
    - an inline form in the list for adding an employee's info with the following fields: first and last name, email, department and role
    - inputs for changing office hours
    - input for changing minimum working hours
- On validation failure, user will be shown an error
- Below the login form, there'll be a link leading to punch form

## Rules & Validations

- **All data should be stored in Github gists**. Gists are generally used to store small (or not so small) snippets of code or other information in form of files. Check out API [here](https://developer.github.com/v3/gists/).
- Employee IDs are generated automatically according to the provided department (e.g SE-122)
- Employee code should be in range [000 - 999]
- PIN code should be 4 digits long; default PIN code for a new employee should be `0000`
- Every punch-in should have a corresponding punch-out; in case user doesn't punch out at day end, the last punch-in will be discarded at the start of the next working day
- Apply logical validations on inputs

## Tech Stack / Libraries

- React
- Redux
- NodeJS

Rest of the tools are your own choice. You can use [create-react-app](https://github.com/facebook/create-react-app) to get started.

## Coding Guidelines

- Integrate `eslint` with code guidelines from [airbnb](https://github.com/airbnb/javascript).
- Install a code formatter extension for your editor; you can use Prettier if it's available for your editor of choice.

## Submission

The result of this assignment should be a project source code, uploaded at GitHub. Please forward GitHub repo link to your mentor.

## Timeline

You've 5 working days to finish the assignment, starting from the date it was shared with you.

## Questions

If you have any questions, please feel free to ask your mentor.
