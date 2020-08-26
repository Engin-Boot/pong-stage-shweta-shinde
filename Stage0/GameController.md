# Game Controller
Consists of BallMovement, SlabMovement and ScoreKeeper module 

## Feature
This module controls the every game functions 

## Acceptance Criteria

### Scenario: When user opens the PingPong Game

  Given -The Menu Options are Visible

  When -The user clicks on "START" button

  Then -The game must start

### Scenario: When the game ends

  Given -The user is playing the game

  When -The ScoreKeeper returns "WINNER"

  Then -Game End, Display the "WINNER" player

