==================================================
Option 1 - Revised script
==================================================
- Smarter spellcasting (better targeting and not as wasteful)
- Won't cast statuses on undead or enemies with high magic resist
- Will teleport to catch up with the party (i.e. while traveling with Boots of Speed)
- Is more cautious at low HP if it has spells remaining
- Will not attack or cast spells at enemies if invisible
- Cooldown hotkeys to delay spellcasting

Compatible with EEs and original BG2 engine, including SCS.
Not compatible with atweaks PnP Fey.

DDoor: As in the unmodded script, the nymph may use Dimension Door at will if conditions are met. It will alway teleport to either the nearest enemy or to a PC (usually, its summoner). It will not use Dimension Door if invisible, unless instructed to by the player (with the D key).

Marking: The nymph "marks" a PC as an object for various actions (by default, this is the summoner). If the marked PC is not on the map for any reason, the nymph will choose another PC on the same map. The nymph will always switch back to its summoner if in visual range. Note that the summoner, as an identifier, is not saved if a summon is still on the map (so if reloading, the script will default to Player1 as the "marked" PC).

Hotkeys:
- If the D key is pressed outside of combat, and not in visual range of enemies, the nymph will teleport to its summoner (or other PC)
- If the B key is pressed, the nymph will enter Cooldown for 3 rounds; will not cast offensive spells or teleport to an enemy in Cooldown mode
- If the E key is pressed, the Cooldown timer is set to 0 (deactivated)


==================================================
Option 2 - Patch existing script
==================================================
- Adds Cooldown hotkeys (B to enable, E to disable)
- Adds D hotkey to teleport to party
- Will teleport to party if not in visual range (and not invisible)
- Will preserve invisibility

NOTE: Dimension Door is more limited with this patch. Will only teleport to the summoner or Player1.

Usable with atweaks PnP Fey, as well as AI mods that still use NYMPH.BCS (ex. SCS).