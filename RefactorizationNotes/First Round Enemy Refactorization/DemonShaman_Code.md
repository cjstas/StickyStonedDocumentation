# Player Code Notes
## First Impressions
 - There are a lot of class variables. Maybe some can be removed
 - The room connections seem loose. Maybe a signal could be sent from the room to the enemies on load.
  - This could be a call/response signal. Room loads, Enemy Loads, Enemy calls to room, Room responds with reference.
 - In process, rather than checking nav_target and room.started every tick, maybe handle this through func_refs?
  - Physics process could be refined here too
  - This could serve as a guide for a greater refactoring for second round of mobs
 - Navigation is Navigation. Needs reworked.
 - attacking variable used in attack function seems annoying. worthless check.
  - This could be handled through a func_ref as well.
  - The timer here could be  handled in a different way.
 - Glue faces same problem as BigDemon

## Forming Ideas & Digging Deeper
 - Many of the variables are related to navigation. It might be nice to group these together for a better understanding of how it can be refined for another round.
 - Call response system could be outlined through this class and then extended to others in second round
 - Process/physics process needs to be refined as previously stated
 - 

## Final Tasks
 - [ ] Normalize function/variable names
 - [ ] Group Navigation class variables together for clarity
 - [ ] Group functions together based on function. Establishing a good rule for other mobs eventually
 - [ ] Footing is not accounted for with this enemy. This needs to be added. can function off of current system and it will be picked up for later.
 - [ ] If BigDemon reworked, copy the process func ref system, otherwise, make it happen for process/physics process
  - [ ] Make sure to include glue spatter mode with this.

## Hard tasks Reserved for Later
 - [ ] Navigation needs looked at
 - [ ] Signals system needs created or extended to other mobs
 - [ ] Pick candidate for reworking reference. This is a good candidate as it is complex, but I understand most all aspects. Also is not too dependent on other systems currently