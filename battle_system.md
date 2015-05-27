
# Battle system

Generally turn based.
All turns are planned before executing the first turn.
At the first turn it is possible to use instant abilities (Flash Heal, Instant Strike etc.)
Combat actions are executed in their [priority order](#Priorities).
Combatants react towards attacks / magic with a predefined [Counteraction](#Counteraction) strategy.
If the target of an ability is not available anymore (e.g. target dies/flees before the ability could be used) the turn of the caster expires.



## Priorities

1. Priority 0: Always used before the first turn starts (instant abilities)
2. Priority 1: Executed in order depending on the [Speed](attributes.md).
3. Priority 2: Executed after all other combatants have acted in this turn.


## Counteraction

Standard actions to be executed as reaction of being attacked.

**Block**
**Dodge**
**Counter**

**Spell-Shield**
**Spell-Counter**


## Death

## Escape
