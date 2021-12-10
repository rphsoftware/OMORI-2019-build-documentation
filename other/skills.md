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
Changes will be represented with an arrow (=>), the 2019 version of the value will be on the left side of the arrow, the release value will be on the right side.

### GAURD => GUARD (id: 2)
- Description: None => `"Acts first, reducing damage taken for 1 turn.\nCost: 0"`

### RUN AWAY (id: 6)
- Message: " flees." => " flees!"

The skill would not actually make the character escape in the 2019 build, but it does in the release build.

### ENEMY HAPPY SKILL (id: 12)

The skill would apply happy in a slightly different way, which was unnecessarily complicated in the final build

### ATTACK (id: 15)
- Message: `" attacks"` => `" attacks!"`

### TEST ATTACK (id: 18)
- Animation ID: 68 => 307
- Damage formula: `999` => `2` (Variation 20 => 0) 
- Message: `" attacks"` => `" attacks!"`

The skill also did not have a battle message type and whole action tag. This skill also inflicts *SAD* on the target in the release build but not in the 2019 build.

### ATTACK (id: 21)
- Element: Normal Attack => None
- Description: `"Omori's Basic Attack"` => `"OMORI's Basic Attack"`
- Base Success rate: 91% => 100%

This skill would not be hidden from the skill menu in the 2019 build but it is in the release build.
This change also applies to the two other attack skills (which are used to display different follow-ups)

### ATTACK NO ACS (id: 24)
- Element: Normal Attack => None
- Description: `"Omori's Basic Attack"` => `"OMORI's Basic Attack"`

This skill would not be hidden from the skill menu in the 2019 build but it is in the releae build.

### OBSERVER (id: 25)
- Description: `"Stare at an enemy\nReveals an enemies HEART and JUICE"` => `"Predicts who a foe will target next turn.\nCost: 0"`
- Message: `" focuses his vision!"` => None
- Speed: 0 => -1000

This skill would act completely differently to its release version. Upon being used, it would write in the battle log the current health and juice of the selected foe. *OBSERVE* was likely remade because of the health bar that is visible when selecting an enemy to attack.

### SAD POEM (id: 26)
- Description: `"Read a sad poem\nMakes someone SAD"` => `"Inflicts SAD on a friend or foe.\nCost: 5"`

This skill would be hidden from the menu in the 2019 build.

### STAB (id: 27)
- Damage formula: `a.atk * 2 - b.def` => `(a.isStateAffected(10) || a.isStateAffected(11) || a.isStateAffected(12)) ? a.atk * 2 : a.atk * 1.5 - b.def;`
- Juice cost: 15 => 13
- Description: `"Stab an enemy\nAlways deals a critical hit"` => `"Always deals a critical hit.<br>\nIgnores DEFENSE when OMORI is SAD. Cost: 13"`

This skill would, as described by the description, not have its secondary ability of ignoring defense against *SAD*
 foes in the 2019 builds.

### HACK AWAY (id: 28)
- Damage formula: `a.atk * 2 - b.def` => `(a.isStateAffected(14) || a.isStateAffected(15) || a.isStateAffected(16)) ? a.atk * 2.25 - b.def : a.atk * 2 - b.def;`
- Description: `"Swing your knife wildly\nAttacks 3 times hitting random enemies"` => `"Attacks 3 times, hitting random foes.\nCost: 30"`
- Juice cost: 25 => 30

### PICK POCKET => PICKPOCKET (id: 29)
- Description: `"Reach into an enemies pocket\nSteal an item from an enemy"` => `"DELETE"`
- Message: `" tries to steal an item."` => `" tries to steal an item..."`
- Message type: None => `PICK POCKET`

### BREAD SLICE (id: 30)
- Damage formula: `a.atk * 2 - b.def` => `a.atk * 2.5 - b.def`
- Description: `"Make an enemy into bread\nIf this skill defeats an enemy gain a bread"` => `"If this skill defeats a foe, gain BREAD.\nCost: 10"`
- Juice Cost: 12 => 10

This skill had the property to also remove the immortal property of a target if it has it.

### HIDE (id: 31)
- Description: `"Hide from you enemies\nEnemies cannot target Omori for 1 turn"` => `"Foes cannot target OMORI for 1 turn.\nCost: 7"`
- Speed: 2000 => 1000

### QUICK SLICE => LUCKY SLICE (id: 32)
- Damage formula: `a.atk * 2 - b.def` => `(a.isStateAffected(6) || a.isStateAffected(7) || a.isStateAffected(8)) ? (a.atk + a.luk) * 2 - b.def : (a.atk + a.luk) * 1.5 - b.def;`
- Description: `"A fast cut\nAttack goes first"` => `"Acts first. An attack that's stronger\nwhen OMORI is HAPPY. Cost: 15"`
- Juice Cost: 10 => 15
- Speed: 1000 => 2000

### TRICK (id: 33)
- Element: HAPPY => None
- Damage formula: `a.atk * 2 - b.def` => `a.atk * 3 - b.def`
- Description: `"Trick an enemy and hurt their feelings\nDeals extra damage to HAPPY enemies"` => `"Deals damage. If the foe is HAPPY, greatly \nreduce its SPEED. Cost: 20"`
- Hit type: Physical Attack => Certain Hit
- Juice Cost: 10 => 20

The ability to deal extra damage to happy foes was implemented differently in the release build. It uses the element system in the 2019 build and notes in the release build.

### SHUN (id: 34)

## Added skills
TODO
