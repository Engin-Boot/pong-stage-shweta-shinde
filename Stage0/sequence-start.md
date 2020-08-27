# Interaction Sequences

## Start up Sequence-describe-how-your-modules-interact-to-start

Given that the game initializes and Menu is visible

1)When Player clicks on "START" button
    Then start the game

2)When Player clicks on "EXIT" button
    Then exit the game

## Movement Initiation-describe-how-modules-interact-to-make-the-ball-move

There are four entities initialized-
    one instance of class GameBall, two instances of Slabs, one instance of ScoreKeeper.
    The fieldInitializer method initials the member field of all instances.
The GameController Module controls all the functionalities of the game
The BallMovement Module controls the motion of the ball
The SlabMovement module controls the motion of slabs

## One score-describe-how-the-modules-interact-to-record-scores

Given that the game starts

When the penalty of any one Player reaches to MAXLIMIT.
Then end the game and declare other Player as "WINNER"
