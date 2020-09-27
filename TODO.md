# TO DO

## BUGS
v0.4.0 If you drag tokens into the Journal Entry, later adding new Actors will be ignored
        - should compare the Actors to the tokens and add ones that aren't represented
v0.5.0 You still see and hear HP rolling with Token Mold, even though the saved tokens are not changed        


## FEATURES

- Method 2 should create an embedded button and the button should be smaller (or linked to the embedded actors)
    - Or maybe the Actor links are individual buttons that populate the scene instead of showing the Actors
    -- Maybe shift-click shows the Actor or shift-click populates the Map
- Allow you to use Compendium entries as well as Actors
>>>- If you drag a Journal Entry to the Map, then intercept to change the icon etc.
- Improve the way the Journal Entry gets built to do more with the template and handlebars



## FIXED BUGS
FIXED 1. If the Actor embed text includes a number that is the only number, it will be used (Rion -L14) will result in 14 copies
FIXED (v0.3.4) Sometimes the corresponding Map Note is not deleted when you delete the Journal Entry
                - This happens for Method 2 because the scene isn't recorded
FIXED (v0.3.4) 5. With Method 1, the Journal Entry is re-opened when we create the Map Note
FIXED (v0.4.0) Error in onDelete of Tutorial Journal because oneDelete->close triggers another deletion call
NOT A BUG 6. Why do we sometimes get Unknown tokens being added - seem to be left over from previous interruptions in testing
FIXED (v0.4.0) v0.3.4 If you drag additional Actors to the Journal Entry, they are not getting added
FIXED (v0.4.0) v0.3.4 If you're on another Scene, the embedded button will switch scenes but the Quick Encounter button won't
FIXED (v0.4.1) v0.4.0 Method 2 isn't creating a Map Note - EncounterNote.place needs to place a Note or ask you to do that if one does not exist
FIXED (v0.4.1) v0.3.4 If you don't drag the Journal to the scene pressing the Quick Encounter button will fail silently
FIXED (v0.4.2) 0.4.1 If the number of Actors is part of a sentence, it won't be picked up correctly
FIXED (v0.4.2) 0.4.1 If you have a Player selected when you open your Quick Encounter, it will create a new one instead
            - Fixed: Ignore Friendly tokens
FIXED (v0.4.2) 0.4.1 Was using Dialog.prompt which doesn't exist in 0.6.6 - replaced with local implementation
FIXED (v0.5.0) 0.4.3 Saved tokens should bypass Token Mold
FIXED (v0.5.0) v0.3.4 If you click Quick Encounters again you get a second copy of the Tutorial
FIXED (v0.5.0) 0.4.3   Switch Scene still not working properly (qeScene.view() needs to wait until finished)
NOT A BUG  0.4.0   The TurnMarker app is throwing errors - are those related to 0.7.2 or in 0.6.6
        - Doesn't seem to be happening in 0.6.6
FIXED (v0.5.0) 0.5.0 Token.create() was returning a single token if you passed in a single-element array of token data; fixed to check
    - (would mean single-opponent encounters wouldn't be added to the Combat Tracker)


## COMPLETED FEATURES
DONE: (v0.4.0): If you're on a different scene, pops a dialog to check that you want to switch scenes
DONE v0.3.4: De-select all other controlled tokens when placing tokens to add them to the combat Tracker
DONE (v0.4.0) Replace forEach calls with for/of
DONE 2. If you open the Quick Encounter Journal with stored token information then use that in preference
DONE - Finish i18n for dialogs (but not for tutorial Journal)
DONE Method 1 should put the # of Actors in front of the actor link - this will enable later changing the specific actors
DONE (v0.4.1) Sum up and show the XP (5e only) for a combat - Total XP for this Encounter Journal, and a way of calculating per # of players
DONE (v0.4.2) Add the count x Actor to the documentation/tutorial
DONE (v0.5.0) - If you include Friendly tokens, show a dialog to check that's what you want
DONE (v0.5.0) - Method 1 should create the Map Note without asking
DONE (v0.5.0) - Method 2 will now always ask you to create a Map Note when you close the Journal Entry