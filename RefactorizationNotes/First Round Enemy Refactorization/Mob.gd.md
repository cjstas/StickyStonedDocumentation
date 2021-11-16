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
 - [x] No immediate tasks for this file

## Hard tasks Reserved for Later
 - [ ] Need to review this and decide if this is the means we want or if a static reference file might be nicer.