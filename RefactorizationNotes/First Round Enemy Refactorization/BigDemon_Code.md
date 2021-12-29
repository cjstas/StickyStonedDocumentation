# Player Code Notes
## First Impressions
 - Feet are handled via pits. Might need ro review this later
  - UpdateFooting is a heavy method to be running for every enemy on every frame. This could be temp fixed by only doing this when the room signals a target.
 - pathfind() is also heavy for a physics process call. Might be worth looking into nicer means for pathfinding (universal node system to avoid polygon pitfalls?)
 - Glue method is heavy

## Forming Ideas & Digging Deeper
 - Glue method could be a state of process handled by a func_ref similar to the controls that the player class now utilizes
 - It would be nice to not queue_free() the glue spatter on a timer as the killing of enemies makes it a risk that had to be individually addressed. Could simplify future development
 - feet_area does not need to be a class variable. Proven by player

## Final Tasks
 - [ ] Normalize function/variable names
 - [ ] Remove feet_area class variable
 - [ ] Rework the glued activity to function on a func_ref which is called through the process

## Hard tasks Reserved for Later
 - [ ] Review Feet system with Pitfalls
 - [ ] Review the glue spatter system