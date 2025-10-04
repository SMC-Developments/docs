# chance

**Action tag**  
`@chance`

**Description**
<br>Runs the action based on a chance value between 0 (never) and 100 (always).

## Examples

### 50% chance to give the player a diamond
```yaml
actions:
 - "[giveitem] DIAMOND;1@chance=50"
```

### Picking a random message with weighted chances
```yaml
actions:
 - "[message] Going to select a random message based on chance..."
 - "[delay] 100"
 - "[message] Group 1 - Message 1 (Chance 50%)@group=group-1@chance=50"
 - "[message] Group 1 - Message 2 (Chance 25%)@group=group-1@chance=25"
 - "[message] Group 1 - Message 3 (Chance 1%)@group=group-1@chance=1"
```
> When actions share the same @group, only one will be executed.
<br>The @chance tag controls how likely each one is to be picked.
<br>If no @chance values are set, each action in the group has an equal chance.

### Weighted rewards with follow-up actions
```yaml
actions:
 - "[message] &bRolling for a random reward..."
 - "[delay] 100"

 # Weighted random selection
 - "[message] &aYou won 10 coins!@group=reward@chance=50@trigger=reward-10"
 - "[message] &aYou won 25 coins!@group=reward@chance=25@trigger=reward-25"
 - "[message] &6Jackpot! You won 1000 coins!@group=reward@chance=1@trigger=reward-1000"

 # Follow-up actions for each reward
 - "[currency] give coins 10@trigger-id=reward-10"
 - "[currency] give coins 25@trigger-id=reward-25"
 - "[currency] give coins 1000@trigger-id=reward-1000"
```



