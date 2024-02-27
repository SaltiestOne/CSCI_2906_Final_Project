# TEESTFX

Welcome to TeestFX, the JavaFX port of the Modern Remaster of that game you* played on your** dad's old calculator! 
	<sub>*I     **my</sub>

## The Game

Our Hero can be male, female, or described in the second-person. That said, the Hero's past, personality, and procedures are better known by you than by me. For example: 

-"_He_" could be a light-skinned human, a dark-skinned elf, or a blue-skinned lizard. 

-"_She_" could be wearing an old cloak, shiny plate mail, or a floofy ballgown. 

-"_You_" could be a on a quest for money, revenge, or the future of your people.

All that the Hero ultimately needs to have are two working arms and the will to fight on. 

But like everything else, the Hero is defined just as much by actions as appearance. Some circumstance within the Hero's similarly nameless (and only slightly less featureless) fantasy realm will create a single-combat dual between the Hero and some foe or another. Each varies in fantasticality and familiarity, but all match or exceed the ferocity of their opponent. Initially, these enemies will be resisted by nothing sans a club. However, the Hero will gain access to new gear, martial maneuvers, and magical spells (all ambiguous in their specific appearance and method of use) as enemies fall. And these boons will certainly be necessary to turn the tide, as successive foes grow stronger faster than the Hero does.


## How to Run

Most Java compilers with JavaFX should be able to run Teest without any other assets, aside from the included files for object classes. A list of all 26 classes needed for the game is presented in Appendix II, for troubleshooting or in case of accidental deletion. If one has Java 8, and all necessary files are present, the game can also be run from the system command line once compiled there. 
<sub>~~Best practice is apparently including a Java install with the game but I haven't learned that yet so...~~<sub>

The gameplay isn't too obtuse, but as a summary: the Hero and the enemy at hand make Attempts to attack or defend against each other. until one is defeated. 
If the Hero wins, one of several boons can be selected. A new Stat can be learned, or a current Stat can be upgraded. These include all of the Stats available at creation, as well as many new Stats to supplement them. Upgrading a learned Stat’s level will increase certain values, as well as granting access to different Actions. A brief summary of each appears, along with the Actions learned from them, in Appendix I.

Certain enemies may have Actions as well. And as the Hero advances, enemies of all types will grow in power: their stats scale faster than the Hero's, including the power of their abilities. When the Hero runs out of upgrades at level 15, the game is finished.



~~The Pentagon
Each of the Five (non-**Neutral**) Attempt types interact with each other. Each beats two, loses to two, and ties with itself. Their relationships are as follows:

**QUICK** attacks happen before their **WIDE** or **TRICK** alternatives, but if the defender is prepared to **EVADE** or **BLOCK**, they won't make contact.
**WIDE** attacks follow **EVADEing** foes and bypass **TRICKs**, but are slower than **QUICK** attacks and can be **BLOCK**ed.
**TRICK** attacks will pursue an **EVADEing ** foe and get around a **BLOCK**, but are slower than **QUICK** and **WIDE** attacks.
**BLOCKing ** will stop **QUICK** and **WIDE** attacks, but **TRICK** attacks and **EVADEing ** opponents can get around.
**EVADEing ** will avoid **QUICK** attacks and flank **BLOCKing ** foes, but can be pursued by **WIDE** and **TRICK** attacks.

When winning a clash of Attempts, the winner will take their prepared action, while the loser will not. 

~~Basic Attempts
Any fighter can make a Basic Attempt using one of the main five types (**NEUTRAL** basics are not allowed). After winning a clash with a basic attempt, **QUICK**, **WIDE**, and **TRICK** will deal damage, and **EVADE** and **BLOCK** will grant Advantage. If the winner already had Advantage, **EVADE** and **BLOCK** will do damage but won't grant Advantage again. Regardless of its type, clashing with an attempt will Rust that type for the next turn.


~~ Action Attempts

Attempts can be made using a valid, usable Action as its base. Each Action has its own set attempt Type. Some may even deal damage as **EVADEs** or **BLOCKs** -- though in exchange, they won’t typically grant Advantage. They inherit Advantage from their user in the same way that Basic Attempts do, and they cause and are affected by Rusting normally as well. Regardless of the result of a clash made with an Action Attempt, resources will be spent according to the type of Action. If an Action Attempt wins its clash, it executes its effect immediately. If it loses, or ties (without breaking), its effect is lost.

~~Advantage
Advantage is a state granted when successfully **EVADEing** or **BLOCKing** a Basic Attempt, or by the effects of some special Actions. When one has Advantage, their clashes always break ties (even if the opposing action is a Tiebreaker), and winning a clash will have additional or more potent effects. Both basic and special actions benefit from this. However, Attempts with Advantage do NOT win against opposing types that beat them. For example, an Advantaged **QUICK** attack would be faster than any opposing **QUICK** attacks (and certainly against **WIDE** and **TRICK** attacks, as normal), but it would not overcome a **BLOCK**. Advantage is almost always lost the turn after it is gained (either from being spent or losing a clash). Advantage is a one-way relationship: if one fighter has Advantage on another, the latter cannot have Advantage on the former. Thus, a clash cannot involve two Advantaged Attempts.


~~Ties
If two actions of the same type clash, they may stalemate, with neither action happening. However, there are some exceptions. Some actions have a Tiebreaker effect, and will act as if they won when they are opposed by the same type. Many Attacking Stats have a "signature" type, whose basic Attempts will always be Tiebreakers (and will be more potent as well). This goes for enemies as well – most of them have one set “signature” type for their Basic Attempts. In addition, some special actions are natively Tiebreakers, as noted by their description. (In the current build, none do. TBA) However, neither signature attacks nor Tiebreaking actions will break ties if their type is Rusted, and two Tiebreakers clashing will stalemate. Non-Rusted Attempts with Advantage always break ties, and Tiebreaker actions do not break ties with Advantaged actions. **NEUTRAL** Attempts are always Tiebreakers, unless they are Rusted.


~~**NEUTRAL** actions
**NEUTRAL** Attempts are the "sixth" type of Attempt. No one can make a **NEUTRAL** Basic Attempt, so they only occur when a special skill has **NEUTRAL** as its type. The affects of **NEUTRAL** actions will always happen if the type is not Rusted. However, while **NEUTRALs** typically interrupt non-NEUTRAL Attempts, they do not cause the opposing Attempt to fail for the purpose of Rusting and resource costs. If an opposing non-NEUTRAL is Advantaged, it will always beat a **NEUTRAL**. **NEUTRAL** actions tend to have weaker Advantaged benefits, if any. In the event that two **NEUTRAL** Attempts clash, a Rusted one will always be beaten, and a non-Rusted one with Advantage will always beat the other. If neither is Advantaged or Rusted, one happens at random. **NEUTRAL** Attempts can Rust like normal types, and when they are, they will always lose. Thus, using two **NEUTRAL**s in a row is not recommended.


~~Rust
Making any Attempt - regardless of type or whether it won a clash - will Rust its type for one turn. Making an Attempt with a Rusted type will incur some penalties: Any Attempt that would be a Tiebreaker will no longer be so, and the action taken upon winning a clash will lose potency. Additionally, Rusted Attempts never grant Advantage, even if they otherwise should.

## Contributors

While there is no one else who directly contributed to this project (as all original objects and methods are mine), this version, as its name implies, was built for JavaFX. All credit for inherited code goes to them. This game would also not have been possible without the support and guidance of my instructors.


## Some Code I'm Proud Of
TBA, there's some for sure


# Appendix I: Stats and their Actions
Though the Hero cannot take the same Stat twice, different Stats have no restrictions on each other; taking one does not exclude or diminish another. The Hero will always have one Attacking Stat (labeled here and in game) active at a time. This Stat can make Basic Attempts, factoring in its signature type and damage scaling. The Hero’s Attacking Stat can be switched at any time before a clash at no penalty. Non-Attacking Stats lack the reliability to make Basic Attempts but can do various things with their Actions, and often have powerful Actions and/or passive benefits compared to Attacking Stats. Actions learned from any Stat can be used regardless of which Stat is actively Attacking.

##Sword (Attacking)
A reliable weapon whose signature type is **TRICK**, representing fast and precise moulinets.
### Sword level 2: ***Spin Attack***
Type: **WIDE**

Standard **WIDE** Action with strong potency. 
<sub>Do NOT attempt in a real sword fight. You could be hurt, or bullied by HEMA nerds.</sub>
Deals damage scaled from the _Sword_ stat. Has a wider damage range than a normal attack. If it kills, the enemy will be denied any chance of a mutual-kill, making it useful when both parties are close to death.
### Sword level 4: ***Mana Burst***
Type: **EVADE**

Sacrifices 50% of maximum Mana to deal a strong, _Sword_-scaled attack. Cannot be used if Mana is below that threshold.

Special: ***Ascended Mana Burst***

If the Hero lacks the Mana necessary to perform a _Mana Burst_ but also knows the _Ascend_ Spell, health can be sacrificed to perform the Skill. No confirmation is asked before _Ascend_ing a qualifying _Mana Burst_, so be careful if the Hero knows both Actions and is below 50% Mana.

##Spear
A classic weapon whose signature type is **QUICK**, representing its long reach.
###Spear level 2: ***Throw***
Type: **BLOCK**

Standard **BLOCK** Action with good scaling.
###Spear level 4: ***Heavenpierce***
Type: **TRICK**

Deals strongly-scaling damage, and damages Mana when used against MagiCritters and Spellcasters.

##Shield (non-Attacking)
An iconic implement that provides the Hero with a higher maximum health parameter as it levels.
### Shield level 2: ***Counter***
Type: **QUICK**

Acts like **BLOCK** and **EVADE** do during Basic Attempts: deals no damage but grants Advantage when winning a clash, unless the user already had Advantage, in which case, it deals damage.
### Shield level 4: ***Shield Bash***
Type: **BLOCK**

Deals damage scaling from the _Shield_ stat. Has a coin-flip chance to outright stun the target; if this succeeds, cooldown is increased by two.

##Arcanism (non-Attacking)
A field of magic that involves the study of magic itself. Has useful spells for any Caster and scales the Hero’s maximum Mana as it levels.
### Arcanism level 1: ***Drain***

Restores a small amount of health to the user scaled from the _Magic_ stat. This amount is also reduced from its target’s Mana, if it has any. If the target doesn’t, it deals light damage.


### Arcanism level 3: ***Ascend***
Type: **NEUTRAL**

Sacrifices a portion of current Health* to restore 50% of maximum Mana. Has no Mana cost itself.
<sub>*it's actually a level-scaled attack by, and against, the Hero</sub>





##Elementalism (Attacking)
A field of magic involving the study of the four elements – both their specialty and their harmony.
###Elementalism level 2: ***Temperence***
Type: **TRICK**

Heals its user for a moderate amount. If used with Advantage, it instead heals by spending as much Mana as available or as needed to heal to maximum health.

##Elementalism level 4: ***Towerfall***


##Appendix II: the files
Action
ActionButton
ActionDoer
ActionList
ActionUser
AllActions
Arcanism
Attempt
AttemptTypeButton
Caster
Conjuration
ConsolePane
Critter
DamageScaler
Elementalism
Entity
Fighter
FormattedButton
FormattedText
Formatter
Gauge
Gear
HealthScale
Hero
Humanoid
HumanoidMonster
Magic
MagiCritter
ManaScale
Monster
MonsterFlavor
MonsterReader
PaintableButton
PhantomPane
PronounSet
Scaler
Shadow
Shield
Skill
SkilledMonster
SkillUser
Spear
Spell
SpellMonster
Stat
SwitchAttackButton
Sword
TeestFX
UpgradeButton
Weapon

