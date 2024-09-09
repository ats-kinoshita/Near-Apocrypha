# 10,000 (Ten Thousand) // Last Stand
## Pitch
Wo Long + Wuthering Waves + Ghost of Tsushima + Vampire Survivor + 20 Minutes to Dawn musou style game, where aggressively attacking and parrying the enemies allows you to cut through swaths of enemeis and breakdown overwhelming bosses. Death is always one hit away, but with the tools of the trade and excellent execution you can overturn the odds and survive the last stand.

## Tags
tags: Musou, Villain Protagonist, Replay Value, Blood, (Co-op, Mature, Boomer Shooter)

## Tasks and Topics
I might be able to reappropriate the Xandering Dungeon Design into a sort of Xandering Sequence Design.

### TODO
3rd person player controller (parkour and martial arts movements)
Xandered Sequence Generator (Looped Levels vs One-Directional Plot Progression Graphs)
Level & Spawn Operators (extrapolating the Xandered Sequences)
AI/World State Machine (moment to moment state machine directing the active scenario)

## Gravity Wave
I want to implement a controller which internally manages character buoyancy, similar to how Mario's jump works. Implicitly, holding jump accelerates you up as long as you hold it down, until a break point where buoyancy is equalized. When the jump disengages, Mario sinks faster than the rate of gravity for a snappy motion. This snappy jump arc is what I aim to gamify. I want there to be a virtual pose to which the character snaps to - or rather I want the character to fall up and snap down. This arc is the basis of the motion, and being able to control the orientation of the snap will allow for parkour. Wall running too should feel snappy, so that the player bounds to the next position, and if they are blocked they try and leap to the edge and flip over like in Wuthering Waves.

I think one thing I could try is create a sprint simulator, where the elipse of the stride has to be timed with the compression of the body, so that the strike of the foot is timed with the arc of the body. First I would implement the rhythm-like game of timing the strides to the terrain, then introduce a left-stick controller for target facing direction.

One of the key "game feel" principles is that all motion is "falling with style". The idea is to make the locomotion itself fun and snappy, where the player "floats" forward/up and "snaps" back/down. To time the float and snap with incoming attacks is how parrying and jump countering will work, locking the character into a counter based on the smart-item style logic embedded in the attack/enemy. One of the key elements of this controller is the contextual snapping logic based in the environment and enemies. The principles of movement come from my experiences in Tae Kwon Do, where each strike is first chambered for power. In essence, when compared to my dream game of elemental movement, this is developing the "fire-style" of snappy, leaping action.

Maybe using negative edge for the chamber-release controls would be best. Hitting the key will chamber, then the release will strike. The visual indicators of how momentum rebounds and flows in and out of equilibrium like gravity waves will be one of the make-or-break aspects of the game I think.

When the legs are chambered for a walk the leading leg knee is slightly bent. When released, the leg kicks out and the heel generally strikes the ground. If there is a step ahead, either the body drops into the next step below or the raised leg catches the next step and rather than strike off pushes up to raise the body. Does this difference in push-up/catch-down require new inputs, or can I compress them into the chamber-release scheme? I think the fall down should look natural, so I am not worried about that, but the push up is a little different since the body snaps up. Maybe this is not a problem, and a slerp would allow me to hide the lift/fall of the rigid body.

I think first I would create the controller for the rigid body capsule, then attach IK to a puppet that animates on key-press and release. Once I get the feel of the walk cycle down I need to add directional inputs. Like in Mario, if the chamber is held too long the float forward will end and the snap down will automatically engage. This movement of the capsule is the first thing I need to rig and toy with