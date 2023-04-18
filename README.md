# qr-inventory
- Inventory System for QR-Core

## Features
- Stashes (Personal and/or Shared)
- Inventory Hotbar
- Shops
- Item Drops

## Dependencies
- [qr-core](https://github.com/QRCore-RedM-Re/qr-core)
- [qr-smallresources](https://github.com/QRCore-RedM-Re/qr-smallresources) - Logging item transfers and other interactions
- [qr-shops](https://github.com/QRCore-RedM-Re/qr-shops) - Create shops

## Screenshots
![image](https://user-images.githubusercontent.com/101474430/232665287-27e6f830-58c4-4c66-9e06-6dc3a38de874.png)
![image](https://user-images.githubusercontent.com/101474430/232665345-c4d96270-a6bf-4068-b20c-344d9b03a7ea.png)
![image](https://user-images.githubusercontent.com/101474430/232665512-9484ce52-2389-4c27-85ca-934c83fe3c80.png)

## Installation
- Download the script and put it in the `[qr]` directory.
- Import `qr-inventory.sql` in your database
- Add the following code to your server.cfg/resouces.cfg

```
ensure qr-core
ensure qr-smallresources
ensure qr-inventory
ensure qr-shops
```

## Configuration
```
Config = {}

Config.UseTarget = GetConvar('UseTarget', 'false') == 'true' -- Use qr-target interactions (don't change this, go to your server.cfg and add `setr UseTarget true` to use this and just that from true to false or the other way around)

Config.MaxInventoryWeight = 120000 -- Max weight a player can carry (default 120kg, written in grams)
Config.MaxInventorySlots = 41 -- Max inventory slots for a player

Config.CleanupDropTime = 15 * 60 -- How many seconds it takes for drops to be untouched before being deleted
Config.MaxDropViewDistance = 12.5 -- The distance in GTA Units that a drop can be seen
Config.UseItemDrop = false -- This will enable item object to spawn on drops instead of markers
Config.ItemDropObject = `p_bag_leather_doctor` -- if Config.UseItemDrop is true, this will be the prop that spawns for the item
```
