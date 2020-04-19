# DHEWM 3 HARD CORPS 1.0.00
Updated files for Doom 3: Harqore 2 Dhewm 3 sdk.  This is an online back up of the updated files only during development.  The original sdk with all files is over at dhewm3 sdk's hub.  They are meant to be used with Hard Corps 1.0.00 for Dhewm 3 1.5.0+ after it is released.  It will not work with the original HardQore 2012 release.

Formerly known as HardQore 2 for Doom 3;  the Dhewm 3 version features many improvements and additions to the game while running on a modern source port of Doom 3.

List of updated features:

+Instant aim change when using "Contra", keyboard/controller, controls.  Removes the lag when changing angles. Massive improvement to firing.

+Multiple character select.  Different characters can be selected via the cvar pm_character.  Player def includes the full info.  characters can have different stats including health, armor, speed, jump height, starting weapon, etc.

+Instant melee weapon attack.  Each character has a melee weapon they can fire instantly instead of being forced to select them.  Most of the changes are in the soft code per weapon.  Pressing the bound impulse key will go straight to the attack and then back to previous weapon.  This makes melee weapons much more useful.  Scarlet Uses a sword, Doom Marine uses the chainsaw gauntlet.

+Replaced ROE bloom with Denton's HDR lighting system.  Note that the needed shaders and material file can be found in the Rivensin mod.  This is not the same HDR lighting system found in the Denton mod.  It has been modified and improved.  This includes incorporating rebb's improved ambient lighting.

+Jump through platform support.  Done with a trigger_jumpdown for above and just a trigger_multiple with wait set to 0 below.  Both entities should target the new func_platform_jumpthrough entity.  This functions the same as a fun_static with the new platform key set to 1...  this key is checked in the hard code for setting the contents to allow the player to go through or not go through.  Any entity with the platform 1 set will also allow everything but bullets to go through it as a useful by product.

+Waitfordamage key.  Checked from the player.def file. Used to enable and disable the player taking damage.

+Charge Attack added.  Dashing charge attacks can be done on ground or in air.  Dash charges damage enemies, push the player forward quickly and can be done in pairs.  Charge attacks also pass through enemies.  Player can do 2 in a row.  Gauge slowly recharges.  Adrenaline power up refils gauge.

+Slide attack is now apart of the Charge attack system and does damage the same way.

+noaim key for enemies.  When set to 1, enemies and bots will only shoot straight ahead in the direction of the player and not aim directly at them.  Very common side scrollers.  Ducking is now much more useful & dependable to avoid enemy fire.

+Disable_Moving key added to enemies.  When turned on the enemy will not move, only turn to face the player.  Useful for old school style enemy snipers.  Works on all enemeis.

+Enemies may pass/clip through each other if on the same team and the new team_nonsolid key is set to 1.  This is on by default.

+Always crouch key added to enemy soldiers.  When set to 1, they will crouch and stay that way.  0 to turn it off, 1 for a fifty chance they will stand or crouch.

+New "touchofdeath" key for enemies.  Enemies who have this set to 1 will damage the player via touch.

+Breakable objects have a new key to allow Everything to pass them except projectiles.  This is useful for item containers as seen in 2d games such Castlevania and Ninja Gaiden.

+Player invulnerability after taking damage and knock up.  After taking damage a script is called.  The script itself uses the new waitfordamage key to enable and disable the player taking damage for a brief period of time.  sdk is used to call the scripts and timer to turn off.  The player is also knocked up a bit. The knock up is done using the imported Rivensin full body animation system.
This system is very similar to classic platformer games such as Castlevania and Ninja Gaiden.  Visual fx is controlled in the player's script and def.

+Various adjustments to enemy AI and projectile distance for wide screen aspect ratios *Not finished*

+Camera updates: Enable/disable the camera following the player vertically similar to many 2d games.

+Display all ammo types in hud.  Unlike vanilla Doom 3, all ammo types available can be displayed in the hud.  The types shown are sdk controlled.  Easily expandable.

+Ported Rivensin's kick damage system.  Uses a chain of bones from the player to damage actors and objects.  Useful for melee attacks that require more accurecy and in a set direction.  Used heavily for Charge and slide attacks.

+Ported Rivensin's melee motion trail system.  Uses the melee bone and it's children on a world weapon model to create a trail.  Called from animation frames through automelee system

+Ported Rivensin's automelee system.  System uses the world weapon model's melee bone, must be named melee*, to detect hits and does not hit more than one target at a time.  Turned on and off via animations.  Includes damage multiplier and motion trails.

+Updated the fullbody animation system to Rivensin version.  This version adds in options to change the gravity, movement type, ammo use and much more.  Some bugs do occur when using anim_input for it, and other odd bits.  When combined with HQ2/Rivensin's new script based input systems; it allows for Mortal Kombat style special move inputs and dial in combos.  This opens the door to create 2d fighters with the source code.
