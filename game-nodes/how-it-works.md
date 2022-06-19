---
cover: ../.gitbook/assets/Energy8LabsHeader.png
coverY: 0
---

# How does it work?

**For example, a user sends a withdrawal request from a game server.**

1. The user opens our bridge application, selects a game and makes a withdrawal request\
   &#x20;                     ↓
2. Sends a withdrawal request to the game\
   &#x20;                     ↓
3.  Is the balance in the game correct?

    **·** If “False”, then transaction is canceled\
    **·** If “True”, then the balance on the game wallet is frozen\
    &#x20;                     ↓
4. Calls the game node system\
   **·** Selects an active game node or gets in a queue\
   &#x20;                     ↓
5.  The game node begins to work with blockchain\
    **·** If the address is correct - next step\
    &#x20; else **** - cancel transaction\
    **·** If the chain is correct - next step

    &#x20; else - cancel transaction

    **·** If there are enough funds on the game wallet - next step

    &#x20; else **** - cancel transaction

    **·** If there are enough funds on the liquidity pool\* - Done

    &#x20; ****  else **** - cancel transaction\
    &#x20;                     ↓
6. Freezes the transaction amount in the liquidity pool\*\
   &#x20;                     ↓
7. Sends the assets to the user’s crypto wallet\
   **·** Waits for the user to get the assets\
   &#x20;                     ↓
8. The game node receives an award (PoS based)

\* - each game/game server has its own liquidity pool for funds safety.
