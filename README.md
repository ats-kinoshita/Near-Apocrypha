# Near-Apocrypha
A collection of design notes and pages on action/adventure RPGs.

## Principle of Play

### Player Control
As I prototype games it is clear to me that the root of play is found in the PlayerController. The game-feel is rooted in how I/O map to player control, and that control is the basis of play. 

When it comes to tabletop gaming, this control comes in the form of action-resolution. Action-resolution comes in three flavours, obstacle impact, situational insight, and acquiring sources.

### Game Mastering
Gameplay scenarios are instantiated through the game-master - managing the assets and levels of the scene. The player then controls their character(s) to engage with and overcome the scenarios encountered on their quest.

In terms of tabletop game mastering, the actions they take are framing obstacles, revealing triggers, and inviting context. These are effectively Spawn/EventManager scripts, as well as dialogue prompts for player character perspective and understanding.

### Level Design
The layering and interconnection of levels, as well as the way the players will explore and internalize the layout, is the secret to the Souls series' great success as RPGs. I wish to reverse-engineer principles which would guide me in creating similar levels.

My weakness as a game master is in level design. I don't know how to improvise levels, nor how to narrate their intricacies in a digestible manner. Level design is narrative design - I believe there is a lead in following Ki-Sho-Ten-Ketsu structure in how a level is created and converyed to the players. 

### Old-School Influence
From Ueda and Miyazaki, first comes play, then comes plot, and last is story. Likewise, the play of the level comes from each individual room's narrative structure, then when stitched together each path's, and last the intricate topology that comes from the complete structure. 

These levels form a complex dungeon in the traditional D&D sense - with levels of escalating risks and rewards. By stacking so many levels on top of each other, the layout becomes topologically a dungeon like those of OD&D, similar to the Caverns of Thracia.

## Xandering the Level Design
Based on Justin Alexander's excellent analysis of old-school dungeon designs, there are some key features of Xandered design:

1. Multiple Entrances - in the context of a hub world, there are multiple paths out from the hub as-opposed to into the dungeon. Usually there is one immediate approach, with multiple hidden or difficult secondary (and tertiary) entrances which reward venturous players.

2. Loops - branching paths and multiple entrances  allow for choice, but are functionally linear in design (i.e. in practive you follow a branch to its end, and either backtrack or loop around to explore a different branch). 

3. Discontinuous Level Connections - as opposed to linear dungeons which continue from level 1 to 2 to 3 and so on, when you introduce multiple loops there should be paths between non-neighbouring levels. These skips create fruitful strategy in advancing through the world.

4. Secret & Unusual Paths - these are self-explanatory; rewarding curiosity and exploration is indispensable as a feedback-loop encouraging adventurous play.

5. Sub-Levels - the distinction between a level and sub-level is somewhat arbitrary, but perhaps a defining characteristic of a sub-level is that it departs from the main "sequence" of the dungeon. 

6. Divided Levels - similar to sub-levels, divided levels exist within the main "sequence" of the dungeon, but cannot be traversed without detouring through levels above or below.

7. Nested Dungeons - nested dungeons are taking sub-levels and divided levels to the extreme. By partitioning a dungeon complex within the main dungeon through means of sub-levels and divided levels, you can create a wholy distinct "sub-sequence" which explores a different, parallel "world".

8. Minor Elevation Shifts - when the Player Characters come to a staircase or elevator they may naturally assume they are going to a new level of the dungeon, but by including minor elevation shifts within the topography of a single level you can confound their internal compass and surprise them with hidden rooms and secret level skips.

9. Midpoint Entry - Another way to xander a dungeon is to create midpoint entries into the dungeon (or from the hub). This is seen most famously in Dark Souls in the return to Firelink Shrine from the first church/bell of awakening. This is essentially a skip from the entrance/hub to a deeper level, but is different from hidden secondary entrances in that it is expected to be a default entry point back into the level.

10. Non-Euclidean Geometry - Escher inspired spaces are a lot of fun as sources of spectacle and interconnection between non-adjacent places. 

11. Extradimensional Spaces - sections of a dungeon comlpex might link to areas entirely beyond the dungeon itself, such as the Painted World of Ariamis or the DLC area for Artoria of the Abyss in Dark Souls.

### Landmarks

As per Justin Alexander's article:

<blockquote>
"In order to successfully navigate a dungeon, the players will need distinct, memorable landmarks to orient themselves.  

If you’re designing a dungeon with lots of unique, interesting features, this problem will generally take care of itself: The players will glom on to whatever details particularly resonate with them, and use those details to guide themselves. On the other hand, it can never hurt to do another quick pass on your design and add in a few deliberate landmarks: A large bloodstain. A unique statue. A room of strange runes.  

Of course, players may also provide their own landmarks: “Hey, it’s that ogre we killed last week. Awesome.”  

On the other hand, you may also be able to use landmarks to mess with your players. Some landmarks could easily disappear. (An ogre’s corpse that gets dragged away by scavengers.) Those unreliable landmarks then open the question of how a missing landmark should be interpreted. (The runes are missing. Does that mean we’re in a different room? Or have the runes vanished?) And some landmarks which might seem unique could easily prove otherwise. (There’s the golden statue of a cyclops in a hexagonal room… but I thought that was on the other side of the complex. Did we get turned around?)  

To flip it around one last time, particularly crafty DMs might be able to hide reliable navigation information into seemingly unreliable landmarks."  
</blockquote>

The key to pathfinding are the landmarks along each sequence and fork, and the narrative that each player experiences comes in large part the events that landmark their journey. From Dark Souls, the curse mechanic was meant to be a disaster which occured, spurring an emergent quest/journey on which the player either endures the curse or finds a means to break it. This curse acted as a personal landmark, and was a key part of Miyazaki's design intent of systemic narrative.

## On Game Animation, Level Design, and Meaningful Mechanics

### Cognitive Maps

Paths - linear references. The most dominant feature and travel is concentrated on them. They are also the most temporal element, and are understood in scaling time.
Dead reckoning and path integration are basically the idea of continuity of where you are now is where you were before plus the sum of all the steps you took to get here.
In game development, camera movement needs to feed into the path integration of the player.

Landmarks - point references. Useful for orienting distances, but also orienting when trailblazing new paths or journeys. Only useful if stationary (large creatures are not good landmarks!). Also, much better when they are directional (i.e. not radially symmetric along the y axis). Like photogramatry, the reference needs to be made multiple times to make it stick!

Districts - zonal references (i.e. industrial zone, nature preserves, etc.). Use a squint test to distinguish clustered features. Districts have edges, and you go through these boundaries. A good metaphor is a colour-by-numbers painting. Districts are characterized by clustering of like objects (semantic or visual likeness).

Edges - linear, elevational references (due to movement being generally horizontal in nature). Vertical boundaries like walls, cliffs, forest boundaries, doors. Edges are thresholds which are very memorable if they are crisp or clean. These edges of districts should be deliberate, and the more distinct the clearer they are in memory.

Nodes - point references defined by paths. Usually hubs, places with many "ins" or many "outs". Very dense, and repeatedly used (and remembered). Need to be sign-posted due to complexity.

Plan first - the plan should be clear and legible. Section is where emotion comes out. Should be tested without a HUD or UI elements, as those lead to ego-centric frame of reference as opposed to a allo-centric frame of reference. For example, using GPS navigation primarily focuses on what your next maneuver is going to be, and breaking down the journey in that way leads to a breakdown of understanding. However, without HUD people tend to do allo-centric mapping, where the world exists and I am just moving through it - exploring the space and not the map.

tldr; 
1. there exists things called "cognitive maps", the digestion of the environments we go through
2. getting lost is when the cognitive map is misaligned with what the environment is telling you
3. to ensure spaces are robust and foster robust cognitive maps, we can be deliberate with the 5 elements: paths, landmarks, districts, edges, and nodes

I think a key aspect of my favourite games is this allo-centric mapping. Hidetaka Miyazaki and Fumito Ueda's works all encourage this sense that the world has existed, and you are exploring it. They remove the arcade, player centric feel and add weight to the world with every design choice, and that is my ideal in terms of game design.

### Art of Game Design
"Life" in games is the wholeness and coherence of the game lenses, in particular the 15 principles in the Phenomenon of Life.

1. Levels of Scale
2. Strong Centers
3. Boundaries
4. Alternating Repetition
5. Positive Space
6. Good Shape
7. Local Symmetry
8. Deep Interlock
9. Contrast
10. Graded Variation
11. Roughness
12. Echoes
13. The Void
14. Inner Calm
15. Non-Separatness

Mechanics	Dynamics	Aesthetics
Systemic	Strategic	Narrative
Emergence

## Game Feel and A Theory of Gameplay Innovation
Sensitivity
Versatility
Combinatorial

Attack
Decay
Sustain
Release

Button inputs as actions
Contextual positioning and movement as inputs

Action Verbs are below the neck

Immediate Outcome - Delayed Outcome
Interpreted Input - Direct Control
