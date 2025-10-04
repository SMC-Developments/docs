## Actions
Actions are the core system used to make things happen on your server.
<br>They let you send messages, play sounds, launch players, run commands, spawn particles, give rewards, and much more. Every action follows a unified syntax, so you can mix and chain them together to create anything from a single chat message to complex interactive sequences.

### Action types

| #  | Type        | Args                                                           | Description                                                                 |
|----|-------------|----------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1  | [`[message]`](action-types/message.md) | `<text>` | Sends a chat message to the player. |
| 2  | `[player]` | `<command>` | Executes a command as the player. |
| 3  | `[console]` | `<command>` | Executes a command from the console. |
| 4  | [`[item]`](action-types/item.md) | `<action> <material> <amount>` | Gives or takes a specified item from a player. |
| 5  | [`[exp]`](action-types/exp.md) | `[exp] <action> <amount>;[options]` | Gives or takes experience from a player. |
| 6  | [`[sound]`](action-types/sound.md) | `<sound> <volume> <pitch>` | Plays a sound effect for the player. |
| 7  | [`[firework]`](action-types/firework.md) | `<type> <power> <y-offset> <color1>,<color2>,<color3>...` | Launches a firework effect at the player’s location. |
| 8 | [`[teleport]`](action-types/teleport.md) | `<world> <x> <y> <z> <yaw> <pitch>` | Teleports the player to a specific location in a given world. |
| 9 | [`[title]`](action-types/title.md) | `<fade-in> <stay-time> <fade-out> <title>;[subtitle]` | Displays a title and subtitle on the player’s screen. |
| 10 | [`[particle]`](action-types/particle.md) | `<particle> <amount> <offset-x> <offset-y> <offset-z> <speed> <visible-all>` | Displays a particle effect at the player’s location. |
| 11 | [`[bossbar]`](action-types/bossbar.md) | `<style> <progress> <color> <duration> <text>` | Displays a temporary bossbar message at the top of the player’s screen. |
| 12 | [`*[toast]`](action-types/toast.md) | `<icon> <frame> <header>;[footer]` | Displays a toast popup notification (like the advancement popups). |
| 13| [`[hologram]`](action-types/hologram.md) | `<mode> <duration> <y> <text>` | Displays a temporary hologram in front of the player. Supports three modes.|
| 14 | [`[summon]`](action-types/summon.md) | `<mob> <amount> <radius> [display-name]` | Summons one or more mobs near the player. |
| 15 | [`[launch]`](action-types/launch.md) | `<mode> <arg1> <arg2> <arg3>;[options]` | Launches the player by applying a velocity. |
| 16  | [`[currency]`](action-types/currency.md) | `<action> <currency> <amount>` | Gives or takes a certain amount of a currency from a player. |
| 17 | [`[effect]`](action-types/effect.md)    | `<type> <amplifier> <duration>` | Applies a potion effect to the player. |
| 18 | [`[actionbar]`](action-types/actionbar.md) | `<duration> <text>` | Sends a message to the player’s actionbar (the text area above the hotbar). |
| 19 | `[delay]` | `<duration>` | Executes the action after the specified delay (in ticks, 20 ticks = 1 second). |
| 20 | `[close]` | | Closes the currently opened GUI menu. |

### Action tags
Action tags extend the behavior of actions with extra features.
<br>They let you control how and when actions run, for example `- "[message] Hello World!@broadcast"`.

| #  | Tag          | Description |
|----|-------------|-------------|
| 1  | [`@broadcast`](action-tags/broadcast.md) | Sends the action to all players currently online on the server. |
| 2  | [`@chance`](action-tags/chance.md) | Runs the action based on a chance value between 0 (never) and 100 (always). |
| 3  | [`@group`](action-tags/group.md) | Lets you group multiple actions. When the group runs, only one action from it will be chosen at random. |
| 4  | [`@condition`](action-tags/condition.md) | Adds one or more requirements that must be met before the action can run. |
| 5  | [`@trigger`](action-tags/trigger.md) | Allows one action to trigger another. You can connect actions this way to build sequences or chain follow-up actions. |
| 6  | [`@cooldown`](action-tags/cooldown.md) | Adds a cooldown to the action. This limits how often it can be triggered within a set time. |
| 7  | [`@centered`](action-tags/centered.md) | Centers the text of a message action in chat. This tag only works with the `[message]` action type. |










