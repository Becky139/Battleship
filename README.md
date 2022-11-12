# Battleship Game

![Battleship Mockup Images](assets/readme_files/responsive.png)

[View the live project here](https://battleship-rm.herokuapp.com/)

## Table of contents
1. [Introduction](#Introduction)
    1. [How To Play](#How-To-Play)
2. [UX](#UX)
    1. [Ideal User Demographic](#Ideal-User-Demographic)
    2. [User Stories](#User-Stories)
    3. [Development Planes](#Development-Planes)
    4. [Design](#Design)
3. [Features](#Features) 
    1. [Imagery](#Imagery)
    2. [Existing Features](#Existing-Features)
    3. [Features to Implement in the future](#Features-to-Implement-in-the-future)
4. [Issues and Bugs](#Issues-and-Bugs)
5. [Technologies Used](#Technologies-Used)
    1. [Main Languages Used](#Main-Languages-Used)
    3. [Frameworks, Libraries & Programs Used](#Frameworks,-Libraries-&-Programs-Used)
6. [Testing](#Testing)
    1. [Testing User Stories](#Testing-User-Stories)
    2. [Manual Testing](#Manual-Testing)
    3. [Automated Testing](#Automated-Testing) 
        - [Code Validation](#Code-Validation)
    4. [User Testing](#User-Testing)
7. [Deployment](#Deployment)
    1. [Deploying on GitHub Pages](#Deploying-on-GitHub-Pages)
8. [Credits](#Credits)
    1. [Content](#Content)
    2. [Media](#Media)
    3. [Code](#Code)
9. [Acknowledgements](#Acknowledgements)
***


## Introduction

For the Portfolio Project 3 - Python Essentials, the developer decided to build a battleship game. Battleship (also known as Battleships or Sea Battle is a strategy type guessing game for two players. It is played on ruled grids (paper or board) on which each player's fleet of warships are marked. The locations of the fleets are concealed from the other player. Players alternate turns calling "shots" at the other player's ships, and the objective of the game is to destroy the opposing player's fleet.

Battleship is known worldwide as a pencil and paper game which dates from World War I. It was published by various companies as a pad-and-pencil game in the 1930s and was released as a plastic board game by Milton Bradley in 1967. The game has spawned electronic versions, video games, smart device apps and a film.

### How To Play

- The player enters their name and jumps straight into the action.
- The player places their 5 ships on the board.
- When all ships have been placed on the board the battle begins the player guesses the co-ordinates of the computers ships and the computer guesses where the player placed their ships. 
- The first to destroy all ships wins the game.

[Back to top ⇧](#)

## UX
### Ideal User Demographic
The ideal user for this website is:
* New user
* Current user

#### New User Goals
1. As a new user, I want to see clear instructions for gameplay. 
2. As a new user, I want to see a visual representation of my remaining Shots.
3. As a new user, I want the ability to replay the game.

#### Current User
1. As a current user, I want the ability to replay the game.
2. As a current user, I want the guess and hit the various ships.
3. As a current user, I want the choice to use different ship sizes. 

### Development-Planes
To create a command-line application that allows the user to play a classic game Battleships or Sea Battle is a strategy type guessing game for two players.

#### Strategy
Strategy incorporates user needs as well as product objectives. This website will focus on the following target audience, divided into three main categories:
- **Roles:**
    - New users
    - Current users

- **Demographic:**
    - All ages
    - All puzzle playing levels

- **Psychographic:**
    - Lifestyles:
        - Interest in games
        - Interest in battles
        - Interest in Ships
        - Interest in puzzles
    - Personality/Attitudes:
        - Focused
        - Forward-Thinking
        - Creative
    
The application needs to enable the **user** to:
- play the game "Battleship" using alpha characters and numbers.
- generate a random board on each play-through placing ships in different locations.
    

#### Scope
The scope plane is about defining requirements based on the goals established on the strategy plane. Using the information in the strategy plane, the identified required features have been broken into the following two categories.
- Content Requirements:
    - The user will be looking for:
        - Clear and concise instructions.
        - A consistent theme, and game play. 
- Functionality Requirements:
    - The user will be able to:
        - Enter co-ordinates using numbers and letters.
        - Replay the game.
        - End the program at the end of the game.

#### Structure
The project will be deployed to a Heroku terminal. There will be no styling aside from the image of Funny Bones built using special characters within the terminal. 

#### Skeleton
A flowchart was created to show the logic the functions would follow.

<details>
<summary>Flowchart</summary>
    
![Flowchart](assets/readme_files/battleship-flowchart.png)

</details>

[Back to top ⇧](#)

## Features

### Imagery
The project uses the board class as my model. The game creates four boards the first to hold the players guesses the second to display the users board and the other two are the same but for the computers board.
The board class stores the boards size (8), how many ships are on the board, the positions of the chosen ships on the board and information such as board type (player or computer board).
The board class also runs functions such as the place ship function so the player and computer can enter valid ship positions and a hit count function to count all the hit ships on the board.

### Existing Features
- The Welcome Message

    - When a new game starts the welcome message is displayed.
    - The user is met with colour coded sections and ASCII art (Battleships Logo) for clarity. 
    - Within this the different types of ship are listed, as well as the: board size, total number of hits needed to win (17) and the different styles of marker.
    - It also contains the instructions in how to play the game.
    - The player is then prompted for name input, which complies to the validation checks listed. Input is repeated until a valid name is entered.

![Welcome message](/assets/readme_files/battleship-homescreen.png)
![Instructions](/assets/readme_files/battleship-instrutions.png)
![Name input](/assets/readme_files/battleship-name.png)
![Start game](/assets/readme_files/battleship-start-game.png)

- The Board
    - Once name input is validated, it is then used to create the player's board, which is displayed to them in the terminal. The user is prompted to place each ship in turn from smallest to largest (2-5), the ship size is displayed to them.
    - Orientation, row and then column inputs are requested for the ship location, all having validation checks on them. Before placement of the ships on the board, overlap and fit checks are ran on the input location for the ship, which must be passed else the user is prompted for input again.
    - Once a all of the inputs are entered and valid the ship is placed on the players board, their board is then printed to them with the placed ship for reference when placing the next. The computers ships are randomly placed on their board before the player places their ships, following the same validation checks.

![Player board](/assets/readme_files/player-board.png)

![Player ship](/assets/readme_files/place-ship.png)

![Player placed all ships](/assets/readme_files/all-ships-placed.png)

- The Guess Board
    - Once the ships have been placed on each board the game play begins.
    - The player always goes first, their guess board is printed out to them for reference when entering a row and column, which must pass validation checks if not the user is prompted to enter valid data again. Once a valid input is entered the result of their attack is printed out to them before the guess board is updated and printed out to them again. The computers guess is printed out to the user alongside the computers board of where the player hit for reference to see where there shot landed. Validation checks prevent the user repeating already guessed spots on the board.
    - The sleep method of the time library and phase/line break is used to separate and emphasize the individual turns. There is a countdown of two seconds before the computer makes their attack and the terminal is updated this also adds more suspense.

![Guess ship](/assets/readme_files/guess-ship.png)
![Guess again](/assets/readme_files/guess-again.png)

- Ship Display
    - Ships that haven't been hit are displayed on the player's board as the at sign "@".
    - Letters are used for the column display and numbers for the rows, this allows for easy differentiation when inputting coordinates.
    - The markers that have been used give a good level of contrast and distinction between the different markers and what they represent.  "@" to represent ships, "-" for a miss and "X" for a hit.

![Ship display](/assets/readme_files/ship-display.png)

- Game Play Display
    - Feedback to the user is provided constantly throughout all phases of the game.
    - All sequences are broken down to increase ease of use and clarity. The boards are updated appropriately as well as the hit counter incrementing when required.
    - A consistent use of the sleep method and phase/line breaks is also used throughout to increase ease of use and clarity.

![Game play display](/assets/readme_files/play-game-display.png)

- Play Again
    - Once all the conditions of an end game have been met, which is a player either computer or user has hit the total hit count of 17, the turn sequence is broken out off, with a win or lose message being displayed.
    - The player is them prompted to play again, input validation is used here to ensure a Y or N is entered.
    - If the user inputs with a "y" then the game is started from the beginning, else the player is told goodbye and the program ends.

![Result](/assets/readme_files/result.png)
![Result](/assets/readme_files/result-lose.png)
![End game](/assets/readme_files/end-game.png)

### Features to Implement in the future
*There are no features left to implement from the initial scope of my project, however I have some features that I would like to add in the future.*

- Print the Player Board and Computer Board side by side in the terminal, rather than on top of one another.
- Make a 2 player version of the game.
- Let the player choose the size of the board.

[Back to top ⇧](#)

## Issues and Bugs 
The developer ran into several issues during the development of the website, with the noteworthy ones listed below, along with solutions or ideas to implement in the future.

- Solved Bugs
    - A bug I came across was the players error message for when placing a ship which overlaps over existing ships or doesn’t fit the board was being printed when it was the computers turn to place its ships. I fixed it by using a for loop in the players turn of the place ship function to print the message therefore no message would be printed if the computers ship overlapped or did not fit the board. 

- Remaining Bugs
    - No bugs remaining.

[Back to top ⇧](#)

## Technologies Used
### Main Languages Used
- [Python](https://en.wikipedia.org/wiki/Python_(programming_language) "Link to Python Wiki")

### Frameworks, Libraries & Programs Used
- [GitPod](https://gitpod.io/ "Link to GitPod homepage")
    - GitPod was used for writing code, committing, and then pushing to GitHub.
- [GitHub](https://github.com/ "Link to GitHub")
    - GitHub was used to store the project after pushing.
- [Lucid](https://lucid.app/ "Link to Lucid homepage")
    - Lucid was used to create a flowchart of information, making the logic of the game easily understood.
- [Am I Responsive?](http://ami.responsivedesign.is/# "Link to Am I Responsive Homepage")
    - Am I Responsive was used to generate mock-up imagery of the terminal showing the game in use on Heroku.

[Back to top ⇧](#)

## Testing

Due to the nature of the project, testing has been implemented throughout the entire project mainly debugging through running the program in the terminal as well as debugging using the python debugger. This is shown by commits of refactoring code.
Sections of code where developed before implementation to make sure it worked and also where run through the PEP8 validator.
Tested with invalid inputs: Such as using Type Errors and Value Errors, string instead of integers, out of bound inputs, same input twice.
Tested in both Gitpod terminal and CI Heroku terminal.
Limit testing has been conducted by myself, users and peers on slack through the peer-code-review channel, there is currently no reported issues that cause the game to break.

#### New User Goals:
1. As a new user, I want to see clear instructions for gameplay.
  - when the program is run, an introduction appears, telling the user how to play the game.
  
2. As a new user, I want to see a visual representation of my remaining lives.
  - On entering a wrong letter or word, a section of Funny Bones the skeleton is created. When the user has run out of tries, the skeleton will be fully formed.

3. As a new user, I want the ability to replay the game.
  - At the end of each game, regardless of the outcome, the user is given the option to enter Y to replay or N to end the game.

#### Current User
1. As a current user, I want the ability to replay the game.
  - At the end of each game, regardless of the outcome, the user is given the option to enter Y to replay or N to end the game.

2. As a current user, I want the guess word to follow a certain theme.
  - The entire game is Halloween themed, with a list of words that follow this theme. From "cemetery" to "ghouls" and plenty more besides.

3. As a current user, I want the choice to use different themes.
  - Unfortunately, this feature was not able to be implemented at this stage. 
  - In future developments, the user will have the option to input a number from a list, referencing the theme they wish to play with. This will include separate pages for each theme's code and separate lists of words to import.

[Back to top ⇧](#)

## Manual Testing

### Common Elements Testing
Manual testing was conducted on the following elements that appear in the program:
     
- Due to the nature of the project, testing has been implemented throughout the entire project mainly debugging through running the program in the terminal as well as debugging using the python debugger.
- Sections of code where developed before implementation to make sure it worked and also where run through the Python validator.
Tested with invalid inputs: Such as using Type Errors and Value Errors, string instead of integers, out of bound inputs, same input twice.
- Tested in both Gitpod terminal and CI Heroku terminal.
- Limit testing has been conducted by myself, Family and peers on slack through the peer-code-review channel, there is currently no reported issues that cause the game to break.

[Back to top ⇧](#)

## Automated Testing

### Code Validation
The [PEP8 Online Checker](https://extendsclass.com/python-tester.html/) service was used to validate the code written in the run.py file.

**Results:**

<details>
<summary>run.py Validation results</summary>

![run.py Validation results](assets/readme_files/python-code-validator.png)

</details>

## User testing 

This was tested by some members of my family including my Mum and Sister and some people in the slack community were asked to review the site and documentation to point out any bugs and/or user experience issues. Also with the helpful advice and with guidance from my mentor throughout the process led to changes and improvements.

## Deployment
### GitHub
This project was developed using [GitPod](https://www.gitpod.io/ "Link to GitPod site"), which was then committed and pushed to GitHub using the GitPod terminal. To create a GitHub repository you must:

1. Sign in to your account on Github.
2. On the top left of the home screen, click the 'New' button.
3. Under 'Repository template', select the required template from the dropdown.
4. Enter a repository name and description of your project.
5. You can select if you wish to make this project public or private.
6. There is an option of adding a README file, a .gitignore file, or choosing a license.
7. Click the 'Create Repository' button and your repository will be created.


### GitHub Forking and Cloning
To fork and clone the project, you will need to follow these steps:

1. Forking a GitHub repository.

    You might fork a project to propose changes to the upstream, or original, repository. In this case, it's good practice to regularly sync your fork with the upstream repository. To do this, you'll need to use Git on the command line. 
    - Navigate to the repository you wish to fork.
    - In the top-right corner of the page, click Fork. 

2. Cloning your forked repository.
    
    - Navigate to your forked repository.
    - Above the list of files, click 'Code'.
    - To clone the repository using HTTPS:
        - Under "Clone with HTTPS", click the copy icon (a clipboard).
    - To clone the repository using an SSH key, including a certificate issued by your organization's SSH certificate authority:
        - Click 'Use SSH', then click the copy icon. 
    - To clone a repository using GitHub CLI:
        - Click 'Use GitHub CLI', then click the copy icon.
    - Open Git Bash.
    - Change the current working directory to the location where you want the cloned directory.
    - Type git clone, and then paste the URL you copied earlier. It will look like this:
        git clone https://hostname/YOUR-USERNAME/repo-name
    - Press Enter. Your local clone will be created.

### Deploying on Heroku
To deploy this project to Heroku from its GitHub repository, the following steps were taken:

1. In your repository, type "pip freeze > requirements.txt" to create the list of dependencies to the requirements.txt file. Save, commit and push your changes to GitHub.

2. Create an account with [Heroku](https://www.heroku.com/ "Link to Heroku site"), selecting Python as the 'Primary development language'.

3. Go to your emails and click the link to verify your email address. The link will bring you to a page where you can create a password. Create a password and log in.

4. On the dashboard, click the 'create new app' button. Enter a unique name for your app and select your region. Click 'Create App'.

5. Go to the settings tab and click 'Reveal Config Vars'. Enter PORT as the KEY value and 8000 as the VALUE value.

6. Click 'Add Buildpack' and select 'Python' and 'Nodejs'. Python must be on the top of the list. Click and drag the buildpacks to the correct positions if needed.

7. Go to the deploy tab and, under 'Deployment method', click 'GitHub' and then 'Connect to GitHub'.

8. In 'Connect to GitHub', search for the repository you wish to use, then click 'Connect'.

9. If you 'Enable Automatic Deploys', Heroku will rebuild the app every time you push a change to GitHub. You can also choose to manually deploy using the 'Deploy Branch' option. Heroku will build the app and when it is finished, click the 'View' button to open the terminal.

## Credits 

The webpage [GitHub Docs - Fork a repo](https://docs.github.com/en/github-ae@latest/get-started/quickstart/fork-a-repo "Link to a GitHub Docs article on cloning and forking a repository") was used to get instructions on forking and cloning a repository. This information was used in the Deployment section of the README file.

### Code 
The developer consulted multiple sites to better understand the code they were trying to implement. The following sites were used on a more regular basis:
- [Stack Overflow](https://stackoverflow.com/ "Link to Stack Overflow page")
- [W3Schools](https://www.w3schools.com/ "Link to W3Schools page")
- [github](https://github.com/renatalantos/Battleship-in-Python "link to another students game")
- [Heroku](https://fruit-hunter.herokuapp.com/ "Link to another students game on heroku")

[Back to top ⇧](#)

## Acknowledgements

- I would like to thank my family for their valued opinions and critic during the process of design and development.
- I would like to thank my tutor Seun, for their invaluable help and guidance throughout the process encouraging me to push myself and make a better project.
- Lastly, I would like to extend my deepest gratitude to the amazing people in Slack who helped me rigorously test every aspect of my site.

[Back to top ⇧](#)
