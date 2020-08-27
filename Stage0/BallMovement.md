
# Ball Movement Module

This module controls the ball instance.

## Feature

It consists of-
  BallMotion -which moves the ball in the field(Changes the co-ordinates of Ball)
  BallCollision -checks if the ball collides with the wall or slab
  PlaceBallInCentre - Resets the co-ordinates of the ball to the centre

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
