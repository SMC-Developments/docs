# Items
Items are the core elements of a GUI menu.  
They define how each slot in the menu looks, behaves, and reacts when clicked.

### Syntax
```yaml
items:
  item-id:
    material: TEXT
    slot: #
```
> [!NOTE]
> Always use a unique item-id to prevent conflicts.

### material
```yaml
material: TEXT
```
> *Supported values:*  
> - [Material name](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html) (`DIRT`)  
> - Minecraft texture (`PLAYER_HEAD:http://textures.minecraft.net/texture/<id>`)  
> - Player head (`head-notch`)  
> - Placeholder head (`head-%player_name%`)

Sets the material of the item.  

### display name
```yaml
display-name: "TEXT"
```
Sets the item’s display name.
<br>Supports placeholders and color/format codes.

### lore
```yaml
lore:
 - "TEXT"
 - "TEXT"
```
> *Wrapped lore lines:*
> ```yaml
> lore:
>  - text: "TEXT"
>    wrap: true
> ```
> Lore lines can optionally be wrapped across multiple rows if the text is too long to fit on a single line.
> <br>The wrap width can be set in the Core's config file.

Sets the item’s lore (the text shown under the item’s name). 
<br>Supports placeholders and color/format codes.

### slot
```yaml
slot: #
```
> *Multiple slots:*
> ```yaml
> slots:
>  - #
>  - #
>  - #
> # OR
>  - #-#
>  - #-#
> ```

<img src="https://github.com/VinceSMC/SMC-Developments/blob/2340e4f55e1d40989c508a8ca77ba1a6cb528394/images/slots.png" alt="Logo" width="auto" height="325">
Sets the slot where the item should be placed in the menu.

### amount
```yaml
amount: #
```
Sets the item’s amount in the GUI menu.

### glow
```yaml
glow: BOOLEAN
```
If set to true, gives the item the enchantment glow effect. Some items cannot glow.

### model data
```yaml
model-data: #
```
Sets a CustomModelData value for the item (e.g. `model-data: 14`).

### enchantments
```yaml
enchantments:
 - "ENCHANTMENT-ID;LEVEL"
 - "ENCHANTMENT-ID;LEVEL"
```
> *Available enchantments:* [Enchantments list](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/enchantments/Enchantment.html)

Adds enchantments to the item (e.g. `SHARPNESS;3`).

### item flags
```yaml
item-flags:
 - ITEM-FLAG
 - ITEM-FLAG
```
> *Available flags:* [Item Flags list](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/ItemFlag.html)

Sets item flags for the item (e.g. `HIDE_ATTRIBUTES`).

### potion effects
```yaml
potion-effects:
 - POTION-TYPE;DURATION;AMPLIFIER
 - POTION-TYPE;DURATION;AMPLIFIER
```
> *Available effects:* [Potion Effects list](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionEffectType.html)

Adds potion effects to the item.
<br>Only applies if the [material](items.md#material) is `POTION`, `SPLASH_POTION`, or `TIPPED_ARROW`.  

### hex
```yaml
hex: "#000000"
```
Sets the HEX color for leather armor, potions, splash potions, tipped arrows, and firework stars.

### hide tooltip
```yaml
hide-tooltip: BOOLEAN
```
If set to true, hides the vanilla attributes tooltip of the item. Only supported on Minecraft 1.20.5 and above.

### priority
```yaml
priority: #
```
Sets the item’s priority number.
<br>If multiple items want the same slot, the one with the highest priority is checked first. If its view-conditions are met, it is displayed; otherwise the plugin evaluates the next item in line. The highest priority is `0`.

### click actions
```yaml
left-click-actions: ACTIONS
shift-left-click-actions: ACTIONS
right-click-actions: ACTIONS
shift-right-click-actions: ACTIONS
click-actions: ACTIONS
```
Sets the actions to run when the item is clicked.
<br>Actions execute from top to bottom in the list.
<br>Check the [Actions](https://github.com/VinceSMC/SMC-Developments/blob/f5a97c218bf83512aa6d5232cb35e18444c6d88d/documentation/actions.md) section for more information.

### view conditions
```yaml
view-conditions: CONDITIONS
```
Sets the conditions a player must meet to see the item.
<br>Check the [Conditions](https://github.com/VinceSMC/SMC-Developments/blob/main/documentation/conditions.md) section for more information.

### type
```yaml
type: TEXT
```
> *Global types:*
> - `FILLER` — functions as a filler item, populating all empty slots in the menu.

Sets the item’s type. Item types attach special functions or behavior to an item.
<br>Each plugin may also add its own unique item types.
<br>Check the plugin’s documentation for supported values.





















