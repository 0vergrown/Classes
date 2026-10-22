# Origins: Classes (data pack)

A data pack version of Apace's *Origins: Classes* mod, rebuilt on Overgrown's Apoli and Origins. It adds a second layer, **Class**, next to the origin layer. You pick one of 14 classes, and each class grants two small perks.

The ids are the same as the mod's (`origins-classes:class`, `origins-classes:rogue`, `origins-classes:sneaky` and so on), so the translation files and any commands written for the mod keep working.

## Requirements

| | Version |
| --- | --- |
| Minecraft | 1.20.1 or 1.21.1 |
| Loader | Fabric (1.20.1, 1.21.1) or NeoForge (1.21.1) |
| Apoli | 1.119.0 or newer |
| Origins | 1.47.12 or newer |

## Installing

The folder is both a data pack and a resource pack.

1. Put it (or a zip of it) in the world's `datapacks` folder.
2. Put the same folder in `resourcepacks` and enable it. This loads the class and power names, the descriptions and the Stealth effect icon. Without it, players see raw translation keys.

## The classes

| Class | Power | Status |
| --- | --- | --- |
| Archer | Accuracy (`no_projectile_divergence`) | Works |
| | Agility (`less_bow_slowdown`) | Works |
| Beastmaster | Fauna Friends (`tamed_animal_boost`) | Works |
| | Effective Empathy (`tamed_potion_diffusal`) | Works |
| Blacksmith | High-Quality Equipment (`quality_equipment`) | Works |
| | Efficient Repairs (`efficient_repairs`) | Works, see notes |
| Cleric | Extended Potions (`longer_potions`) | Works, see notes |
| | Enchantment Mastery (`better_enchanting`) | Works |
| Cook | Good Meals (`better_crafted_food`) | Works |
| | Smoking (`more_smoker_xp`) | Works |
| Explorer | Explorer Kit (`explorer_kit`) | Works |
| | Fit (`no_sprint_exhaustion`) | Works |
| Farmer | Bountiful Harvest (`more_crop_drops`) | Works |
| | Fertilizing Techniques (`better_bone_meal`) | Works |
| Lumberjack | Timber! (`tree_felling`) | Works |
| | Woodcutting (`more_planks_from_logs`) | Works |
| Merchant | Restocking (`trade_availability`) | Works |
| | Charisma (`rare_wandering_loot`) | Works |
| Miner | Mining Expert (`more_stone_break_speed`) | Works |
| | Experienced Excavator (`no_mining_exhaustion`) | Works |
| Nitwit | none | Works |
| Rancher | Twin Births (`twin_breeding`) | Works |
| | Scavenging (`more_animal_loot`) | Works |
| Rogue | Sneaky (`sneaky`) | Works |
| | In the Shadows (`stealth`) and Stealth (`stealth_descriptor`) | Works, see notes |
| Warrior | Weapon Knowledge (`more_attack_damage`) | Works |
| | Shield Wield (`less_shield_slowdown`) | Works |

## How the working powers behave

- **Accuracy**: arrows, tridents, snowballs, eggs, ender pearls and thrown potions fly exactly where the Archer aims.
- **Agility, Shield Wield**: drawing a bow or raising a shield slows you to 60% instead of 20%. Items in the `#origins-classes:bows` and `#origins-classes:shields` tags count, which include the vanilla items and the common `c:` tags for modded ones.
- **High-Quality Equipment**: crafted armor gets +0.25 armor toughness, swords, bows and crossbows +0.5 attack damage, shields +1 knockback resistance (shown as the vanilla tooltip shows it) and pickaxes, axes, shovels and hoes mine 5% faster on blocks they are made for. Dyeing leather armor or decorating a shield doesn't count as crafting new equipment. Repairing two items in the crafting grid gives the result the bonus, as in the mod.
- **Efficient Repairs**: combining two damaged items in the crafting grid restores 15% bonus durability instead of 5%, to the exact point the mod gave. In an anvil, each piece of repair material restores half of the item's durability instead of a quarter, and combining two items adds 144% of the maximum durability, which always repairs the result fully.
- **Fauna Friends**: animals the Beastmaster tames get 30% more maximum health and 1.5 more attack damage for good. That covers wolves, cats and parrots tamed with food, horses, donkeys, mules and llamas broken in by riding, and the puppies, kittens and foals the Beastmaster breeds.
- **Effective Empathy**: when the Beastmaster gains a status effect, from a potion or anything else except a beacon or conduit, their tamed wolves, cats and parrots within 8 blocks (2 up or down) get a copy.
- **Enchantment Mastery**: items the Cleric enchants at an enchanting table count as 10 points more enchantable, for better enchantments at the same level cost.
- **Smoking**: cooking in a smoker gives the Cook twice the experience when they take the food out.
- **Extended Potions**: use a potion, splash potion or lingering potion with effects on a water cauldron. The cauldron loses one level, and the potion keeps its name, gets an "Extended" line and lasts twice as long. Instant effects keep their duration. A potion can only be extended once.
- **Good Meals**: food crafted by a Cook carries a "Nourishment: +N" line. Whoever eats it, Cook or not, gets N extra hunger and the matching saturation one tick after eating. N is a third of the food's hunger, rounded up (at least 1). The tiers are the `#origins-classes:cook/nourishment_2`, `_3` and `_4` item tags, and any other food gets 1.
- **Fit**: sprinting on the ground costs no hunger. Sprint-jumping, attacking and mining still do.
- **Bountiful Harvest**: wheat, carrots, potatoes, beetroots, torchflower crops and melons have a 30% chance to drop their loot twice.
- **Fertilizing Techniques**: bone meal works twice on crops and plants. The second growth lands one tick after the first.
- **Woodcutting**: any recipe that makes planks makes 2 more.
- **Timber!**: chopping a log with an axe, without sneaking, also chops every log of the same kind joined to it sideways and upward, up to 256, as long as the tree touches natural leaves somewhere. Log cabins stay standing. Each log costs the axe durability and the felling stops if the axe breaks. A whole tree takes as long as three quarters of its logs would one by one.
- **Restocking**: villagers never run out of stock for the Merchant. Wandering traders still sell out.
- **Charisma**: every wandering trader offers the Merchant two extra one-time trades: a random item for 6 to 17 emeralds, and a random item for 1 to 16 of another random item. Items that can be enchanted are enchanted half of the time. The trades are rolled once per trader and saved with it, and other players don't see them.
- **Mining Expert, Experienced Excavator**: pickaxe-mineable blocks break 45% faster with the right tool, and breaking blocks costs no hunger.
- **Scavenging**: animals you kill have a 30% chance to drop their loot twice.
- **Twin Births**: animals the Rancher breeds have a 20% chance of twins.
- **Sneaky**: you count as sneaking without crouching: your nameplate never shows through walls and only shows within 32 blocks, mobs notice you from 80% of the usual distance, foxes don't run from you, and walking makes no footstep sounds or vibrations.
- **In the Shadows and Stealth**: after 10 seconds of sneaking you get the Stealth effect. While it lasts, other players don't hear your sounds, the blocks you break crumble without sound or particles, and a melee hit on an enemy facing away deals your weapon's base damage a second time. Attacking, or letting go of sneak, ends it.
- **Weapon Knowledge**: +1 attack damage.

## Notes and known differences

- Tooltip lines the mod drew in code (Nourishment, Mining Speed, Extended) are item lore here, so they sit above the attribute section.
- The Blacksmith's bonuses come from a marker on the item, read by a power every player has. They don't show inside the vanilla "When in Main Hand" section, and mobs wearing the gear don't get them. In exchange they carry over to netherite gear upgraded in a smithing table.
- Extended Potions only knows the vanilla potions (38 on 1.20.1, 42 on 1.21.1). The mod could also double potions made with `/give` or by other mods. It also doesn't stop an extended potion from going into a brewing stand. On 1.20.1, brewing it into a splash or lingering potion loses its effects. On 1.21.1 the brewing stand leaves it unchanged and still uses up the ingredient.
- Accuracy also covers crossbows, which the mod left out.
- In the anvil, the mod only doubled the repair of the first piece of material, though its code calls the change halving the material cost. Here every piece repairs half.
- Charisma picks from the items in the vanilla loot tables (1001 on 1.20.1, 1075 on 1.21.1), minus the mod's blacklist. The mod built the list from every loot table loaded, so modded items could show up there and can't here.
- Twin Births works for every animal that gives birth. The mod only handled animals that breed through the older breeding goal, so axolotls, goats, camels and hoglins never had twins there.
- Fauna Friends boosts a baby when the Beastmaster breeds it. The mod boosted it when the parents belonged to a Beastmaster, whoever fed them. In practice that's usually the same player.
- Timber! decides whether you were sneaking when the log breaks, while the mod checked when you started hitting it.

## Layout

| Path | Contents |
| --- | --- |
| `data/origins-classes/origin_layers/`, `origins/` | The layer and the 14 classes |
| `data/origins-classes/powers/` | One file per power; `powers/global/` holds the two powers every player gets |
| `data/origins-classes/global_powers/players.json` | Grants those two powers to all players |
| `data/origins-classes/effects/stealth.json` | The Stealth status effect |
| `data/origins-classes/item_modifiers/`, `item_modifier/` | Item changes for crafting and potions (1.20.1 and 1.21.1 spellings) |
| `data/origins-classes/loot_tables/`, `loot_table/` | The double-loot tables, and the price and item tables for Charisma |
| `data/origins-classes/functions/`, `function/` | The Beastmaster boost, one copy for each version's `/attribute` syntax |
| `data/origins-classes/tags/items/`, `tags/item/` | Item tags |
| `assets/origins-classes/` | Translations and the Stealth icon |
