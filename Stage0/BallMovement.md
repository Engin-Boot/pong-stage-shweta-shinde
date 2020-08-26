# Ball Movement Module

This module controls the ball instance.

## Feature

It consists of-
  1) BallMotion -which moves the ball in the field (Changes the coordinates of Ball)
  2) BallCollision -checks if the ball collides with the wall or slab
  3) PlaceBallInCentre - Resets the coordinates of the ball to the centre of the field

## Acceptance Criteria

### Scenario: The ball collides with the Slab

  Given - The user is playing the game

  When - the ball hits the slab

  Then - invert the direction of the ball

### Scenario: The ball collides with the side walls

  Given - The user is playing the game

  When - the ball hits the side wall

  Then - change the direction of the ball by ANGLELIMIT degree

  ### Scenario: The ball collides with the right or left wall
  Given - The user is playing the game

  When - the ball hits the right or left wall

  Then - ScoreKeeper increments the penalty and checks for penalty limit
