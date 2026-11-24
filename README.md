# S.T.A.L.K.E.R.: Callsign "Polytech"

**A story and gameplay modification for S.T.A.L.K.E.R.: Call of Pripyat**

Game Design Document

---

## Table of Contents

1. [Experience Overview](#experience-overview)
2. [Experience Information](#experience-information)
3. [Gameplay Loop](#gameplay-loop)
   - [Gameplay Objectives](#gameplay-objectives)
   - [Gameplay Story](#gameplay-story)
   - [Gameplay Flow](#gameplay-flow)
4. [Core Mechanics](#core-mechanics)
   - [User Controls](#user-controls)
   - [Progression](#progression)
   - [Core Features](#core-features)
5. [Design Style](#design-style)
   - [Game Locations](#game-locations)
   - [Character Designs](#character-designs)
   - [Concept Art and Notes](#concept-art-and-notes)
   - [Reference Images](#reference-images)
   - [Bibliography](#bibliography)
6. [Monetization Strategy](#monetization-strategy)
7. [Risk Analysis](#risk-analysis)
8. [The MVP](#the-mvp)
9. [Target Dates](#target-dates)
10. [Credits and Additional Resources](#credits-and-additional-resources)

> [!WARNING]
> This modification works only with the project's fork of the OpenXRay engine:
> [serrhiy/xray-16](https://github.com/serrhiy/xray-16), branch
> [`callsign-polytech`](https://github.com/serrhiy/xray-16/tree/callsign-polytech).
> The engine was modified for this project, and the final quest does not work without it.

---

## Experience Overview

**Callsign "Polytech"** is a single-player modification for
S.T.A.L.K.E.R.: Call of Pripyat that adds a new non-player character, a
stalker known in the Zone as "Polytech", and a set of side quests and
gameplay mechanics connected to him. The main storyline of the original
game is not changed: all new content is optional side content.

### Concept

Polytech is a former engineering student who came to the Zone not for
money or fame, but for knowledge. For him, anomalies, artifacts and the
remains of Soviet research facilities form a vast unfinished laboratory.
He is not a fighter and rarely leaves safe territory, so he needs
someone who is able to go where he cannot.

Polytech is permanently located on the Skadovsk, the grounded ship on
Zaton that serves as the main stalker base of the location. The player,
playing as Major Degtyarev from the original game, meets him there and
can take side quests from him. The quests send the player into the Zone
to collect data, components and artifacts, test prototypes of Polytech
and help him with his research. In return, the player receives unique
rewards and access to the new mechanics of the modification.

### Design Pillars

| Pillar | Description |
| :-- | :-- |
| Optional side content | All quests are side quests; the player decides whether and when to take them, and the main storyline remains fully playable. |
| Single quest hub | All quests are given by Polytech on the Skadovsk, which makes the content easy to find and gives the character a clear place in the world. |
| Engineering theme | Quests and mechanics are built around research, prototypes and equipment rather than simply fighting. |
| Faithful atmosphere | The modification preserves the tone of the original game: isolation, danger and the mystery of the Zone. |

### Content Added by the Modification

- **New NPC** - Polytech, a stalker-engineer with his own backstory and dialogues, located on the Skadovsk.
- **Side quests** - a set of side quests given by Polytech, connected to his research and his past.
- **New mechanics** - systems that support the engineering theme (see [Core Mechanics](#core-mechanics)).
- **New items** - components, prototypes and rewards required by the quests and mechanics.

### Value for the Player

For players who have already completed Call of Pripyat, the modification
provides a reason to return to the Zone: a new character with his own
story, additional side quests on familiar locations and rewards that
change the way the player prepares for trips into the Zone.

### Requirements

- S.T.A.L.K.E.R.: Call of Pripyat, patch 1.6.02
- OpenXRay with the day-of-week extension (`CTime:dayOfWeek()` in Lua, console variable `g_show_week_day`); the final quest "Sine of Monday" depends on it. It is in the [`callsign-polytech`](https://github.com/serrhiy/xray-16/tree/callsign-polytech) branch of the engine fork

---

## Experience Information

| | |
| :-- | :-- |
| Genre | Story side-quest modification for a first-person shooter with RPG elements |
| Platform | PC, OpenXRay engine (Linux, Windows) |
| Base game | S.T.A.L.K.E.R.: Call of Pripyat 1.6.02 |
| Mode | Single player |
| Languages | Ukrainian, English |
| Playtime | About 1-2 hours |

---

## Gameplay Loop

### Gameplay Objectives

Help Polytech in three quests: get Rokovoy's router back, recover Max's
FPGA board and find out how Igorek computed the "sine of Monday".

### Gameplay Story

1. **Rokovoy's router.** Faraday is hiding with the router in a hut at the
   Forestry. The player can take it by force or escort Faraday to the
   Skadovsk through a bandit ambush.
2. **FPGA board.** Max, a FICE student, lost his board among the Electras
   in the Iron Forest. If the player carries it through an anomaly, it
   burns, and Polytech gives Max a cheap one instead.
3. **Sine of Monday.** Polytech remembers a night in room 207 of dorm 8
   when Igorek "computed the sine of Monday". The player collects Igorek's
   three notes (the last one is guarded by Mad Armlet), works out the day
   and the hour, and passes Igorek's exam at the Skadovsk bar.

### Gameplay Flow

Talk to Polytech on the Skadovsk → take the quest → go into the Zone →
return to Polytech for the reward → the next quest unlocks.

---

## Core Mechanics

### User Controls

Standard Call of Pripyat controls. New: right-click a note in the
inventory and choose "Examine" to read it as a handwritten page.

### Progression

The quests are taken one after another. Rewards are money, consumables,
an artifact and a unique rifle, TOR-168.

### Core Features

- Branching quests: the router can be taken from Faraday by force or by
  escorting him to the Skadovsk; the FPGA board can arrive intact or burnt.
- Day of the week in game time (engine extension): the PDA clock shows
  "Fri 21:00", and Igorek comes to the bar only on Fridays from 21:00
  to 23:00.
- An exam in dialogue: a share of loot for every right answer, and after
  a mistake the exam goes on next Friday.

---

## Design Style

The tone of the original game is kept; the new characters bring in
student life of Kyiv Polytechnic.

### Game Locations

All quests take place on Zaton: the Skadovsk, the Forestry, the Iron
Forest, the Shevchenko, the port cranes, the old gas station and the
burned farm.

### Character Designs

- **Polytech** - stalker-engineer, the quest giver.
- **Faraday** - stalker hiding with Rokovoy's router.
- **Max** - FICE student on the Shevchenko.
- **Igorek** - legend of dorm 8.
- **Mad Armlet** - bandit in a black sweatshirt with white flames (new texture).

### Concept Art and Notes

Not prepared.

### Reference Images

Not used.

### Bibliography

- [OpenXRay](https://github.com/OpenXRay/xray-16)
- Scripts and configs of the original Call of Pripyat

---

## Monetization Strategy

None. A free non-commercial fan modification.

---

## Risk Analysis

| Risk | Mitigation |
| :-- | :-- |
| The final quest needs an engine change | The change is small and kept in a separate engine branch (see [Requirements](#requirements)) |
| Old saves may break | Start a new game with the modification |
| Too much work for a student team | One quest per person, all on one location, reusing original game mechanics |

---

## The MVP

Polytech on the Skadovsk with three quests that can be played from start
to finish in Ukrainian and English.

---

## Target Dates

| Date | Milestone |
| :-- | :-- |
| September 2026 | Game design document |
| October 2026 | Polytech, the router and FPGA quests |
| November 2026 | The "Sine of Monday" quest |
| December 2026 | Submission |

---

## Credits and Additional Resources

- **Serhii Lytvynenko** - Polytech, the "Sine of Monday" quest, the engine extension
- **Yana** - the Rokovoy's router quest
- **Myroslava Saveniuk** - the FPGA board quest
- GSC Game World - S.T.A.L.K.E.R.: Call of Pripyat
- OpenXRay team - the engine
