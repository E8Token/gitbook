---
cover: ../.gitbook/assets/Energy8LabsHeader.png
coverY: 0
---

# How it works?

**For example, user send withdrawal request from game server.**

1. User opens our bridge application, selects a game and make withdrawal request\
   &#x20;                     ↓
2. Sends a withdrawal request to game\
   &#x20;                     ↓
3.  Is the balance in the game correct?

    **·** If “False”, then transaction will be canceled\
    **·** If “True”, then the balance on the game wallet will be frozen\
    &#x20;                     ↓
4. Calls the game node system\
   **·** Selects active game node or gets in queue\
   &#x20;                     ↓
5.  The game node begins to work with blockchain\
    **·** If the address is correct - next step\
    &#x20; else **** - cancel transaction\
    **·** If the chain is correct - next step

    &#x20; else - cancel transaction

    **·** If the funds are enough on the game wallet - next step

    &#x20; else **** - cancel transaction

    **·** If the funds are enough on the liquidity pool\* - Done

    &#x20; ****  else **** - cancel transaction\
    &#x20;                     ↓
6. Freezes the transaction amount on the liquidity pool\*\
   &#x20;                     ↓
7. Sends the assets to the user’s crypto wallet\
   **·** Waits for user to get the assets\
   &#x20;                     ↓
8. The game node receives an award (PoS based)

\* - each game/game server has its own liquidity pool for funds safety.
