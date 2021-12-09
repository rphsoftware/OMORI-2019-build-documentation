# other/Skills
**Changes from 2019 build**

# Description
Description of the file and its contents/use in the context of the game. If the use is only stipulative, it may be included here with an explicit disclaimer.

# Changes
Many skills have been changed since the 2019 build, the following list will describe changes as relative to the skill ID, meaning that if a skill has been moved in the list, it will be marked as both removed and added. A skill is considered changed if its overall use has remained the same but its name, description, stats or functionality have been changed.

`NOTE: If a removed skill does not have a juice cost, it would have been free to use`

## Removed skills
### ATTACK (id: 1)
- Description: None
- Message: `" attacks!"`
- Speed: `0`

This is the default skill that would be used upon using the *ATTACK* command, it was replaced in the final game with the *PLAY* skill that has inherited most of *ATTACK*'s stats, including its damage formula, icon, and notes, all of which are irrelevant in the context of the final game.
### HIT ALL ENEMY SKILL (id: 9)
- Description: None
- Message: `" attacks!"`
- Scope: All enemies
- Damage: `10` (Cannot deal a critical hit)
- Animation ID: 104

This is a debug skill that would deal a bit of damage to all enemeis.

### HIT ALL ALLIES SKILL (id: 10)
- Description: None
- Message: `" attacks."`
- Scope: All allies
- Damage: `10` (Cannot deal a critical hit)
- Animation ID: 184

This is a debug skill that would deal a bit of damage to all allies.

### HIT USER SKILL (id: 11)
- Description: None
- Message: `" attacks."`
- Scope: The user
- Damage: `10` (Cannot deal a critical hit)
- Animation ID: 184

This is a debug skill that would deal a bit of damage to the user. In addition, it would inflict *ANGRY* to the target (user in this case).

### COUNTER HEADBUTT (id: 75)
- Description: None
- Message type: `COUNTER HEADBUTT`
- Scope: The user
- Damage formula: `a.atk * 3 - b.def` (Cannot deal a critical hit, unused)
- Juice cost: 20
- Speed: 2000
- Indended user: AUBREY
- Animation ID: 232

This skill would give AUBREY the state *(A) COUNTER HEADBUTT* (id: 58) which would cast *HEADBUTT* (id: 69) when AUBREY is attacked.

### COUNTER ANGRY (id: 76)
- Description: None
- Message type: `COUNTER ANGRY`
- Scope: The user
- Juice cost: 20
- Speed: 2000
- Intended user: AUBREY
- Animation ID: 232

This skill would give AUBREY the state *(A) COUNTER ANGRY* (id: 59) which would cast *SELF ANGRY* (id: 77) when AUBREY is attacked

### SELF ANGRY (id: 77)
- Description: None
- Message: `" gets angrier"`
- Scope: The user
- Speed: 0
- Intended user: AUBREY
- Animation ID: 214

This skill would inflict *ANGRY* on AUBREY. It was seemingly meant to be the effect of skill *COUNTER ANGRY* (id: 76) although it is visible in the menu. This skill would also remove any *AFRAID* status, which would never happen in normal gameplay as skills cannot be used when affected by *AFRAID*

### DODGE ANNOY (id: 116)
- Description: None
- Message type: `DODGE ANNOY`
- Scope: The user
- Juice cost: 25
- Speed: 600
- Intended user: KEL
- Animation ID: 233

This skill would give KEL the state *(K) DODGE ANNOY* (id: 55) which would cast *ANNOY COUNTER* (id: 118) when KEL is attacked.


## Changed skills

## Added skills


# Speculation
`WARNING: The following section is speculative, none of it is confirmed information!`

Speculation on what the changes may signify about the game's development. If changes in other files are used for speculating, they must be linked here. Speculation must remain plausible and based on objectively verifyable information. Try to write this section in a way that its text cannot be taken out of context and misunderstood by, for instance, using the conditional instead of the past. 
