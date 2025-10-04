# has item

**Requirement type**
<br>`has item`

**Description**
<br>Checks if the player has the specified item in their inventory.

## Syntax
```yaml
type: has item

# Sets the material of the item to check for.
material: MATERIAL

# Sets the display name the item must have.
display-name: "TEXT"

# Sets the lore lines the item must have.
# This can also be a single string: lore: "TEXT"
lore:
- "TEXT"

# Sets the amount of the item required.
amount: #

# Represents the CustomModelData the item should have.
model-data: #

# If set to true, also checks the player's armor slots for the item.
armor: BOOLEAN

# If set to true, also checks the player's off hand for the item.
off-hand: BOOLEAN
```

## Useful links
- [Materials](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)

## Examples

### Checks if the player has a wooden sword in their inventory
```yaml
requirements:
 - type: has item
   material: WOODEN_SWORD
```

### Checks if the player has at least 3 diamonds named "Quest Gem"
```yaml
requirements:
 - type: has item
   material: DIAMOND
   display-name: "Quest Gem"
   amount: 3
```

### Checks if the player is wearing golden boots in their armor slots
```yaml
requirements:
 - type: has item
   material: GOLDEN_BOOTS
   armor: true
```
