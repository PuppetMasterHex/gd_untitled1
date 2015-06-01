# Attributes

## Level

The level is increased by gaining experience points.  
Each level gives 5 attribute points that the player can spend on primary attributes.  
All primary attributes raise by +1 on levelup.

## Experience Points

Gained by killing enemies.

## Hit Points

If these reach 0 the character is [dead](battle_system.md#death).
Raise by +7 on levelup.

## Magic Points

Required to use [Magic](magic.md) type abilities.
**Don't raise on levelup.**

## Skill Points

Required to use [Skill](skills.md) type abilities.
**Don't raise on levelup**

# Primary attributes

## Agility

Increases hit chance by `Agility/40,96`%.
Increases [Counteraction](battle_system.md#counteraction) chance by `log10(Agility)*5`%.

## Vitality

Reduces Physical damage see [Damage Reduction](#physical-damage-reduction).
Each point of Vitality increase the [HP](#hit-points) by +1.

## Mind

Increases magical damage.
Reduces magical damage.
Each 5 points increase the [MP](#magic-points) by +1

## Speed

Decides the turn order in combat.
Increases [Counteraction](battle_system.md#counteraction) chance by `log10(Speed)*5`%.
Reduces enemy hit chance by `Speed/40,96`%.

## Strength

Strength increases physical damage by `log2(Strength)*10` and `Strength*0.25`%.


# Other Attributes


## Counteraction chance
## Hit chance
## Physical damage
Base damage from [Weapons](items.md#weapons) or other [Items](items.md)

## Physical damage reduction

### Flat
50% of the Armor and 50% of the Vitality value is reduced flat from the incoming damage.  

### Percentual
[Vitality](#vitality) / [Block](battle_system.md#abilities) provides a percentual damage reduction that is applied after the flat damage reduction.  
The value is capped at 66% damage reduction.  
Formula for Vitality is `log10(Vitality)*8+Vitality/40.96`  
25% damage reduction at 243 Vitality, 50% at 1057 Vitality, 66% at 1649 Vitality).  
The base value of Block is 20%, [Shields](items.md#shields) can add to that value.  

## Magical damage
## Magical damage reduction
