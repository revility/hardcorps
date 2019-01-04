# hq2019
updated files for Doom 3: Harqore 2 Dhewm 3 port.  This is an online back up of the updated files only during development.  They are meant to be used with Hardqore 2 for Dhewm 3 1.5.0

List of updated features:

+Replaced ROE bloom with Denton's HDR lighting system.  Note that the needed shaders and material file can be found in the Rivensin mod.  This is not the same HDR lighting system found in the Denton mod.  It has been modified and improved.  This includes incorporating rebb's improved ambient lighting.

+New "touchofdeath" key for enemies.  Enemies who has this set to 1 will damage the player via touch.

+Waitfordamage key.  Checked from the player.def file. used to stop enable and disable the player taking damage.

+Invulneralbe to damage script.  After taking damage a script is called.  The script itself uses the new waitfordamage key to enable and disable the player taking damage for a brief period of time.
This system is very similar to classic platformer games such as Castlevania and Ninja Gaiden.  Visuals and amount of time is controlled in the player's script.
