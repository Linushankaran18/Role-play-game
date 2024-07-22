# Role-play-game

The game "Dragon Repeller" is a simple text-based RPG (Role-Playing Game) implemented using HTML, CSS, and JavaScript. The player interacts with the game using buttons to make decisions, such as fighting monsters, buying items, or exploring different locations. Here's a breakdown of how the game works:

### HTML Structure
- **Stats Display**: Shows the player's XP, health, and gold.
- **Controls**: Contains buttons for different actions the player can take.
- **Monster Stats**: Displays the current monster's name and health when in a fight.
- **Text Area**: Provides narrative text and updates based on player actions.

### JavaScript Logic
#### Variables and Constants
- **Player Stats**: `xp`, `health`, `gold`, `currentWeapon`, `fighting`, `monsterHealth`, `inventory`.
- **DOM Elements**: References to buttons, text areas, and stat displays.
- **Weapons and Monsters**: Arrays of weapon and monster objects with properties like name, power, level, and health.
- **Locations**: Array of location objects with properties for button texts, button functions, and descriptive text.

#### Initial Setup
- Event listeners are added to buttons to call functions like `goStore`, `goCave`, and `fightDragon`.

#### Functions
- **update(location)**: Updates the button texts and functions based on the current location.
- **goTown()**: Updates the display to the town square.
- **goStore()**: Updates the display to the store.
- **goCave()**: Updates the display to the cave.
- **buyHealth()**: Allows the player to buy health if they have enough gold.
- **buyWeapon()**: Allows the player to buy a weapon if they have enough gold and updates their inventory.
- **sellWeapon()**: Allows the player to sell a weapon for gold.
- **fightSlime(), fightBeast(), fightDragon()**: Sets the current monster to fight and calls `goFight()`.
- **goFight()**: Updates the display for a fight with the selected monster.
- **attack()**: Handles the attack sequence, including calculating damage and updating health.
- **getMonsterAttackValue(level)**: Calculates the attack value of a monster based on its level.
- **isMonsterHit()**: Determines if the player hits the monster.
- **dodge()**: Allows the player to dodge an attack.
- **defeatMonster()**: Updates stats and transitions to the monster defeat screen.
- **lose()**: Transitions to the lose screen.
- **winGame()**: Transitions to the win screen.
- **restart()**: Resets the game to the initial state.
- **easterEgg()**: Transitions to the easter egg screen.
- **pickTwo(), pickEight()**: Functions for the easter egg game, where the player picks a number and sees if it matches randomly generated numbers.

#### Game Flow
1. **Start**: The player begins in the town square.
2. **Navigation**: The player can go to the store, cave, or fight the dragon using buttons.
3. **Store**: The player can buy health or weapons or sell weapons.
4. **Cave**: The player can choose to fight different monsters (slime or fanged beast).
5. **Fight**: The player fights a selected monster, attacking, dodging, or running.
6. **Winning and Losing**: The player wins by defeating the dragon or loses if their health reaches zero.
7. **Easter Egg**: A hidden game accessed after defeating a monster, where the player picks a number and wins gold or loses health based on random outcomes.

The game combines simple mechanics with a narrative to create an engaging experience where the player makes strategic decisions to defeat the dragon and save the town.
