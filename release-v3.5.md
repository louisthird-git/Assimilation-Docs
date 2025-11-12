# Release v3.5

* Released 2025-11-09
* [NexusMods](https://www.nexusmods.com/fallout4/mods/71744)
* [LoversLab](https://www.loverslab.com/topic/160109-assimilation/)

## Issues Fixed

* Transitioned Talk Help Quests from storing Quest Form to storing Quest FormID & plugin filename making it easier to develop external Talk Help Quest mods.
* Assimilation forces third person camera to be centered. Temp fix with "player.caa animarchetypeplayer". The hands-up animation is an AnimArcheType so need to confirm what was done before the problem occurred. Appears to be a PlayerRef.ChangeAnimArchetype(AnimArchetypeNervous) call to make the player nervous which isn't necessary and removed it.
* Today (9/12/2024) was a great day. A big issue that I thought was my fault is not my fault but instead a Bethesda bug documented [here](https://ck.uesp.net/wiki/ForceGreet_\(Procedure\)). It had been reported that NPCs would not always start a conversation with the player. Sometimes it would work, but often it would not and some Quest dialogue scenes would always work. It turns out if you have too many dialogue lines (and due to the number of factions I support I often do) it will not initiate the conversation. The solution recommended is a workaround: start with a simple generic dialogue line then once the conversation is started it can get more complex which requires me reworking some of the scenes.
* If you're Sex Attributes Desperate and talking to a doctor (who you cannot romance) there are no Talk options so just abort the conversation.
* Player is always relocated even if settings are turned off.  Found/fixed issue that wrong setting was being checked.
* Updated DD forms for their latest release.
* Player Assimilated dialogue inappropriate for certain factions (BoS should only salute BoS members). Found/fixed what I could.
* Mods that undress like CWSS or AN76 conflict when apparel is locked.  Need a way to delay re-locking till after redress by those mods.  Also, resetting the lock time.  Tricky but probably not impossible.  There is a difference between ones that should abort the redress (like conflicting clothing), and those that should delay and then re-lock (like undressing when using a toilet).  Aborting the redress is already implemented/working, but the delay/re-lock is not. Watched for furniture forms on sit/getup and AN76 keyword.
* [Fusion Girl](https://www.loverslab.com/files/file/18238-zex-fusion-girl/) and [True Wasteland Body (TWB)](https://www.nexusmods.com/fallout4/mods/36410) support. Both are similar to [CBBE](https://www.nexusmods.com/fallout4/mods/15) with slider names but different Vertices they effect and more spaces in the slider names (CBBE only has 2).  Need to test spaces in slider names to make sure they are working correctly (can use "7B Upper" and "7B Lower" with CBBE for that) and pick "muscular" slider names/values to be affected for FEV (and make them configurable in MCM).
   
## Features Implemented

* General  
  * Trigger possible assimilation via hotkey when not assimilated already.
  * Increase performance of applying physical changes (hair, apparel, skin, face) using cache picking mechanism. Not for body as it is already picked what to change.
  * Option that player makes noise when swinging, bashing, jumping, or swimming (it was easy as Player Menu Clapping already did this).
* Face  
  * Integrated with Scripted Face Tints (SFT): [https://www.nexusmods.com/fallout4/mods/76797](https://www.nexusmods.com/fallout4/mods/76797)
  * Create Medicated Face Wipes aid item that can erase one face damage tint (can be aid gift).
* Skin  
  * Apply Overlays via [Looksmenu](https://www.nexusmods.com/fallout4/mods/12631) from [Captive Tattoos](https://www.loverslab.com/files/file/10004-captive-tattoos-looksmenu-overlays-facial-tattoos-males-females/) thus not requiring [Tattoo After Rape](https://www.loverslab.com/topic/136928-aaf-tattoo-after-rape-1182020) to be installed.
  * Create Medicated Skin Patch aid item that can erase one skin damage overlay (can be aid gift).
* Body  
  * Metabolism: If you don't eat/exercise your body grows thinner by a small, balanced, configurable amount over time... like real people.
  * Walking/Standing-Still Bonus option: To aid in surviving while in faction, you get a tiny heal bonus while walking or standing still.
* Clothes  
  * Raiders / Super Mutant (ToneTigre Slave Clothes): [https://www.nexusmods.com/fallout4/mods/48685](https://www.nexusmods.com/fallout4/mods/48685)
  * Raiders / Super Mutant (Kharneth Slave Clothes): [https://www.nexusmods.com/fallout4/mods/53918](https://www.nexusmods.com/fallout4/mods/53918)
* Hair  
  * Ponytail Hairstyles v3.0: [https://www.nexusmods.com/fallout4/mods/8126](https://www.nexusmods.com/fallout4/mods/8126)
  * Trimming hair blocked during combat & pubic blocked when detected.
  * Scissors have a configurable (tiny by default) chance of breaking when trimming.
* Faction  
  * Alternate Ending quest: If not assimilated to a faction (chance failed), then there is a chance that an alternate ending quest can occur, mostly romantic but depending on the outcome of a small dialog can be other things (if installed) like being Bound In Public or POTC or Real Handcuffed or even Caps taken, etc.
  * Overseer quest: get assigned a random faction Overseer (and possibly shock collared) to check-in with on your progress or be punished.
  * Late to Overseer quest: Overseer sends a group of faction members to track you down and bring you back to them.
  * Increase the number of faction help quests available (i.e. the variety) when assimilated.
    * Watered Down: Fetch water (all)
    * Feed Me: Fetch food (all)
    * Signed, Sealed, Delivered: Deliver mail between mailboxes (all)
