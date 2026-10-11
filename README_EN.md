# More Armors (Laoqi update, v2.6)

**English** ｜ [简体中文](README.md)

> A rework of **More Armors v2.2 (Nether Update)** by **Drag504**

![More Armors](images/cover.png)

> Cover art: the original More Armors artwork (by Drag504)

A Minecraft Bedrock add-on that adds **36 armour sets — 144 pieces in total**. The original mod by Drag504 has not been maintained for years and no longer works on current Bedrock builds — **install it and not a single piece of armour ever shows up**. v2.6 fixes it and brings it up to date.

**Download**: grab [`More Armors.mcaddon`](More%20Armors.mcaddon) from this repository (one file, done), or the separate [`MoreArmorsBP.mcpack`](MoreArmorsBP.mcpack) / [`MoreArmorsRP.mcpack`](MoreArmorsRP.mcpack). See "Installation" below.

---

## A dad's little story

My 5-year-old son saw this mod in a video and wanted it.

I spent ages on it: the packs installed, but not a single piece of armour ever showed up in the game — the add-on did nothing at all. I was getting seriously frustrated.

In the end I used **deepseek v4 flash high** together with codex — it took two hours to track down and fix everything (item format, armour values, icons, recipes, bilingual names …) and cost me a grand total of 2.6 CNY.

This update is for my lovely son, and for every Minecraft fan out there. Enjoy!

---

## What this update does

- **Makes the whole set usable again**: on current Bedrock the original did nothing at all — its item data format is obsolete, so none of the 144 pieces ever appeared
- **Item, armour, enchantment and recipe data rewritten in the new format**
- **Two fatal fields fixed**: chestplates declared an illegal enchantment slot (`armor_chest`), which made the game drop the whole item; the old icon syntax renders as a blank icon
- **Armour rendering**: fixed (the old geometry names no longer exist)
- **Set bonus fix**: the "wear all four pieces" check for Diamond Block / Netherite Block was buggy (it only ever checked the boots); it now really requires the full set
- **English + Simplified Chinese names**: switch automatically with the game language; sets that share a material with vanilla armour (iron / gold / diamond / netherite) are marked **`[MOD]` / 【模组】** so they are easy to tell apart
- **Credits simplified**: the original author is credited as "a rework of Drag504's More Armors v2.2"; this update is by **Laoqi**

## What's inside

36 sets × 4 pieces (helmet / chestplate / leggings / boots) = **144 items**, following the original mod's recipe style (crafted from the material itself or its block):

| Category | Sets |
|---|---|
| Wood | Oak, Spruce, Birch, Jungle, Acacia, Dark Oak, Crimson, Warped |
| Stone | Stone, Cobblestone, Stonebrick, Andesite, Diorite, Granite, Gravel, Dirt, Brick |
| Mineral | Coal, Coal Block, Charcoal, Iron Block, Gold Block, Diamond Block, Emerald, Emerald Block, Lapis Lazuli, Lapis Block, Redstone, Redstone Block, Quartz |
| Nether | Basalt, Blackstone, Obsidian, Crying Obsidian, Netherrack, Netherite Block |

**Diamond Block** and **Netherite Block** are the top-tier sets: wearing all four pieces grants Resistance / Regeneration / Strength (plus more Strength while holding the matching sword), and Netherite Block also grants Fire Resistance. Stat-wise the *Block* sets are generally stronger and more durable than the vanilla armour of the same material.

![Preview](images/cover.png)

## Installation

**Requires**: Minecraft Bedrock **1.21 or newer** (tested on the current release)

**Option 1 (recommended)**: double-click `More Armors.mcaddon`; the game imports it automatically.

**Option 2 (manual — use this if double-clicking does nothing)**:

1. Rename `More Armors.mcaddon` to `.zip` and extract it — you get the folders `More Armors BP` and `More Armors RP`;
2. Open the `com.mojang` folder (use whichever path exists):
   - Minecraft Launcher / GDK build: `%APPDATA%\Minecraft Bedrock\Users\Shared\games\com.mojang`
   - Store build: `%LOCALAPPDATA%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang`

   (search your PC for the `minecraftWorlds` folder — its parent is `com.mojang`)
3. Copy `More Armors BP` into `behavior_packs\` and `More Armors RP` into `resource_packs\`;
4. Restart the game → Edit World → Behavior Packs / Resource Packs → My Packs → enable **More Armors**.

You can also install the two packs separately: `MoreArmorsBP.mcpack` and `MoreArmorsRP.mcpack`.

**Existing worlds keep working**: this version reuses the original namespace and UUIDs, so importing it replaces the old pack in place and items you already own in a world will not be lost.

## Usage notes (important)

- **Enable it inside a world**: Edit World → Behavior Packs / Resource Packs → My Packs → tick **More Armors**.
  ⚠️ **Do not enable it on its own from the global "My Packs" list on the main menu**: the behaviour pack and the resource pack **depend on each other** (BP ↔ RP), so enabling just one globally keeps reporting a missing dependency and looks broken. Enabling both inside a world works with no error.
- **Experimental gameplay**: the original author asked for the world's experimental toggle (Holiday Creator Features) to be on. In 1.21+ custom items are a stable feature and it should no longer be necessary, but we have not verified that piece by piece — if items do not show up after enabling, check whether your world settings still have an experimental toggle and turn it on (newer versions may have removed it entirely; if you cannot find it, it is not needed).
- After enabling the packs, **leave and re-enter the world** once so items and textures reload.
- The author does not actually play the game (this update was made for his son), so the notes above come from real trial and error — please report anything that behaves differently.

## Languages

Names follow the game language: Simplified Chinese shows 「铁块头盔」/「钻石块胸甲」, English shows `[MOD] Iron Block Helmet` and so on. The four sets that share a material with vanilla armour (Iron Block / Gold Block / Diamond Block / Netherite Block) carry the **`[MOD]` / 【模组】** marker.

## Known limitations

- Bedrock does **not** currently expose "armour toughness" or "knockback resistance" to custom armour (vanilla diamond and netherite armour have those hard-coded), so custom armour cannot have them. This pack compensates with higher armour values and set bonuses.
- The author mainly verified things in Creative mode; the survival flow (crafting table, anvil repair, enchanting table) has not been checked piece by piece — feedback is welcome.

## Credits & sharing

- Original mod: **More Armors v2.2 (Nether Update)** by **Drag504** — thanks to the original author for the work
- Current-version port and update: **Laoqi** (using **deepseek v4 flash high** together with codex)
- **License**: released under the **MIT** license (see [LICENSE](LICENSE)). The original More Armors mod and its artwork remain the property of Drag504.
- When reposting, please keep the original author's credit and this update's credit

Have fun, and feel free to report anything you run into.

---

**中文说明**: [README.md](README.md)
