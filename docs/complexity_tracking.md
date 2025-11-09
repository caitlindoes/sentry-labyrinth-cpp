# Complexity Tracking Metrics + Measurement Design

This game will track complexities.

We will record the following metrics during runtime:

| Metric | Description | Why it matters (P v NP) |
|--------|-------------|----------------------------------|
| totalQuestionsAsked | raw count of questions interacted with | proxy for problem input size |
| totalCorrect | how many the player successfully deduced | accuracy vs search performance |
| totalWrong (strikes) | up to 3 ends game | boundary constraint similar to cost budget |
| elapsedTime_ms | time from start menu → game over | real world runtime measurement |
| branching_factor | number of available sentries / paths | maps to combinatorial explosion growth rate |

## How these will be stored
- integer counters increment per round
- timer captured using `<chrono>` high_resolution_clock

## How these will be printed at Game Over
- printed as a mini "complexity report" summary inside console
- example fields:
    - Questions asked: X
    - Correct deductions: Y
    - Time elapsed: Z ms
    - Observed branching factor: B

## Why we are doing this
The labyrinth problem is related to P v NP

Our code will show tangible runtime behavior growth as problem scale (more statements, more members) increases.
