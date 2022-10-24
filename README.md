# Battleship Game

![Battleship Mockup Images](readme_files/Images/responsive.PNG)

[View the live project here]()

## Table of contents
1. [Introduction](#Introduction)
2. [UX](#UX)
    1. [Ideal User Demographic](#Ideal-User-Demographic)
    2. [User Stories](#User-Stories)
    3. [Development Planes](#Development-Planes)
    4. [Design](#Design)
3. [Features](#Features)
    1. [Design Features](#Design-Features) 
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
To create a command-line application that allows the user to play a word guess game, .


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
        - Intrest in Ships
        - Interest in puzzles
    - Personality/Attitudes:
        - Focused
        - Forward-Thinking
        - Creative
    
The application needs to enable the **user** to:
- play the game "Battleship" using alpha characters and numbers.
- generate a random board on each play-through placeing ships in differant locations.
    




#### Scope
The scope plane is about defining requirements based on the goals established on the strategy plane. Using the information in the strategy plane, the identified required features have been broken into the following two categories.
- Content Requirements:
    - The user will be looking for:
        - Clear and concise instructions.
        - A consistent theme, such as Halloween 
- Functionality Requirements:
    - The user will be able to:
        - Enter either a letter or a whole word if they think they know it.
        - Replay the game.
        - End the program at the end of the game.


#### Structure
The project will be deployed to a Heroku terminal. There will be no styling aside from the image of Funny Bones built using special characters within the terminal. 


#### Skeleton
A flowchart was created to show the logic the functions would follow.

<details>
<summary>Lucid Flowchart</summary>
    
![Lucid Flowchart](assets/readme_files/battleship_chart.png)

</details>


### Design
#### Imagery


[Back to top ⇧](#)


## Features
### Existing Features


### Features to Implement in the future


[Back to top ⇧](#)



## Issues and Bugs 
The developer ran into several issues during the development of the website, with the noteworthy ones listed below, along with solutions or ideas to implement in the future.








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
    - Am I Responsive was used to generate mockup imagery of the terminal showing the game in use on Heroku.

[Back to top ⇧](#)


## Testing
### Testing User Stories

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
     
- Inputting a letter would tell the user if the entry is correct or incorrect. The image of the skeleton is built with every incorrect entry.

<details>
<summary>Letter Input</summary>

![Letter Input](readme_files/Testing/input_letter.gif)

</details>

     
- Inputting a non-alpha character will display a message to the user telling them the character is not a valid guess.

<details>
<summary>Invalid Character Input</summary>

![Invalid Character Input](readme_files/Testing/)

</details>



</details>



<details>
<summary>Input Error</summary>

![Word Input Error](readme_files/Testing/)

</details>


</details>



<details>
<summary>Win Game </summary>

![Win Game With Word](readme_files/Testing/)

</details>




<details>
<summary>Lose Game</summary>

![Lose Game](readme_files/Testing/)

</details>



<details>
<summary>Restart Game</summary>

![Restart Game](readme_files/Testing/)

</details>




<details>
<summary>End Program</summary>

![End Program](readme_files/Testing/)

</details>


[Back to top ⇧](#)



## Automated Testing

### Code Validation
The [PEP8 Online Checker](https://pep8online.com/) service was used to validate the code written in the word_list.py and run.py files.

**Results:**

- run file

<details>
<summary>run.py Validation results</summary>

![run.py Validation results](readme_files/Testing/)

</details>

- word_list file

<details>
<summary>word_list.py Validation results</summary>

![word_list.py Validation results](readme_files/Testing/)

</details>


## User testing 


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

[Back to top ⇧](#)

## Acknowledgements



[Back to top ⇧](#)