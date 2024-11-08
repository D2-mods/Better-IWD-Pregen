==================================================
Option 1 - Revised script
==================================================
- Smarter spellcasting (better targeting, checks magic resist, etc.).
- May cast Barkskin, Mass Cure, Entangle, or Summon Insects once each per combat encounter. When the AI uses these spells, it doesn't require or consume any memorized spells.
- Slightly increased movement and casting speed.
- Teleports to catch up with the party (ex. while traveling with Boots of Speed).
- Preserves invisibility (won't attack or cast spells).
- Cooldown hotkeys to delay spellcasting (B to enable, E to disable).

Compatible with EEs and classic BG2 engine, including SCS.  
Not compatible with atweaks PnP Fey (use option 2).

--

Dimension Door: The nymph can teleport if conditions are met. It will alway teleport to either the nearest enemy or to a PC (usually, its summoner). It will not use Dimension Door if invisible, unless instructed to by the player (with the D key).

Marking: The nymph "marks" a PC as an object for various actions (by default, this is the summoner). If the marked PC is not on the map for any reason, the nymph will choose another PC on the same map. The nymph will always switch back to its summoner if in visual range. Note that the summoner, as an identifier, is not saved if a summon is still on the map (if reloading, script will default to Player1 as the "marked" PC).

--

Hotkeys:
- If the D key is pressed the nymph will teleport to its summoner (or other PC). Only works when not in combat.
- If the B key is pressed, the nymph will enter Cooldown for 3 rounds. Cooldown mode disables most combat actions.
- If the E key is pressed, the Cooldown timer is set to 0 (deactivated).


==================================================
Option 2 - Patch existing script (use with revision mods)
==================================================
- Adds Cooldown hotkeys (B to enable, E to disable)
- Adds D hotkey to teleport to party
- Teleports to party if not in visual range (and not invisible)
- Preserves invisibility (won't attack or cast spells)
- Usable with atweaks PnP Fey, as well as AI mods that still use NYMPH.BCS (ex. SCS)

NOTE: Dimension Door is more limited with this patch. Will only teleport to the summoner or Player1.


////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////

/*
*/