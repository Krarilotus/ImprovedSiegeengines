# Improved Siegeengines

A UCP3 module for Stronghold Crusader that makes the AI use its siege engines properly:
catapults and trebuchets shoot from range instead of rolling up to the wall, siege tents stop
drifting away in long games and are placed by the engine's range, siege towers find walls to
dock at (diagonal ones too) or walk with the army until they can, and portable shields stay
with their own troops. The player-facing description is in
[module/locale/description-en.md](module/locale/description-en.md).

## Configure the module

1. Enable Improved Siegeengines and its Map Extensions dependency in UCP. Open
   **Customizations** and find its options under **AI**, **Bugfixes**, **Balance Changes**
   and **Miscellaneous**.
2. Choose the individual features, apply the configuration and restart the game. Click a
   setting title for details. The module supplies its defaults, so you can start without
   a separate configuration file.
3. For ranged AI engines, **Improved target search** enables the base targeting behaviour
   used by **Stop and shoot on the way** and **Shoot at other enemies**. Dropping destroyed
   targets and reducing scatter have independent settings. Set scatter to 100% to use the
   original aim. The default is 50%. For comparison: the game lets a catapult rock land up
   to 12 tiles short (4 long) and 6 to the side, and a trebuchet up to 6 to the side, so at
   long range most shots hit open ground in front of the wall.
4. To carry foot soldiers, enable **Foot soldiers ride on siege towers**, select soldiers
   and click one of your siege towers. Select the tower and use its leave command to unload
   passengers first. A second leave command releases the engineers. AI boarding is a separate
   option and requires the passenger feature. Passenger lift changes only the drawing height.

Use Smarter Walls 1.0.16 or newer with this module. Smarter Walls used to do the diagonal
docking; older versions change the same piece of the game and the two get in each other's way.

Map Extensions stores boarding and riding state in saved games. A complete record that
passes validation is restored in the existing save format. Invalid records are skipped.

## What is in here

| Path | What |
| --- | --- |
| `module/` | the module itself (`init.lua`, `templates.lua`, options and texts) |
| `tools/publish.py` | copy `module/` into the game's `ucp/modules/improved-siegeengines-<version>` |
| `tools/check_sites.py` | every AOB, expected byte and operand, checked against both exes |
| `tools/check_static.py` | lua syntax, and every asm script assembled with UCP's own fasm.dll |

## Working on it

1. Edit `module/`, bump `module/definition.yml` (and the version line in the description).
2. `python tools/check_sites.py` and `python tools/check_static.py` - both must say ALL OK.
3. With the game closed: `python tools/publish.py`, then F5 and apply in the UCP3 GUI.

## How it works

* **Catapults**: one hook in `harassBuildingsWithSiegeAI` where the game starts its own
  direction-by-direction search; a ring scan out to the engine's range (from the game's range
  table) for the nearest enemy wall or damageable building, shot through the game's own path.
* **Tents**: wrappers on `placeSiegeTentAtAttackAngle` and
  `placeSiegeTentOrTunnelAtSuitableLocation` set a distance band for ranged engines; the spot
  test in `algFindAttackAngle` and the layer test in `findAppropriateLocationForSiegeTent`
  check it against a chamfer distance map from the attacked castle's walls and fortifications.
  The spot test also frees spots whose troop is gone, whose 3x3 is clear and that no enemy
  troop can reach.
* **Docking**: `findFreeTileNearby` wrapped - the game's spot, then a diagonal corner dock,
  then the same wall up to three tiles along, in a fixed order.
* **Shields and towers**: the game's shield and tower branches in `aiCommandSiegeEngineTribes`
  are skipped; at its end the AI's shields, towers and ranged engines are collected in asm and
  lua gives the orders.
