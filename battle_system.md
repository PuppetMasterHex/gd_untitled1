
# Battle system

One or more Players fight versus one or more Enemies, Player versus Player is also possible.
Generally turn based.
Players and some enemies may have multiple turns per round.
All turns are planned before executing the first turn.  
At the first turn it is possible to use :boom: Instant Abilities (Flash Heal, Instant Strike etc.).  
Combat actions are executed in their [priority order](#priorities).  
Combatants react towards attacks / magic with a predefined [Counteraction](#counteraction) strategy.  
If the target of an ability is not available anymore (e.g. target dies/flees before the ability could be used) the turn of the caster expires.

## Abilities

The abilities are grouped in:
* [Magic](magic.md) (costs [Magic Points](attributes.md#magic-points)).
* [Skills](skills.md) (costs [Skill Points](attributes.md#skill-points)).
* **Block** Reduces physical damage taken by a percentage, more effective with a [Shield](items.md#shields).
* **Escape** May end the combat even when no [Victory](#victory) or [Death](#death) condition is met.



## Priorities

1. Priority 0: Always used before the first turn starts (:boom: Instant Abilities).
2. Priority 1: Executed in order depending on the [Speed](attributes.md#speed) of the combatants.
3. Priority 2: Executed after all other combatants have acted in the current turn.


## Counteraction

Standard actions to be executed as reaction of being attacked, the player may choose one of them.

* **Dodge** May nullify any damage taken (:boom:Instant Abilities may not be dodged).
* **Counter** Any damage taken is unchanged, may attack the enemy with a counterattack.
* **Skill-Counter** Same as Counter but with a skill instead of a normal attack.
* **Spell-Shield** Reduces magical damage taken by a percentage, consumes [Magic Points](attributes.md#magic-points).
* **Spell-Counter** Any damage taken is unchanged, may cast a spell either on the enemy or on himself. E.g. [Heal](magic.md#heal) on the player or [Fireball](magic.md#fireball) on the enemy.

## Range
Categories:
* Melee
* Ranged

Depending on the active weapon or class in case of monsters the combatant has a range category.  
Characters may not retaliate with a Counter if the enemy is not on the same range category as himself.

## Death

Player death results in game over.

Monster death results in the removal of that monster from combat.  
[Experience](attributes.md#experience) is awarded to the player that did the killing blow.  
If there are no enemies left in combat the [Victory Screen](#victory-Screen) will be shown.

## Escape

**Success probe.**

1. When successful
   * Player escape results in [Victory Screen](#victory-Screen), but will not award any Money.
   * Monster escape results in the removal of that monster from combat.
2. When not successful
   * The turn of that combatant expires.

## Victory Screen

Shows how much experience and money the player gains.  
Also shows ability experience gained.
