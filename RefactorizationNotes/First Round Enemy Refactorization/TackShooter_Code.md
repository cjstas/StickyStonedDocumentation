# Player Code Notes
## First Impressions
 - Simple and basic understanding of the tack shooter. Good
 - Much repitition. Could be simplified with looping or bundling individual tacks into a larger object
 - Tack shooters still persist after the room is over. Maybe they could die?
  - This would probably require an additional animation of it dying
  - Even without it, it could cut down on having a bunch of extra data sitting around

## Forming Ideas & Digging Deeper
 - Separate out into a couple of functions with func refs for activity rather than relying on the physics process alone. This will be less code branches=faster
 - Loop that repitition

## Final Tasks
 - [ ] Normalize function/variable names
 - [ ] Simplify the logic of the physics process (specifically tacks)
 - [ ] Break the activity into individual controls (with func_ref) as to avoid unnecessary variables/branching
 - [ ] Make this die on room objective complete

## Hard tasks Reserved for Later
 - [ ] room.objective_complete might function better as a signal sent out to all room objects.