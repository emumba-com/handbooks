# **M**A**S**T**E**R _MIND_

In this era of apps, strategic games have become part of our daily routine. Either we are in office or in our home, either we are free or busy in our usual tasks; we tend to play these games in order to relax the mind in a most productive way. This assignment also serves the same purpose, so you are going to make a strategy game called **Master Mind** in this phase.

### Rules

Try to guess the pattern, in both order and color, within ten turns. After submitting a row, a small **black** peg is placed for each code peg from the guess which is correct in both color and position. A **white** peg indicates the existence of a correct color code peg placed in the wrong position. And a **cross** represents the wrong color code. More info on [Wikipedia](<https://en.wikipedia.org/wiki/Mastermind_(board_game)>).

### Screens/Pages

It&#39;s a single page application which has the following use-cases/scenarios:

![Landing Page Image](./images/landing-page.png 'Landing Page')

#### Show rules

is a button which shows the rules description.
![Show Rules Image](./images/show-rules.png 'Show Rules')

#### Hide rules

on click: back to 'Show rules'

There are total six colors on the right side of the app as you can see (by default, the 1st one is selected). Clicking on any color makes it selected. Now, you have to fill each row by coloring all circles in it, by color of your choice (but remember, you have to win the game so do it intelligently :stuck_out_tongue_winking_eye: ). When all four circles in a row are filled, app shows a tick to confirm the made choices as shown below:
![Tick Scenario Image](./images/tick-scenario.png 'Tick Scenario')

By clicking on this tick, app will show the results according to mentioned rules.
![All three possible scenarios image](./images/mock-for-black-white-cross.png 'All three possible scenarios (Black, White & Cross)')

In case of winning, app will show the following prompt:
![Winning Scenario Image](./images/winning-scenario.png 'Winning Scenario')

And in case of losing, the prompt will be:
![Losing Scenario Image](./images/losing-scenario.png 'Losing Scenario')

##### PLAY AGAIN

start the game from initial state.

#### Note:

1. At one time, only one row is enable; the rest are disable as you can see in the images.
2. All error and validation checks should be implemented properly.

### Tech Stack

- React
- Redux
- BabelJS/ES6
- CSS/SASS/LESS

You can choose other tools on per your requirement/need.

### Submission

The result of this assignment should be a project source code, uploaded at GitHub. Please forward GitHub repo link to your mentor.

### Timeline

You&#39;ve 3 working days to finish the assignment, starting from the date it was shared with you.

### Questions

If you have any questions, please feel free to ask.
