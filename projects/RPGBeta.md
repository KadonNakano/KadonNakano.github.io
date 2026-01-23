---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "RPG Beta (Text Adventure"
date: 2025-05-01
published: true
labels:
  - C++ 
  - OOP
  - JSON
  - Game Dev
summary: "Final project for ECE 205: a branching story RPG with turn-based combat driven by JSON."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

**RPG Beta** is a horror-themed, text-based RPG I built as my final project for **ECE 205 (University of Hawaiʻi, College of Engineering)**.  
The game combines a *branching narrative* (loaded from a JSON story file) with *turn-based battles* against undead enemies, implemented with an object-oriented character system (Knight/Wizard vs. Zombie/Zombie King).

### What I built
- **Data-driven story system**: scenes, choices, and outcomes are authored in `story.json`
- **Turn-based combat loop**: player-selected hero fights enemies using polymorphic `performAction()`
- **Character architecture**: shared base types + derived classes for professions and enemies
- **Multiple endings**: good/bad/death routes depending on choices + battle results

<hr>

### Sample excerpt (story JSON)
<pre>
"throne_room": {
  "setting": "You slip into the throne room... On the throne sits your fallen king...",
  "triggerBattle": 1,
  "victory": "good_ending",
  "defeat": "bad_ending"
}
</pre>

### Sample excerpt (C++ battle loop)
<pre>
void runBattle(PlayerCharacter* a, PlayerCharacter* b) {
    while (a->getHealth() > 0 && b->getHealth() > 0) {
        a->performAction(b);
        if (b->getHealth() <= 0) break;
        b->performAction(a);
    }
}
</pre>

<hr>

### Tech notes
- **Language**: C++
- **Library**: *nlohmann/json* for story parsing
- **Core concepts**: inheritance, polymorphism, composition via JSON data

<hr>

Source: <a href="https://github.com/KadonNakano/ece205-lab14a-RPGbeta-KadonNakano
"><i class="large github icon "></i>KadonNakano/ece205-lab14a-RPGbeta-KadonNakano</a>
