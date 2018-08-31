---
title: KISS RPG
layout: post
---

Kiss is a set of simple and all-purpose tabletop role playing game rules. 
Even though this document is focussed on the classic medieval fantasy setting, these
rules are highly adaptable for most campaign types.

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
You are free to share and adapt this material for any purpose, including commercially, 
as long as you give attribution.

License information available online at [{{ site.url }}/about]({{ site.url }}/about).

Rules available online at [{{ site.url }}]({{ site.url }}).

Source available at [https://github.com/moccalotto/kissrpg](https://github.com/moccalotto/kissrpg).

Dice and Tests
==============

To see if something succeeds, we roll a d10 (called the base die) against a given target number.
This is called a test. If you are particularly skilled at doing something,
you also add another dice (called a skill dice).
So for instance, if you have the melee skill at the journeyman level,
you roll d10 + d6 when attacking someone in melee combat.
The target number would be the targets Physical Defense rating.
If, on the other hand you are not skilled in melee at all, you would only roll your d10 against the same target number.

**Base Die**:
When you roll a 10 on your base die, you may roll it again and add the result.
You can do this as long as you keep rolling 10s.
If your base die has been modified (for instance, the base die is reduced as a consequence of damage and stress),
this rule still applies as long as you roll the highest possible number on the die.
This rule only applies to the base die.

> Re-rolling the base die is intended to introduce some luck into the game such that even a layperson
> will succeed on ocation.

**Hero Die**:
A sufficiently advanced and skilled character is usually better at everything they do.
As such they may add a hero die to all rolls.
So for instance, if a character has a d4 hero die, and has the melee skill at the journeyman level,
she may roll d10 + d4 + d6 when performing melee attacks.

**Karma Points**:
Whenever your character fails a meaningful roll (i.e.  one that actually affects the character, party or plot),
they are awarded a karma point. Your character can spend these points to create advantages later in the game.
Most notably, your character can spend 3 karma points to reroll their base die.
Character begin every session with exactly 2 karma points, no matter how many points they accumulated during
the previous session.

> Karma points are intended to soften the "blow" of missing a roll, as well as adding a
> luck/fate dimension to the game.
> We reset the karma every session to avoid power gaming through the accumulation of karma points.
> It also allows players to refresh their karma without having to fail any checks.
> High powered campaigns might reset the karma to 3 or 4, while more realistic campaigns might reset
> karma to 1 or 0. Some players prefer not to reset at all, possibly imposing upper limits on how many
> karma points a character can have.

Traits
======

New characters have two advantages and one disadvantage.
Consult the lists below for inspiration and make up your own to suit your campaign and style of play.

> By utilizing advantages and disadvantages, we eliminate the traditional stat-juggling, race-selection,
> and subsequent tweaking via feats, subraces, backgrounds, etc.
> If you want more powerful players, you could use three advantages and one or two disadvantages.



### Advantages

{% assign advantages = site.data.advantages | sort: 'name' %}

{% for item in advantages %}
**{{ item.name}}**:
{{ item.description }}
{% if item.remark %}
> {{ item.remark }}
{% endif %}
{% endfor %}

### Disadvantages
{% assign disadvantages = site.data.disadvantages | sort: 'name' %}

{% for item in disadvantages %}
**{{ item.name}}**:
{{ item.description }}
{% if item.remark %}
> {{ item.remark }}
{% endif %}
{% endfor %}

Skills
======

There are 6 skill levels:

Untrained, 
Novice     (d4),
Journeyman (d6),
Advanced   (d8),
Expert     (d10), and
Master     (d12)

> **Example**: A character who is a Journeyman in the Melee skill will roll d10 + d6
> whenever she makes a melee attack (provided her base die is d10).

A character starts with 3 skills at the novice level, 2 skills at the Journeyman level,
and 1 skill at the advanced level, all other skills are untrained.

{% assign skills = site.data.skills | sort: 'name' %}
{% for item in skills %}
**{{ item.name}}**:
{{ item.description }}
{% if item.remark %}
> {{ item.remark }}
{% endif %}
{% endfor %}

{:.page-break}
<br>

Equipment
=========

Players get 1000 copper pieces with which to purchase their starting equipment.
Characters begin play with 100 copper pieces.

**Load Points**:
Items have Load Points that represent how difficult they are to lug around.
100 coins take up one load point.

**Carrying Capacity**: A character can carry 10 load points. Certain advantages, spells, and items
may increase or reduce a character's carrying capacity.

### Armors

{% assign armors = site.data.armors %}

| Armor | Cost | Load | Defense | Defense |
|:------|:----:|:----:|:-------:|:-------:|
{%- for item in armors %}
**{{ item.name}}** | {{ item.cost }} | {{ item.loadPoints }} | {{ item.stressThreshold }} | {{ item.defense }} |
{%- endfor %}


### Goods

{% assign goods = site.data.goods %}

| Item | Cost |
|:-----|:----:|
{%- for item in goods %}
 **{{ item.name}}** | {{ item.cost }}
{%- endfor %}


Playing the game
================

Stress
------
When a character is wounded or receives some other kind of stress, they receive Stress Points.
Once a character accumulates 10 Stress Points (this is called the **Stress Threshold**),
they receive a Consequence and reset their stress-counter.
Stress points do not carry over.
> **Example**: If a character with 8 stress points receives additional 5 stress points from a single wound,
> they get a consequence, but the stress counter is still reset to zero.
> Thus, it would not have mattered if the character got a 2 point wound or a 15 point wound.

Note that certain special types of attacks allow damage to be carried over.
Such attacks are called vorpal attacks.

> **Note**: Stress and consequences is a way of ensuring that characters do not get one-shot-killed.
> Under normal circumstances, it would require a number of hits to kill a character.
> Vorpal attacks ensure that certain rare kinds of attacks can still kill a character
> in one go.

| Consequences      | Effect                                                |
|:------------------|:------------------------------------------------------|
| 0                 | No effects, base die is not modified (usually d10).   |
| 1                 | Base die is one step below nominal   (usually d8).    |
| 2                 | Base die is 2 steps below nominal    (usually d6).    |
| 3                 | Base die is 3 steps below nominal    (usually d4).    |
| 4                 | Unconsciousness.                                      |
| 6                 | Death.                                                |

### Stress Threshold
The stress threshold is the number of points of damage/stress the character 
can suffer before suffering a consequence. By default this number is 10.
Some monsters or NPCs may have a higher or lower number.
Certain effects (magical spells, items, buffs, debuffs, disease, etc.) can increase or reduce this number.
The character can also increase this number when she advances.

Healing and Recovery
--------------------

During combat, a character can take a *second wind* action that removes (base die) stress points.
This costs one karma point.

If resting for five minutes, a character can reset their stress counter to 0.

Immediately after combat, a character can spend karma point, rest for five minutes,
and remove one consequence.

A character who is trained in the *healing* skill can remove one consequence from a
willing subject. This takes about half an hour and requires a successful healing(10) test.

A character who receives 8 hours of uninterrupted rest in a safe haven can remove one consequence
when waking up.

A character may also receive magical healing.

> **Option**: If you want a more "deadly" campaign, you can rule that,
> no matter how a character is healed (magical healing, resting, or mundane healing),
> no more than two (or even one) consequences can be removed from
> that character per day (or even per session).

Combat
------

At the beginning of each combat round, each side rolls a d10.
The side with the highest roll gets to go first.

On a side's turn, each of its combatants may move up to 5 squares
and take one action.

An action can be:

- Move 5 more squares.
- Attack a target within range.
- Cast a spell.
- Spend one karma point and remove (base die) stress points.
- Drink a potion.
- Etc.

A character cannot use a missile weapon or cast a ranged spell if engaged in melee combat.

> **Areas**: If you prefer to simplify combat a bit, you can use areas instead of squares. An
> area could be a small- or medium sized room, or a part of a large room.
> Moving from one area to an adjacent area is equivalent to moving 5 squares.
> You can make melee attacks against any opponent in your area.
> You can make missile attacks in the adjacent areas.
> You can use ranged attacks and spells even if there are opponents in your area.
>
> If you want combat to be a bit more more slow-paced,
> you can rule that it requires an action to move from one area to the next.
> This way, characters cannot move more than one area per round.


Advancement
-----------

* Levels?
* XP per gold?
* Milestone?
* Fame / Legend?
