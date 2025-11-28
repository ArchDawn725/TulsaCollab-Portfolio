# TulsaCollab-Portfolio

***TulsaCollab (2025)***

Tulsa Game Developers Community Project • Arcade Cabinet Submission

**⭐ Project Overview**

TulsaCollab is a collaborative community project developed by members of the Tulsa Game Developers group for exhibition on a physical arcade cabinet. Although not intended for commercial release, the project showcases professional-level engineering, team coordination, and optimized design tailored for unknown hardware specifications.

I volunteered and was selected as the Lead Programmer and Project Manager for the Unity submission. My responsibilities included:

Overall technical direction

Architecture design (single entry point, async initialization, pooling)

Task coordination across the team

Code quality enforcement

Version control workflows

Performance requirements for arcade hardware

Ensuring every contributor could onboard smoothly

This project reflects my ability to lead and manage a team while implementing scalable architecture that supports contributors with a wide range of experience levels.

**👥 Team Composition**

Under my direction, the development team includes:

Me — Lead Programmer & Project Manager

Programmer #2 — Player class systems & input

Sound Designer — SFX and audio implementation

2D Character Artist

2D Environment Artist

QA Tester

We used GitHub for version control with a script-claiming workflow to ensure no contributor overwrites another’s work.

**🎮 Gameplay Summary**

TulsaCollab is a 1–2 player top-down 2D roguelike, inspired by Vampire Survivors, Brotato, and arcade twin-stick shooters.

*Controller Requirements*

The design is bound by the arcade cabinet’s constraints:

1–2 players

Shared screen or 2-player split screen

Controller-based input (stick + buttons)

Keyboard + mouse support available for debugging

*Game Flow*

1. Loading Screen

    -Everything is initialized through async setup

    -Loading bar reflects real-time initialization

    -Highly optimized startup to accommodate unknown arcade hardware specs

2. Join Prompt

    -Retro arcade-style “Press any button to join” UI banner

    -Each player can join independently

    -Players choose a class once joined

3. Gameplay

    -Players move via joystick

    -Shooting is automatic

    -Buttons activate:

      -Class abilities

      -Items

      -Healing

      -Dodge/evade actions

*Room Progression*

-Defeat all enemies to unlock upgrades

-Each player chooses from three random class-based upgrades

-Players select the next room

-Enemy strength, count, and types scale per room

*Failure & Respawn*

-Players revive after a timer unless both are dead simultaneously

-Run ends on:

  -All players dead

  -Boss room defeated

**🧩 Key Features**

Designed specifically for arcade cabinet hardware

Local 1–2 player co-op

Split-screen mode with fallback to single screen

Retro-inspired joining system

Class-based player progression

Roguelike upgrade system

Scaling enemy waves and room-based progression

Full controller support

Auto-firing combat for accessibility

Clean, heavily commented codebase for contributors

Polished onboarding for developers with minimal Unity experience

**🏗️ Architecture Overview**

As Lead Programmer, I established all core architectural patterns before bringing the team onboard.

*Single Entry Point Initialization*

The main scene is intentionally empty except for a single Initializer object that:

Configures loading UI

Loads all core systems

Sets up asynchronous start functions

Ensures gameplay elements initialize in a deterministic order

Prepares pooling and room generation

This maintains clarity, scalability, and platform-ready optimization.

*Async Start Functions*

Most gameplay systems use custom async initialization, enabling:

Smooth boot flow

Non-blocking load operations

Modular component setup

Cleaner separation of startup logic

*Pooling System*

Both projectiles and enemies use an object pooling system for:

High performance

Consistent frame rates

Avoiding runtime allocation spikes

Supporting unpredictable arcade hardware

*Team-Friendly Practices*

Coding standards include:

Single-responsibility scripts

Strong naming conventions

Clear folder structure

Fully commented methods

Minimal Update usage

Easy-to-follow logic for newer programmers

This ensures all contributors—including beginners—can safely build on top of the codebase.

**🗂️ Key Scripts to Review**

(Filenames will be mapped once uploaded, but here are the responsibilities.)

*Core*

Initializer — Single entry point, async setup

GameManager — High-level game state + room transitions

PlayerJoinManager — Handles join prompts & player spawning

*Player*

PlayerClassSystem — Managed by the second programmer

PlayerInputHandler — Controller & KB/M input

AbilitySystem — Activates class abilities

Dodge/MovementSystem

*Combat*

AutoFireSystem — Weapon logic

ProjectileController — Pooled projectile behavior

EnemyBehaviorSystem — Enemy AI & pathing

EnemyWaveController

*Pooling*

ObjectPoolManager

EnemyPool

ProjectilePool

*Roguelike Progression*

UpgradeSystem — Random upgrade generation

RoomSelector — Next-room UI logic

RoomController — Enemy spawns & scaling

**🧪 Development Notes**
*Arcade Cabinet Constraints*

Because the cabinet specs were unknown, every decision prioritized:

Low memory use

Zero-instantiation gameplay

Predictable performance

Minimal GC pressure

Fast boot times

Controller-first UX

*Team Leadership*

Organized weekly progress updates

Guided inexperienced contributors

Enforced script ownership in GitHub

Provided architecture diagrams and onboarding docs

Maintained coding standards across all scripts

*Community-Driven Production*

The game represents collaboration, mentorship, and creative effort within the Tulsa developer community. It is one of your strongest examples of team leadership and collaborative engineering.

**🚧 Why This Project Matters**

TulsaCollab highlights:

Your team leadership as both project manager and technical lead

Your ability to architect a clean, scalable foundation for a multi-person team

Your skill in writing code that is readable for newer programmers

Your mastery of performance optimization for unknown hardware

Strong communication and coordination through version control

A polished, fun, and highly replayable roguelike experience

This project demonstrates how you lead, delegate, organize, and set standards—traits essential for senior-level engineering roles.

**📚 Lessons Learned**

Arcade hardware constraints require strict optimization from day one

Async bootstrapping dramatically improves load flow

Beginners thrive with clear documentation and safe architecture

Object pooling is essential for reliable cabinet performance

Local co-op design demands consistent UX clarity

Team communication is key in multi-contributor projects

**🛠️ Tech Stack**

Unity 2023 LTS

C#

Async/await initialization patterns

Object pooling

Unity Input System

Local co-op architecture

2D top-down rendering

GitHub version control and collaboration tools
