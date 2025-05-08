# Lua Patcher
Designed specifically for Garry's Mod and Balatro, this addon / mod stops the most common Lua errors from resolving, but has the potential to cause performance issues. Maybe try to only use this as a last resort. 

*CAUTION: Never trigger an ***intentional*** crash while this addon/mod is enabled. That's like pitting an unstoppable force versus an immovable object, anything could happen and it'll be your fault!*

# How do?
To install, decompress this archive and drop the resulting folder into `GarrysMod/garrysmod/addons` for Garry's Mod, or `Balatro/Mods` for Balatro. Check that `addon.json` resides in `GarrysMod/garrysmod/addons/lua_patcher/addon.json` or `Balatro/Mods/lua_patcher/addon.json` after the move.

Discussion of this addon is held in the [Steam Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=2403043112) for Garry's Mod, while for Balatro they are held in Discord in the [official Balatro server](https://discord.com/channels/1116389027176787968/1370113335659593898/1370113335659593898) and the [Steamodded server](https://discord.com/channels/1334988047229653042/1362508338352357556/1362508338352357556).

**For Garry's Mod Players: This addon and other Garry's Mod-specific information pertaining to this addon is on the [Garry's Mod Steam Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=2403043112).**

# What does this do?
This mod attempts to redefine Lua rules to prevent Lua errors from showing up. It does this by having certain Lua operations return an appropriate value instead of throwing an error.

You can think of this mod as providing a new set of rules to the interpreter on how to deal with certain Lua errors before they even happen. As a plus, this sometimes allows broken mods to become functional again!

# What can't this fix?
This does not fix other non-Lua errors, only compiled Lua code. The script files themselves must not have any syntax errors or they won't compile and will be invisible to this. I can't do anything to fix these, sorry.

Lua Patcher also cannot deal with errors that contain the phrase "attempt to compare X with number" or "attempt to compare X with string" due to how number and string comparisons are implemented in Lua 5.1. If __lt and __le metamethods are invoked for mixed types one day, this error will become fixed.

Other than the above, there will exist a way for Lua Patcher to deal with the error.

# I still see Lua problems after installing this.
Sadly, each illegal Lua operation must be redefined one by one. If this happens, give me the error message as well as which mod did it so that I can see what operation Lua was trying to do.

Note that if you don't give me enough information about the error, I might not be able to fix it!
