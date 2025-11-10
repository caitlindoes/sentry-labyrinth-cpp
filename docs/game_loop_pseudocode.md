# Game Loop Pseudocode (Text Based Version)

Initialize sentries (names + statements)
Randomly assign each sentry truth or liar (50/50)

Initialize complexity counters to zero
Start timer

WHILE totalWrong < 3:
    display available sentries by name (0..N-1)
    player selects a sentry index (validate)
    
    randomly select a statement from that sentry
    
    PRINT:
        Sentry Name
        Statement
    
    player inputs guess: (1 = TRUE, 0 = FALSE)
    
    actualTruth = (statement is actually a true fact)
    if sentry is a liar: actualTruth = NOT actualTruth
    
    if playerGuess == actualTruth:
        totalCorrect++
    else:
        totalWrong++
    
    totalQuestionsAsked++

Stop timer

PRINT complexity summary report
PRINT final score
END GAME
