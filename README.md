Introduction
============

Unity Crash Course aims to teach complete beginners the essential basics of Unity in just 90 minutes. It was written by Marc Lepage in August 2014, and heavily revised in March 2015.


Lesson 0 - About Unity
======================

Concepts learned: Unity overview.


Lesson 1 - Learning the Interface
=================================

Concepts learned: layout, views, scenes, saving.

<img src="screenshots/lesson1.png" alt="Lesson 1 Completed"/>

In the Project view, right click on Assets, create a folder, name it Scenes. In the file menu, save the scene as "Game" in that folder.

Save the scene often, in case Unity should crash, as Unity does not auto save. Also periodically save the project.


Lesson 2 - Creating the Arena
=============================

What you will learn:

* understanding the coordinate system
* creating primitive objects
* resetting transforms
* adjusting position and scale
* duplicating objects

<img src="screenshots/lesson2.png" alt="Lesson 2 Completed"/>

Unity's coordinate system is left-handed. From the perspective of an object, Z is forward, Y is up, and X is right. Rotate the scene view to match.

We want to create an arena consisting of four walls and a floor. While not strictly necessary, our hierarchy will be cleaner if we create an object solely to organize the walls and floor. In the hierarchy, create an empty object and name it "Arena". In the inspector, reset its transform using the gear pulldown.

Now we need a floor. In the hierarchy, select the Arena and right click to create a plane as a child of the arena. In the inspector, its transform should already be reset. The plane extends for 5 units in each direction in the XZ plane.

Now for the left wall. In the hierarchy, select the Arena and right click to create a cube as a child of the arena. Again its transform should already be reset. The cube extends 0.5 units in each direction; change its X position to -5.5 so it's adjacent to the plane. Change its Z scale to 10 so it extends the length of the plane. It does not matter that the cube extends below the plane: it won't matter for gameplay and it won't be visible to the player.

It's easiest to create the right wall by duplicating the left wall. In the hierarchy, select the left wall and right click to duplicate it. All that needs to change in its transform is the X position to 5.5. Alternatively, you could drag it by the red arrow in the scene view while holding command, so it moves in 1 unit increments in the X direction, until it is in the proper position.

Now for the near and far walls. In the hierarchy, select the Arena and right click to create a cube as a child of the arena. Change its Z position to -5.5, and its X scale to 12. Duplicate it and change its Z position to 5.5.


Lesson 3 - Materials
====================

What you will learn:

* creating materials
* adjusting colors
* choosing a shader
* applying a texture

<img src="screenshots/lesson3.png" alt="Lesson 3 Completed"/>

Our arena is colorless. Notice if you select any of its primitive objects (the plane or cubes) they use a material called "Default-Diffuse" which is boring white. Aside from being devoid of fun, it makes it more difficult to work with our objects in the scene view. We'll fix that by creating some colorful materials to apply to our primitive objects.

In the project view, create a new folder named "Materials". In that folder, create a new material named "Floor". Select it, and in the inspector, click on its main color to change it to some shade of blue.

With the materials visible in the project, select the arena's plane in the hierarchy, and drag the floor material onto the inspector. This applies the floor material to the floor object; it should change color appropriately in the scene view.

Create a new material named "Wall" with a different shade of blue. You can quickly apply the material to the four walls by dragging it from the project view directly onto them in the hierarchy or scene views.

Create another material named "Enemy" and make it a shade of yellow. Even without an object, we can preview it in the inspector. With the "Diffuse" shader it looks somewhat flat. That's good for the arena but we want our enemies to stand out. We can use the "Specular" shader which makes it look shiner.

Duplicate the enemy shader and name it "EnemyRush". Change it to a shade of red.

Duplicate one of the enemy shaders again and name it "Tank". Change it to a shade of green. Now we want to make the tank material more interesting by adding a camoflage texture. Typically textures are stored in a folder called "Textures" and a small random black/white texture has been provided. In the tank material's inspector, select it.

Notice that materials are effectively global: if you edit the material in an object's inspector, it edits the material itself, and all objects with that material will change appearance.


Lesson 4 - Creating a Tank
==========================

Concepts learned: rotation, hierarchy.


Lesson 5 - Creating Enemies
===========================

Concepts learned: prefabs.


Lesson 6 - Camera
=================

Concepts learned: camera.


Lesson 7 - Lights
=================

Concepts learned: light, shadows.


Lesson 8 - Scripts
==================

Concepts learned: setting up game objects for control.


Lesson 9 - Input
================

Concepts learned: Input, CrossPlatformInput, CN Controls, InControl


Lesson 10 - Asset Store
=======================

Concepts learned: importing from the asset store


Lesson 11 - Handling Player Input
=================================

Concepts learned: reading in joysticks, debug logging.


Lesson 12 - Tank Movement
=========================

Concepts learned: using physics to move, time.


Lesson 13 - Enemy Movement
==========================

Concepts learned: using physics


Lesson 14 - Collisions
======================

Concepts learned: collisions, tag


Lesson 15 - Tank Shooting
=========================

Concepts learned: instantiate, destroy, physics forces


Lesson 16 - Audio
=================

Concepts learned: audio