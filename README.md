# Marvel's Tic Tac Toe
***
## Describtion: 
The popular Tic Tac Toe game, build with a combination of **HTML**, **CSS**, and **JavaScript** for **DOM** and little of **jQuery**. it allows only one player (Cap America) to play the game with the computer (Iron Man), with an ability to play music and with sound effects, if the game end it will show either a winning message or the tie message.
***
## Wireframes:
  ### First page: 
 ![Tic Tac Toe Wireframe 1](./images/ReadmeImages/wireframe1.png)
   ### Second page: 
 ![Tic Tac Toe Wireframe 2](./images/ReadmeImages/wireframe2.png)
  ### Third page: 
 ![Tic Tac Toe Wireframe 3](./images/ReadmeImages/wireframe3.png)
***
## User Stories:
1. As a **player (Cap America)**, I should be able to start a new tic tac toe game by clicking the Start Game button.
2. As a **player (Cap America)**, I should be able to click on a square to add Cap America icon.
2. As a **player (Cap America)**, I should be able to play with **computer (Iron Man)**.
3. As a **player (Cap America)**, I should be shown a message after each turn for if I win, lose or tie.
4. As a **player (Cap America)**, I should not be able to click the same square twice.
5. As a **player (Cap America)**, I should be shown a message when I win, lose or tie.
6. As a **player (Cap America)**, I should not be able to continue playing once I win, lose, or tie.
7. As a **player (Cap America)**, I should be able to play the game again without refreshing the page.
8. As a **player (Cap America)**, I should be able to navigate between the pages.
9. As a **player (Cap America)**, I should be able to know About the Game by hovering the button. **>> Extra Feature**
10. As a **player (Cap America)**, I should be able to play music while playing the Game by clicking the button. **>> Extra Feature**
11. As a **player (Cap America)**, I should be able to play the Game in any device (Responsive). **>> Extra Feature**
***
## Technologies used:
Mainly used the HTML, CSS, and JavaScript for DOM as in the description above, with some additional technology such as Array Destructoring,...CSS Variables to be illustrated in the sections below.
***
## Devolpment Process & The Good Start:
The project success relies on the right way of the development process and how it can breakdown all the required requirements to meet the project goal, you will probably know the game well and how to build it visually but, the main thing is to walk through it step by step avoiding doing it in a conflictual way.
Below the helpful steps that I worked through during the project.
|**Step**|**Name**|**Description**|**Example**|**Reference**|
|----|------|-------------------|-------------|--------------|
|#1 |Determine the user needs|Collect the requirements  that should be done during the project|The user shall be able to start the game|[Requirements Gathering](https://thedigitalprojectmanager.com/requirements-gathering-guide/)|
|#2 |Creating the files|Start with Html, CSS, JS files and link them together and be sure to be all in the same folder|In my case I created two html files, one CSS, one JS|No need for reference (:|
|#3 |Creating the board game|With the help of the `div` selector the board will be created inside the html, it should be 3x3|`const getGameBoard = () => {gameBoardContainer.innerHTML = ""gameBoard.forEach((e, i) => {gameBoardContainer.innerHTML += `<div id="boardCell${i}" class="block" onclick="addcapAmericaMove(${i}); playSound();">${gameBoard[i]}</div>`if (e == capAmerica || e == ironMan) {document.querySelector(`#boardCell${i}`).classList.add("ironManTurn");}});};`|
|#4 |Add some styles|You can add your own styles as you like, I used the grid template for the game board|- |1. [Grid Templates](https://www.w3schools.com/cssref/pr_grid-template.asp) 2. [CSS Variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)|
|#5 |The game logic turn|Jumping into the JS file and start with logics, we need to know how the player will win, lose or tie! |``const checkMatch = () => { for (i = 0; i < 9; i += 3) { if (checkLines(i, i + 1, i + 2)) { document.querySelector(`#boardCell${i}`).classList.add("winner"); document.querySelector(`#boardCell${i + 1}`).classList.add("winner"); document.querySelector(`#boardCell${i + 2}`).classList.add("winner"); return gameBoard[i]; }}``|
|#5.a |The game logic with condetions|Continue to think logically and add the `if()` statement to help of deciding whos the winner?|``for (i = 0; i < 3; i++){if (checkLines(i, i + 3, i + 6)) {documentquerySelector(`#boardCell${i}`).classList.add("winner"); document.querySelector(`#boardCell${i + 3}`).classList.add("winner"); document.querySelector(`#boardCell${i + 6}`).classList.add("winner");return gameBoard[i];}}``|-|
|#5.b|Use the console to check the result|Be sure to use the console for each step|-|[Debugging in the console](https://developers.google.com/web/tools/chrome-devtools/javascript)|
|#5.c|Show the Winning message|Using the `if()` show the message if only if the cells are filled and if the winning combination is met then, will return whos the winner X or O ?|-|-|
|#6 |Reapet Step 5.b|To be sure that you're in the right way|-|-|
|#7|Add restart button|To let the player keep playing we can add a button in html and link it with th JS with `.addEventListener()`|`restartButton.addEventListener('click', startGame)`|-|

***
## Final Result:
![Project Demo](./images/ReadmeImages/finalResult.gif)
***
## Conclusion:
After learning all the needed skills during the SEI course, and leaveraged all the proven abilities to build a project with passionate and love to achive the overall mession and looking forward to learn more to continue enhance the knowledge. In the future, I would like to add some more features to empower the project by creating a score counter, two online players, and the ability to choose the token.