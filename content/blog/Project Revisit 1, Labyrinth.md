+++
title = "Project Revisit 1: Labyrinth"
date = 2023-12-21
draft = false
[taxonomies]
  tags = ['rust', 'game development']
  projects = ['labyrinth_rs']
+++


Let's take a look at one of my more recent projects, one that's most likely to come back from the dead: a map and procedural generation library for roguelike development called [labyrinth_rs](https://github.com/asuratos/labyrinth-rs). 

Labyrinth came about when I was attempting to build a roguelike, and I was considering how to do pathfinding when different modes of traversal were available. Often, roguelike maps assume only one way of traversal: walking, and other methods are exceptions to the rule (i.e. "flying" is just walking over a pit if the entity has a `can_fly` tag, entities can only walk into water tiles when an entity has the `can_swim`, etc).

That way of doing things is well and good, but only as long as all your entities are walkers first, and have other movement methods tacked on top of that. What if you have creatures that can swim and fly, but not walk? What if you wanted to make tiles where it was possible to walk, but not fly through? What if you wanted to add a new kind of traversal, with walls that required that traversal method?

So I went about building Labyrinth, which tries to generalize map traversal by giving every tile has a `can_enter` method, which takes an instance of the `MoveType` enum. It returns a boolean, which determines if an entity with that movement type can enter the tile. The maps themselves implemented the `Algorithm2D` and `BaseMap` traits from [bracket_lib](https://github.com/amethyst/bracket-lib), which meant any of the pathfinding algorithms within could be used.

Adding those extra steps to pathfinding would obviously incur a cost, but unfortunately I never got far enough benchmark and test the library. There's also one or two things about the library API that I'd want to change, should I go back for it.