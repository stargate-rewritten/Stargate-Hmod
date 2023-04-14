> **Note that a** [support discord](https://sgrewritten.org/discord) **has now been created!**

> **THIS IS AN [EXTENDED SUPPORT RELEASE](https://sgrewritten.org/esr) FOR VERSIONS b1.1-1.0!**<br>
> **This version extends Dinnerbone's original 2010 codebase, with some backported fixes**.<br>
> **THIS VERSION WILL RECEIVE NO SUPPORT BEYOND CRITICAL BUG FIXES**<br><br>
> **For modern versions of stargate, please look [here](https://sgrewritten.org/downloads) instead!**.

# Description
Create gates that allow for instant-teleportation between large distances. Gates can be always-open or triggered; they can share a network or be split into clusters; they can be hidden on a network or accessible to everybody.

- Player permissions -- let players build their own networks.
- iConomy support -- can add costs for create, destroy and use.
- Capacity to add custom gates, as well as some pre-set examples
- Message customization
- Gate options

## Background
- This plugin was originally made by Dinnerbone as an immersive transportation plugin for hMod.
- Over time, Sturmeh gradually took over most of the project's development.
- Shortly before porting SG to bukkit, Drakia forked Dinnerbone's hmod original to add some modern features.
- TheRaph later forked Drakia's version to update to later versions of hmod (137)
- This is an EXTENDED SUPPORT VERSION, backported to support versions 133+ of hmod in a modern context, and is minimally maintained by [SGR](https://sgrewritten.org).

# Documentation
## Instructions
### Building a gate:
    OO 
   O  O - These are Obsidian blocks. You need 10.
   O  O - Place a sign on either of these two blocks of Obsidian.
   O  O
    OO
 - Type a name on the first line on the sign, it must be less than 12 characters long.
 
### Sign Layout:
 - Line 1: Gate Name (Max 12 characters)
 - Line 2: Destination Name (Max 12 characters, used for fixed-gate)
 - Line 3: Network name (Max 12 characters)
 - Line 4: Options ('A' for always-on fixed gate, 'H' for hidden networked gate)

### Using a gate:
 - Right click the sign to choose a destination.
 - Left or Right click the button to open up a portal.
 - Step through.
 
### Fixed gates:
 - Fixed gates are like normal gates, but can only go to one destination.
 - If you create two fixed gates that point to eachother, you will have a two-way portal.
 - You can link gates to normal gates, or to other fixed gates which can link to another fixed gate etc. You can't link a normal gate to a fixed gate though.
 - Creating a fixed gate is the same as a normal gate, but you must specify the destination on the second line.
 - Set the 4th line to "A" to enable an always-open fixed gate.

### Gate networks:
 - Gates are all part of a network, by default this is "central".
 - You can specify (and create) your own network on the third line of the sign when making a new gate.
 - Gates on one network will not see gates on the second network, and vice verca.
 
### Hidden Gates:
 - Hidden gates are like normal gates, but only show on the destination list of other gates under certain conditions.
 - They are visible to anyone with access to the /stargatehidden command, or to the creator of the hidden gate.
 - Set the 4th line to "H" to make it a hidden gate.
 
## Configuration:
 - You can edit all values in stargate.txt to your choosing, mostly the RP text on doing actions involving a gate.
 - If you have iConomy, you can set "cost-to-use" and "cost-to-create" to modify how much money it will cost a user to use or create a Stargate, respectively.
 
## Permissions: (These are not in-game commands, just used for permission checking)
 - Destroying gates is restricted to users with the /stargatedestroy command permission
 - Creating gates is restricted to users with the /stargatecreate command permission
 - Using gates is restricted to users with the /stargateuse command permission
 - Viewing every hidden gate is restricted to users with the /stargatehidden command permission


Changes
=============
#### [Version 0.0.3.1] UNIFIED LEGACY ESR -- b1.1 - 1.0
 - Backported this plugin to hmod 133 (b1.1)
 - Added basic gradle support, fixed some modern issues (i.e. missing dependencies, etc).
 - This branch will now receive ABSOLUTELY MINIMAL MAINTENANCE.
[Version 0.0.2.4] THERAPH FORK
 - Fixed an expected block value to be compatible with b1.3+
[Version 0.0.2.3] DRAKIA FORK
 - You can now right click on the button to activate a gate, bypasses spawn protect issues.
[Version 0.0.2.2] DRAKIA FORK
 - The 4th line is now a config line for per-gate options.
 - Re-added ability to have always-on gates, use the 'A' option to enable.
[Version 0.0.2.1] DRAKIA FORK
 - Implemented hidden gates, great way for creating hidden rooms, etc.
 - Fixed gates are now not always-on. When created they will have a button to enable them. They do not open the destination gate.
 - Destination signs are reloaded if a different user tries to toggle them or open the gate.
[Version 0.0.2.0]
 - Improved save management
 - Fixed economy issues
 - Improved teleportation handling and consistency
 - Updated to hmod 132 and added new sign management
[Verson 0.0.1.5]
 - Added basic protection for portals
 - Portals now retain momentum
 - Fixed more general issues
[Version 0.0.1.4]
 - Added iConomy support
 - Added support for custom gate layouts
 - Added the .gate format
 - Improved config file
 - Added more config settings (including "owner")
 - Fixed an assortment of potential crashes
[Version 0.0.1.3]
 - Added gate networks
 - Code cleanup
 - Sign formatting improvements
 - REsolved some potential issues
[Version 0.0.1.2]
 - Fixed a more exceptions
 - Updated to hmod 125
 - Improved general stability
[Version 0.0.1.1]
 - Added permissions
 - Fixed a bunch of exceptions
[Version 0.0.1.0]
 - Added basic portal logic, layout
 - Added basic gate detection, behaviour
 - Added the ability to cycle through active gates
 - Added basic config and portal memory