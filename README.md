# UEFN Tycoon Framework  
A modular tycoon-game framework for Unreal Engine for Fortnite (UEFN), written in Verse.
It covers the economy loop, per-player state, a battle pass, daily rewards, gift boxes and
UI, so you start from working systems instead of a blank project.

**12 Verse device scripts**, ready-made textures and UI assets, Apache-2.0.

## 🚀 Features
- Fully structured folder setup for tycoon gameplay: economy logic, GUI, assets.  
- Device scripts (.verse) for core gameplay: money collection, upgrades, player tracking, etc.  
- Asset folders: `BPTextures`, `DRTextures`, `GBTextures`, `UI` for organizing visual assets.  

## 📦 Folder Structure
```
/BPTextures           — Battlepass texture assets
/DRTextures           — Daily-reward textures
/GBTextures           — Gift-box textures
/UI                   — User interface assets (Permanently shown)
/Devicelist.verse     — Device registry script for registering all sorts of in-game devices dev might want to modify and use in Assets device (./tycoon_Assets_device.verse)
/HitBox_device.verse  — Makes a prop hittable by player to reward him with his current income per second on each hit
/NPC_Killer_device.verse — detects which player kills an NPC to reward him with the players income per second 
/battlepass_main_device.verse  — A Battlepass which levels up with progress made by the player to boost play time
/custom_car_device.verse — Planned device to make ingame cars with custom design purchasable by players
/custom_player.verse — A concrete class with attributes assigned
/daily_reward_device.verse — Keeps track of time to reward returning players daily and boost retention rate
/game_manager_device.verse — Manages mainly a hash-map where players are assigned to custom_player (./custom_player.verse)
/giftbox_device.verse — Reward for players play-time which keeps players engaged
/player_coin_ui_device.verse — Displays all players their (economy) stats on the screen left-side
/tycoon_Assets_device.verse — Connects in-game Assets to the system and manages an array which each tycoon asset is inside
/utils.verse           — Help functions to make framework work
README.md             — What you are reading right now
LICENSE               — Apache-2.0
```

## 🧠 Getting Started
1. Clone the repository:  
   ```bash
   git clone https://github.com/GorianSt/UEFN-Tycoon-framework.git
    ```
or download the .verse files from github and import them manually into UEFN

2. Open the project in UEFN.
3. Inspect the `tycoon_Assets_device.verse` device to understand how the framework wires economy, upgrades, and player interactions.
4. Customize:
   * Replace textures in the `/BPTextures`, `/DRTextures`, `/GBTextures` folders if wanted to.
   * Modify UI (shows player cash stats) images in `/UI`.
   * Add new device scripts by copying an existing `.verse` file and adjusting logic for your gameplay.
5. Build & test your tycoon flow: spawn devices, collect money, buy upgrades, see UI updates.

## 🛠 How to Extend

* **Add a new feature**: Create new (device) script → test & apply → place in level.
* **Add a new UI panel**: Duplicate existing UI asset → hook into the according UI device scripts and follow other UI assets calls.
* **Change economy numbers**: Locate the cost/earning variables in the Device `details panel` in UEFN or in the `.verse` files, tweak values.
* **Add custom player mechanics**: Use `custom_player.verse` as template and add function's needed to add mechanic.

## 🎓 Why use this framework?

* Saves dev time: no need to build core tycoon logic from scratch.
* Modular: everything is separated so you can swap or remove / comment out parts easily.
* Flexible: build any tycoon-style game (factory, farm, space station, city builder) with minimal base setup.
* Easy to understand: folder naming & device scripts are intuitive and ready for modification.

## ✅ Requirements

* [Unreal Engine for Fortnite (UEFN)](https://www.unrealengine.com/en-US/uses/uefn-unreal-editor-for-fortnite) (latest version recommended)
* Basic knowledge of Verse scripting and Fortnite Creative devices
* (Optional) Experience with Unreal Editor, asset management, UI design

## 📄 License

This project is licensed under the Apache License 2.0. See the [LICENSE](./LICENSE) file for details.

## 🧩 Contributing

Contributions are welcome!

* Fork the repo
* Create a new branch: `feature/your-feature`
* Submit a pull request with a clear description of your changes
* Follow the existing code style and add comments where necessary

## 📬 Contact

For questions or suggestions, open an issue in the repo or message me on GitHub.

---

Happy building — go create your next tycoon game!