# The Essentials

1. Breakdown the problem into modules. Name each module
1. Rename the 'give-me-a-name...' files to reflect the module names.
Create more files for more modules.
Fill the responsibility and acceptance-criteria in each module.
1. Fill the sequence-start file with the details of module-interactions,
as indicated in that file.

## Components Diagram

```mermaid
graph TD;
    GameController-->BallMovement;
    GameController-->SlabMovement;
    GameController-->ScoreKeeper;
    SlabMovement-->SlabEventListener;
    BallMovement-->BallMotion;
    BallMovement-->BallCollision;
    BallMovement-->PlaceBallInCentre;
    ScoreKeeper-->AddPenalty;
    ScoreKeeper-->CheckPenalty;
    Ball-->BallMovement;
    Slab-->SlabMovement;

```
## Flow Diagram

```mermaid
graph TD
	A[OPEN] --> B[MENU OPTIONS]
    B[MENU OPTIONS] --> |onClick START button|C(Initialization)
    B --> |onClick EXIT button|Z(EXIT)
	C --> D(Place ball in the middle of field);
    D --> E(Move ball);
    C --> |on SlabChangeEventListener|F(Move slabs);
    E --> G{If ball hits on slab};
    G --> |Yes|K(Invert the direction of ball)-->E;
    G --> |No|H{If ball hits side walls}-->|Yes|I(Change angle and move ball)-->E;
    H --> |No|J(increment penalty and check scores);
    J --> L{if any score is above MAXLIMIT};
    L --> |No|D;
    L --> |Yes| M(Declare the winner)-->B

```

