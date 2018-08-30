---
title: KISS RPG
layout: post
---

Kiss is a set of simple and all-purpose tabletop role playing game rules meant for all types of campaigns,
however the resources given in this document are designed for the classic medieval fantasy setting.
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
You are free to share and adapt this material for any purpose, including commercially, 
as long as you give attribution.


Dice and Tests
==============

To see if something succeeds, we roll a d10 (called the base die) against a given target number.
This is called a test. If you are particularly skilled at doing something,
you also add another dice (called a skill dice).
So for instance, if you have the melee skill at the journeyman level, you roll d10 + d6 when attacking someone in melee combat.
The target number would be the targets Physical Defense rating.
If, on the other hand you are not skilled in melee at all, you would only roll your d10 against the same target number.

**Base Die**:
When you roll a 10 on your base die, you may roll it again and at the result.
You can do this as long as you keep rolling 10s.
If your base die has been modified, this rule still applies as long as you roll the highest possible number on the die.
This rule only applies to the base die.

**Hero Die**:
A sufficiently advanced and skilled character is usually better at everything they do.
As such they may add a hero die to all rolls.
So for instance, if a character has a d4 hero die, and has the melee skill at the journeyman level, she may roll d10 + d4 + d6 when performing melee attacks.

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
and subsequent tweaking via feats, subraces, etc.
If you want more powerful players, you could use three advantages and one or two disadvantages.



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

A character starts with 3 skills at the novice level, 2 skills at the Journeyman level, and 1 skill at the advanced level,
all other skills are untrained.

{% assign skills = site.data.skills | sort: 'name' %}
{% for item in skills %}
**{{ item.name}}**:
{{ item.description }}
{% if item.remark %}
> {{ item.remark }}
{% endif %}
{% endfor %}

Equipment
=========


Playing the game
================

Stress
------
When a character is wounded or receives some other kind of stress, they receive Stress Points. Once a character accumulates 10 Stress Points, they receive a Consequence, but they then reset the number of accumulated stress points to zero. Stress points do not carry over. For example if a character with 8 stress points receives additional 5 stress points from a single wound, they get a consequence, but the stress counter is still reset to zero. Thus, it would not have mattered if the character got a 2 point wound or a 15 point wound. Note that certain special types of attacks allow damage to be carried over. Such attacks are called vorpal attacks.

Once per round the character can reduce the amount of damage she receives by 1 stress point. This costs one karma point.
Consequences
How do consequences affect the character?
The character should get weaker as they accumulate consequences.
Do consequences have names or named “levels”?
Is there more than one kind of consequence?¨
Is there an “unconsciousness” consequence?
Is there a “death” consequence?
Healing and recovery
How are stress points removed?
How fast do they regenerate naturally?
I think they regenerate on a “short rest”. (I.e. at the end of the scene).
Is there a “second wind” that can be used during combat?
I think yes.
Would a “second wind” cost TP?
Regenerating a little bit should be free, provided the cha spends their entire round doing it.
Regenerating by spending only your main action should incur a cost.
Regenerating a large number of points in one go should incur a cost.
Can spells remove consequences (almost) instantly?
Can medical technology remove consequences (almost) instantly?
Can consequences go away naturally over time?
Is there a limit on how fast consequences can be removed?
Does it cost FP to remove consequences?
Can costs be circumvented by “hospitalization”, prolonged downtime, etc. ?
If consequences can be removed by medical technology and magic, would an FP cost have to be paid by the doctor/caster?


Advancement
-----------
