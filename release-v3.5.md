### **Prioritized Issues (these will roll off each release)**

* Transitioned Talk Help Quests from storing Quest Form to storing Quest FormID & plugin filename making it easier to develop external Talk Help Quest mods. \- FIXED, IN NEXT RELEASE  
* Assimilation forces third person camera to be centered. Temp fix with "player.caa animarchetypeplayer". The hands-up animation is an AnimArcheType so need to confirm what was done before the problem occurred. Appears to be a PlayerRef.ChangeAnimArchetype(AnimArchetypeNervous) call to make the player nervous which isn't necessary and removed it. \- FIXED, IN NEXT RELEASE  
* Today (9/12/2024) was a great day. A big issue that I thought was my fault is not my fault but instead a Bethesda bug documented [here](https://ck.uesp.net/wiki/ForceGreet_\(Procedure\)). It had been reported that NPCs would not always start a conversation with the player. Sometimes it would work, but often it would not and some Quest dialogue scenes would always work. It turns out if you have too many dialogue lines (and due to the number of factions I support I often do) it will not initiate the conversation. The solution recommended is a workaround \- start with a simple generic dialogue line then once the conversation is started it can get more complex which requires me reworking some of the scenes. \- FIXED, IN NEXT RELEASE  
* If you're Sex Attributes Desperate and talking to a doctor (who you cannot romance) there are no Talk options so just abort the conversation. \- FIXED, IN NEXT RELEASE  
* Player is always relocated even if settings are turned off.  Found/fixed issue that wrong setting was being checked.  \- FIXED, IN NEXT RELEASE  
* Updated DD forms for their latest release \- FIXED, IN NEXT RELEASE  
* Player Assimilated dialogue inappropriate for certain factions (BoS should only salute BoS members). Found/fixed what I could. \- FIXED, IN NEXT RELEASE  
* Mods that undress like CWSS or AN76 conflict when apparel is locked.  Need a way to delay re-locking till after redress by those mods.  Also, resetting the lock time.  Tricky but probably not impossible.  There is a difference between ones that should abort the redress (like conflicting clothing), and those that should delay and then re-lock (like undressing when using a toilet).  Aborting the redress is already implemented/working, but the delay/re-lock is not. Watched for furniture forms on sit/getup and AN76 keyword. \- FIXED, IN NEXT RELEASE  
* [Fusion Girl](https://www.loverslab.com/files/file/18238-zex-fusion-girl/) and [True Wasteland Body (TWB)](https://www.nexusmods.com/fallout4/mods/36410) support. Both are similar to [CBBE](https://www.nexusmods.com/fallout4/mods/15) with slider names but different Vertices they effect and more spaces in the slider names (CBBE only has 2).  Need to test spaces in slider names to make sure they are working correctly (can use "7B Upper" and "7B Lower" with CBBE for that) and pick "muscular" slider names/values to be affected for FEV (and make them configurable in MCM). \- FIXED, IN NEXT RELEASE

   
Prioritized Features (these will roll off each release)

* General  
  * Trigger possible assimilation via hotkey when not assimilated already. \- DONE, IN NEXT RELEASE  
  * Increase performance of applying physical changes (hair, apparel, skin, face) using cache picking mechanism. Not for body as it is already picked what to change. \- DONE, IN NEXT RELEASE  
  * Option that player makes noise when swinging, bashing, jumping, or swimming (it was easy as Player Menu Clapping already did this). \- DONE, IN NEXT RELEASE  
* Face  
  * Integrated with Scripted Face Tints (SFT) \- [https://www.nexusmods.com/fallout4/mods/76797](https://www.nexusmods.com/fallout4/mods/76797) \- DONE, IN NEXT RELEASE  
  * Create Medicated Face Wipes aid item that can erase one face damage tint (can be aid gift). \- DONE, IN NEXT RELEASE  
* Skin  
  * Apply Overlays via [Looksmenu](https://www.nexusmods.com/fallout4/mods/12631) from [Captive Tattoos](https://www.loverslab.com/files/file/10004-captive-tattoos-looksmenu-overlays-facial-tattoos-males-females/) thus not requiring [Tattoo After Rape](https://www.loverslab.com/topic/136928-aaf-tattoo-after-rape-1182020) to be installed \- DONE, IN NEXT RELEASE  
  * Create Medicated Skin Patch aid item that can erase one skin damage overlay (can be aid gift). \- DONE, IN NEXT RELEASE  
* Body  
  * Metabolism \- If you don't eat/exercise your body grows thinner by a small, balanced, configurable amount over time... like real people. \- DONE, IN NEXT RELEASE  
  * Walking/Standing-Still Bonus option \- To aid in surviving while in faction, you get a tiny heal bonus while walking or standing still. \- DONE, IN NEXT RELEASE  
* Clothes  
  * Raiders / Super Mutant (ToneTigre Slave Clothes) \- [https://www.nexusmods.com/fallout4/mods/48685](https://www.nexusmods.com/fallout4/mods/48685) \- DONE, IN NEXT RELEASE  
  * Raiders / Super Mutant (Kharneth Slave Clothes) \- [https://www.nexusmods.com/fallout4/mods/53918](https://www.nexusmods.com/fallout4/mods/53918) \- DONE, IN NEXT RELEASE  
* Hair  
  * Ponytail Hairstyles v3.0 \- [https://www.nexusmods.com/fallout4/mods/8126](https://www.nexusmods.com/fallout4/mods/8126) \- DONE, IN NEXT RELEASE (UPDATE REQUIRED TO 3.0 AS IDS CHANGED\!)  
  * Trimming hair blocked during combat & pubic blocked when detected. \- DONE, IN NEXT RELEASE  
  * Scissors have a configurable (tiny by default) chance of breaking when trimming. \- DONE, IN NEXT RELEASE  
* Faction  
  * Alternate Ending quest \- If not assimilated to a faction (chance failed), then there is a chance that an alternate ending quest can occur, mostly romantic but depending on the outcome of a small dialog can be other things (if installed) like being Bound In Public or POTC or Real Handcuffed or even Caps taken, etc. \- DONE, IN NEXT RELEASE  
  * Overseer quest \- get assigned a random faction Overseer (and possibly shock collared) to check-in with on your progress or be punished. \- DONE, IN NEXT RELEASE  
  * Late to Overseer quest \- Overseer sends a group of faction members to track you down and bring you back to them. \- DONE, IN NEXT RELEASE  
  * Increase the number of faction help quests available (i.e. the variety) when assimilated. \- DONE, IN NEXT RELEASE  
    * Watered Down \- Fetch water (all) \- DONE, IN NEXT RELEASE  
    * Feed Me \- Fetch food (all) \- DONE, IN NEXT RELEASE  
    * Signed, Sealed, Delivered \- Deliver mail between mailboxes (Settlers, Minutemen) \- DONE, IN NEXT RELEASE

