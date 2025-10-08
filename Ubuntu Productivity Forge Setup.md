## Daily Working Output — *Ubuntu Productivity Forge Setup*

>2025-10-08  | Arles Zhang & GPT-5

### Theme

**High-Frequency Multi-Monitor Workflow & Window Management for AI Compiler and System Development**

**Install Forge for Multi-monitor support** Since the Pop OS repository isn't available for your Ubuntu version, let's install **Forge** - which is an excellent alternative and works great with GNOME 46. **Forge Key Features:**
> - Auto-tiling like Pop Shell
> - Keyboard shortcuts for window management
> - Workspace management
> - Multi-monitor support  

**what is gnome-shell-extension ? what is extension-manager ?**
- **App store** for GNOME extensions
- **Browse, install, enable/disable** extensions
- **No terminal commands needed**
The document include High-Frequency Multi-Monitor Shortcuts Guide.

### Context

Today’s focus: building a **zero-latency, keyboard-centric development environment** in Ubuntu to accelerate multitasking for:

* **Project 1** → AI Training Data Pipeline & Cleaning
* **Project 2** → AI Code Agent (MCP-based Intelligent Coding System)
* Future Research Direction → *MLIR + NPU + Distributed Compilation Optimization*

---

## Today’s Progress Summary

### 1. Environment Maintenance

* Learned and practiced `apt`, `snap`, and `flatpak` package management difference
* Explored command patterns:

  ```bash
  apt list --installed | grep code
  snap list | grep code
  flatpak list | grep code
  ```

  → now understand how to trace duplicate VS Code installations and identify package sources.

**Common Multi-Monitor Features Across Tools**:

| Feature                           | Pop Shell | GNOME        | Awesome          | i3wm          |
| --------------------------------- | --------- | ------------ | ---------------- | ------------- |
| **Display detection**             | Automatic | Automatic    | Automatic/Manual | Manual config |
| **Workspace per monitor**         | ✅         | Configurable | ✅                | ✅             |
| **Move windows between displays** | ✅         | ✅            | ✅                | ✅             |
| **Hotplugging support**           | Excellent | Excellent    | Good             | Good          |
| **Different resolutions**         | ✅         | ✅            | ✅                | ✅             |
All of these tools handle multiple displays well, but the **configuration effort** varies:
- **Easy**: Pop Shell, GNOME, Material Shell (mostly automatic)
- **Medium**: Awesome WM (some configuration needed)
- **Advanced**: i3wm, Hyprland (manual configuration for optimal setup)


### 2. System & Shell Enhancement

* Installed **GNOME Shell Extension Manager** to handle extensions visually:

  ```bash
  sudo apt install gnome-shell-extension-manager
  ```
* Discovered that `gnome-extensions-app` comes from `gnome-shell-extension-prefs`.
* Verified Pop Shell deprecated for Ubuntu 24.04+; switched to **Tiling Assistant** (modern replacement).

### 3. Tiling Workflow Configuration

Installed core tools:

```bash
sudo apt install gnome-shell-extension-tiling-assistant gnome-shell-extension-gtile
```

Set up **multi-monitor tiling system** with:

* **Super + ← / →** for window tiling
* **Super + Shift + ← / →** for moving windows across monitors
* **Super + 1 / 2 / 3** for workspace switching
* **Tiling Assistant + gTile** for advanced layouts
* Optional **Keyd** mapping:

  ```
  capslock = leftmeta
  ```

  → transforms Caps Lock into system-wide modifier for ultra-fast control.

### 4. Workflow Design

| Monitor      | Workspace   | Usage                                  |
| ------------ | ----------- | -------------------------------------- |
| Primary  | Workspace 1 | VS Code + Docs                         |
| Secondary | Workspace 2 | Terminal + BQ Shell + Logs             |
| Optional  | Workspace 3 | Browser + Research PDFs                |
| Virtual   | Workspace 4 | Background Tasks / Docker / Monitoring |

---

## Key Learnings

* `apt search` ≠ `apt list --installed` — former queries repository, latter shows local packages.
* GNOME’s native tiling is minimal; **Tiling Assistant + gTile** provides power equivalent to Pop Shell or i3 but easier to manage.
* Window management is a productivity multiplier for long compile-run-debug cycles.

---

## Next Steps

* Build a reproducible **Forge Config YAML** (Keyd + GNOME shortcuts)
* Automate layout restoration using `wmctrl`
* Integrate setup guide into your **technical-blog series**: *“System Efficiency for AI Compiler Research.”*

---

## Deep Interactive Questions for Followers

1. **Workflow Depth** —
   How do you balance between full keyboard control and GUI convenience in your own development workflow?
   Where’s your “flow breakpoint” before switching context?

2. **System-Level Efficiency** —
   If you could design your own *developer OS layer*, what would you optimize first: input latency, visual focus, or workspace intelligence?

3. **Research Mindset** —
   For large-scale compiler or ML system research, what’s your philosophy on environment design — minimalism (bare-metal control) or integration (automated tooling)?

---

## Hashtags / Tags

`#UbuntuDev` `#TilingAssistant` `#MLIR` `#SystemProductivity` `#OpenSourceJourney` `#AICompiler` `#DeepWork` `#DevEnvironmentForge`

---

Welcome to follow My GitHub
