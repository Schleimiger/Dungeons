# Dungeons Plugin

A comprehensive Minecraft plugin that creates an advanced dungeon system with multiple areas, boss fights, and reward systems.

## Features

- **Multi-area dungeons** with increasing difficulty
- **Economy integration** using Vault
- **Configurable dungeon parameters**
- **GUI-based dungeon selection**
- **Admin setup GUI** for easy configuration
- **Boss fights** with mini-bosses and final bosses
- **Reward system** with configurable loot
- **Multi-player support** (up to 4 players per dungeon)
- **Comprehensive logging** for all dungeon activities

## Commands

- `/dungeons` - Teleport to dungeon spawn world
- `/dungeons reload` - Reload plugin configuration (admin only)
- `/dungeoncreate <player>` - Open dungeon selection GUI for player (console only)
- `/dungeonsadmin setup` - Open admin setup GUI for dungeon configuration

## Permissions

- `dungeons.use` - Allows using the dungeons command (default: true)
- `dungeons.admin.reload` - Allows reloading the plugin (default: op)
- `dungeons.admin.setup` - Allows using the dungeon setup GUI (default: op)

## Requirements

- **Bukkit/Spigot/Paper** 1.16.5 or higher
- **Vault** plugin for economy integration
- **Economy plugin** (like EssentialsX) for money handling

## Worlds Required

- `dungeonspawn` - Main lobby world
- `dre1` - Dungeon world where battles take place
- `rewards` - Optional reward room world

## Configuration Files

All configuration files are automatically created in `plugins/Dungeons/` when the plugin first runs:

### config.yml
- Plugin prefix and world settings
- Maximum players per dungeon
- Teleport delays and timeouts

### lang.yml
- All plugin messages
- Fully customizable language support
- Admin setup messages

### dungeons.yml
- Define available dungeons
- Set prices, kill goals, and boss health
- Create new dungeon types easily

### rewards.yml
- Configure rewards for each dungeon
- Set different reward tiers
- Customize loot for different difficulty levels

## Admin Setup GUI

Use `/dungeonsadmin setup` to access the comprehensive setup interface:

- **Create New Dungeon** - Add new dungeon configurations
- **Edit Existing Dungeon** - Modify current dungeons
- **Dungeon Size Settings** - Configure area dimensions
- **Mob Configuration** - Set mob types and spawn rates
- **Boss Settings** - Configure mini and final bosses
- **Reward Configuration** - Set up loot tables
- **Economy Settings** - Adjust pricing
- **World Settings** - Configure world names and locations

## How It Works

1. Players use `/dungeons` to teleport to the spawn world
2. Admins use `/dungeoncreate <player>` to open the dungeon selection GUI
3. Players select a dungeon and pay the required fee
4. Players are teleported to the dungeon world and progress through:
   - **Area 1**: Kill monsters to reach kill goal
   - **Mini Boss**: Defeat to unlock Area 2
   - **Area 2**: Kill stronger monsters for second kill goal
   - **Final Boss**: Ultimate challenge
   - **Reward Room**: Collect rewards if successful

## Installation

1. Download the plugin JAR file
2. Place it in your server's `plugins` folder
3. Install Vault and an economy plugin
4. Create the required worlds: `dungeonspawn`, `dre1`, and optionally `rewards`
5. Restart your server
6. Configuration files will be automatically created in `plugins/Dungeons/`
7. Use `/dungeonsadmin setup` to configure your dungeons

## Building from Source

```bash
mvn clean package
```

The compiled JAR will be in the `target` directory.

## Support

For support, please check the configuration files in `plugins/Dungeons/` and console logs for any error messages. All dungeon activities are logged for debugging purposes.