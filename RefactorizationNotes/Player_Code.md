# Player Code Notes
## First Impressions
 - Classwide variables are high. Should make little difference as there is only 1 player. Should still be refactored
  - foot1, foot2, feet_area, managed_pits, foot1S, and food2S seem like they could be condensed.
 - pitfall system needs reworked in general. May be out of scope for this card & saved for the pitfall card
 - Highlight process might be excessive. Need to dig deeper and think of a means of simplifying this
 - Structure used for input of dodge_roll & shoot_glue are similar, but I don't think refactoring is necessary as it might add unnecessary complexity
 - Direction is updated after the dodge_roll attempt. Confirmed that this means that pressing both keys at the same time results in undesired movement
  - Fix should be easy (should just be able to move this to after the direction is input & before the velocity is applied)
 - getclosestinteractable is called twice. Could result in unhighlighted item being picked updated
 - ignoring UpdateFooting for now
 - closest interactible closest is null why is obj.is_in_group("interactable") here? Should be assumed. Bad code elsewhere?
 - pickupInteractable() might be able to refactor into passing in that closest object. This would probably be better structuring for fancy activity later.
 - player_heal() could use refactoring, but would require refactoring of the heal item. (pickedUp() call is too specific)
 - GlueBullet instance could be used as an injection point for passing information for upgrades.
 - dodge_roll might be refactorable to be dependent on itself instead of a timer (more consistent maybe)

## Forming Ideas & Digging Deeper
 - foot1 & foot2 & feet_area may be removable as class variables. They are only used in UpdateFooting(), and they are refreshed there anyway.
 - the queued item on highlight (_process function) might be worth storing instead of calling getclosestinteractable() twice (and potentially having its results change).
  - This would increase ram usage slightly, but lighten processor load a bit more. Seems like a good change
 - Move dodge_roll attempt in controls() to after directional change
  - dodgeroll_Controls() functions off of velocity. This would need to be updated as well.
 - Need to attempt to remove obj.is_in_group("interactable") in getClosestInteractables. Should be assumed (test to make sure, and route back changes for bad code)
 - Research how dodge_roll could be self dependent and not timer based.

## Final Tasks
 - [x] Remove foot1, foot2, and feet_area class variables
 - [x] create queued_interact class variable updated in _process function. pickupInteractable() can reference this in place of recalculating this
 - [x] Move dodge_roll attempt in controls() to after directional change
 - [x] getClosestInteractables() check for if in group of interactables can be removed

## Hard tasks Reserved for Later
 - [ ] make dodge_roll self dependent instead of timer based.
