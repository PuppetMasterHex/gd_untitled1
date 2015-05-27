
# Battle system

Generally turn based.

All turns are planned before executing the first turn.

At the first turn it is possible to use instant abilities (Flash Heal, Instant Strike etc.).

Combat actions are executed in their [priority order](#priorities).

Combatants react towards attacks / magic with a predefined [Counteraction](#counteraction) strategy.

If the target of an ability is not available anymore (e.g. target dies/flees before the ability could be used) the turn of the caster expires.

## Abilities

The abilities are grouped in:
* [Magic](magic.md) (costs [Magic Points](attributes.md#magic-points)).
* [Skills](skills.md) (costs [Skill Points](attributes.md#skill-points)).
* **Block** Reduces physical damage taken by a percentage, more effective with a [Shield](items.md#shields).
* **Escape** May end the combat even when no [Victory](#victory) or [Death](#death) condition is met.

Skills may also combine a weapon with magic to a magical attack.

## Priorities

1. Priority 0: Always used before the first turn starts (instant abilities).
2. Priority 1: Executed in order depending on the [Speed](attributes.md#Speed) of the combatants.
3. Priority 2: Executed after all other combatants have acted in the current turn.


## Counteraction

Standard actions to be executed as reaction of being attacked, the player may choose one of them.

* **Dodge** May nullify any damage taken (instant abilities may not be dodged).
* **Counter** Any damage taken is unchanged, may attack the enemy with a counterattack.
* **Skill-Counter** Same as Counter but with a skill instead of a normal attack.
* **Spell-Shield** Reduces magical damage taken by a percentage, consumes [Magic Points](attributes.md#magic-points).
* **Spell-Counter** Any damage taken is unchanged, may cast a spell either on the enemy or on the player. E.g. [Heal](magic.md#heal) on the player or [Fireball](magic.md#fireball) on the enemy.


## Death

Player death results in game over.

Enemy death results in the removal of thatenemy from combat.
If there are no enemies left in combat the [Victory Screen](#victory-Screen) will be shown.

## Escape

**Success probe.**

1. When successful
   * Player escape results in [Victory Screen](#victory-Screen), but will not award any Money.
   * Enemy escape results in the removal of that enemy from combat.
2. When not successful
   * The turn of that combatant expires.

## Victory Screen

Shows how much experience and money the player gains.
Also shows ability experience