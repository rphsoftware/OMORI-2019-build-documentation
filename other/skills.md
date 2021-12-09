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
- Speed: 0

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

### ANNOY COUNTER (id: 118)
- Description: None
- Message type: `ANNOY`
- Scope: 1 Enemy
- Speed: 0
- Intended user: KEL
- Animation ID: 55

This skill would inflict *ANGRY* on an enemy. It was seemingly meant to be the effect of skill *DODGE ANNOY* (id: 116) although it is visible in the menu.

### DODGE TAUNT TEXT (id: 119)
- Description: None
- Message: `" dodges the attack!"`
- Scope: 1 Enemy
- Speed: 0
- Intended user: KEL
- Animation ID: None

This skill would be used to display text. It was seemingly meant to be the effect of skill *YOU CAN'T CATCH ME* (id: 117) although it is visible in the menu. This skill was moved to ID 121 in the final game.

### ATTACK (id: 120)
- Description: None
- Messages: `" throws JACK!"`, `"ha ha ha ha ha ha ha ha ha ha "`
- Scope: 1 Random enemy
- Damage formula: `a.atk * 3 - b.def` (Cannot deal a critical hit)
- Intended user: KEL (?)
- Animation ID: 17

The purpose of this skill is unknown, its damage formula is the default formula and it has no notes. It is referred to as `// JACK ATTACK NO ACS`

### TENDERIZE (id: 150)
- Description: None
- Message type: `TENDERIZE`
- Scope: 1 Enemy
- Damage formula: `a.atk * 4 - b.def`
- Juice cost: 30
- Intended user: HERO
- Animation ID: None

This skill would've been a simple attack that cannot miss for HERO.

### ATTACK (id: 976)
- Message type: `SH ATTACK`
- Scope: 1 Enemy
- Damage formula: `a.atk * 2 - b.def` (Repeats x2)
- Intended user: SWEET HEART
- Animation ID: 132

This skill would've been a standard attack for Sweetheart during her fight. This skill is a stronger version of *ATTACK* (id: 972). This skill also has an even stronger version of itself at id 976, which repeats 3 times instead of 2.

### SWING MACE (id: 977)
- Message: `" swings her mace!"`
- Scope: All enemies
- Damage formula: `a.atk * 2 - b.def` (Repeats x2)
- Intended user: SWEET HEART
- Animation ID: 206

This skill would've been an AOE attack for Sweetheart during her fight. This skill is a stronger version of *SWING MACE* (id: 974). This skill also has an even stronger version of itself at id 979, which repeats 3 times instead of 2.

### SING (id: 1039)
- Message: None
- Scope: 1 Enemy
- Intended user: MUTANT HEART
- Animation ID: None

This skill appears to be an idle skill that wasn't completed in this build. This skill was replaced by *CRY* (id: 1039) in the release build.

### FEAR (id: 1130)
- Message type: `O SOMETHING BLACK SPACE`
- Scope: 1 Enemy
- Damage formula: `$gameParty.stressEnergyCount += 2`
- Intended user: OMORI'S SOMETHING
- Animation ID: 150

This skill would've increased the stress count during one of the final fights

## Changed skills
TODO
## Added skills
TODO
