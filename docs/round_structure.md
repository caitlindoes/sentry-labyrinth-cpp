# Round Structure (Text Based Game)

1) Game randomly selects a guild member.
2) Game randomly selects one of that member's statements from the statement pool.
3) Game displays:
   - the member's name
   - the statement text

4) Player enters:  1 = they believe this is TRUE   |   0 = they believe this is FALSE

5) Game checks:
   - check if this sentry was assigned truthful or liar at start
   - invert answer if liar
   - determine if player's guess is correct or incorrect

6) Game updates strike count and score.

7) If the player reaches 3 incorrect guesses -> immediate game over.

