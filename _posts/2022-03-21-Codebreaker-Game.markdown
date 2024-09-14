---
title: "Codebreaker Game"
layout: post
date: 2022-03-21 00:00
tag: 
- java
- swing
- gui
- game development
image: null
headerImage: false
projects: true
hidden: false 
description: "This is an overview of the Codebreaker game Java program implementing swing."
category: project
author: James Gardner 
externalLink: false
---
## Overview
Codebreaker is a puzzle game developed in Java that challenges players to guess a randomly generated code made up of seven colours. The game uses Swing to provide the player with a Graphical User Interface (GUI), allowing players to input their guesses for the correct colour sequence within a limited number of attempts. After each guess, the game provides the player with visual feedback to help guide the player towards solving the randomly generated code.

<p align="center">s
  <img src="../assets/projectPostContent/codebreakerGame/StartingBoard.PNG" alt="starting Codebreaker board" width="80%"/>
  <br/>
  <em>Example screenshot of the Codebreaker starting board</em>
</p>

### Technologies Used
- **Java:** The language used to develop the Codebreaker game.
- **Swing:** GUI framework used to create the interactive interface.
- **Visual Studio Code:** IDE used for coding and debugging.

## Gameplay Mechanics
### Code Generation
The code is created when the game is loaded; it is a randomly generated sequence of four colours, selected from seven possible colour options. Each game begins with a unique combination, ensuring a different challenge every time.

### Guessing The Code
Players have a set number of attempts to guess the correct colour sequence. After each guess, visual feedback is provided to help guide the player towards the correct combination.

- A black circle with two ticks indicates that a colour is correct and in the correct position.
- A white circle with one tick indicates that a colour is correct but, in the wrong position.

To make the game more difficult, the feedback does not reveal which specific selected colours are correct, only that it has occurred. 

<p align="center">
  <img src="../assets/projectPostContent/codebreakerGame/MidwayComplete.png" alt="Partially completed game board" width="80%"/>
  <br/>
  <em>Example screenshot of the Codebreaker board part way through a game</em>
</p>

### Completing a Game
The game ends either when the player successfully guesses the code or when the player is unsuccessful and runs out of attempts.

In the event of the player guessing the code, a message is displayed to inform the user they were successful.

<p align="center">
  <img src="../assets/projectPostContent/codebreakerGame/CompleteSuccessful.png" alt="A successfully completed game" width="80%"/>
  <br/>
  <em>Example screenshot of a successful game</em>
</p>

If the player fails to guess the code within the set number of attempts, a message is displayed, informing the player that the game is finished and correct code sequence is revealed.

<p align="center">
  <img src="../assets/projectPostContent/codebreakerGame/CompleteFail.png" alt="An unsuccessfully completed game" width="80%"/>
  <br/>
  <em>Example screenshot of a unsuccessful game</em>
</p>

## Conclusion
