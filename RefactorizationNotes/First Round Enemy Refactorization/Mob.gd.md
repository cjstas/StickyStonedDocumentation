# Player Code Notes
## First Impressions
 - Having the GlueSplatter load here made sense for the scope before. It would be nice to replace this system with individual animations per mob
  - Save this for second round
 - File seems lightweight. This is nice, but the number of variables could be what is causing lag upon high number of mobs
 - Might be able to replace this file with file of static methods. Save this for rework of greater system

## Forming Ideas & Digging Deeper
 - If it is decided to remove this file, the static method file could define regular activity referenced with a func_ref
 - if this file remains, it might be worth making the file itself more comprehensive with real activity to be inherited. Worst case, some activity methods could be referenced more loosly


## Final Tasks
 - [ ] Reference to room can be established here since it is used for all enemies.
  - [ ] The room itself could also send out a signal with its current "state" upon it updating those variables. Refactor the room to support this and extend it to the mob & all mobs
 - [ ] Normalize function/variable names
 - [ ] Add logic for death on empty health to the process and remove it from individual enemies

## Hard tasks Reserved for Later
 - [ ] Need to review this and decide if this is the means we want or if a static reference file might be nicer.