# JBeam for Sublime Text

Syntax highlighting for BeamNG `.jbeam` files in Sublime Text (ST3/ST4).

This is heavily inspired by (and originally derived from the TextMate grammar shipped in) BeamNG’s official VS Code extension:
https://github.com/BeamNG/vscode-jbeam-editor

Also yes: we basically spun up an agent, pointed it at that repo, and vibed this package into existence in more or less one prompt.


## Install (Preferred): Package Control

This repo includes a Package Control repository definition at `repository.json`.

1. Open `repository.json` on GitHub and click **Raw**
2. Copy that URL
3. In Sublime: `Preferences → Package Control: Add Repository`
4. Paste the Raw URL
5. `Preferences → Package Control: Install Package` → install `JBeam`

## Install (Manual)

Drop the files into your Packages folder under a `JBeam` directory.

- Find Packages: `Preferences → Browse Packages...`
- Create: `JBeam` folder
- Copy in:
  - `JBeam.sublime-syntax`
  - `JBeam Dark.sublime-color-scheme`
  - `JBeam Light.sublime-color-scheme`
  - `JBeam.sublime-settings`
  - `Comments.tmPreferences`
  - `Default.sublime-keymap`

Windows path note:
- Most installs use `%APPDATA%\Sublime Text\Packages\` (ST4) or `%APPDATA%\Sublime Text 3\Packages\` (ST3).
- Some setups/portable installs use a `Data\Packages\` folder next to the executable.


## What’s Highlighted

- JSON structures + C-style comments (`//`, `/* */`)
- jBeam keys get extra treatment:
  - section keys like `nodes`, `beams`, `flexbodies`, `mainEngine`, `slots`, `powertrain`, etc.
  - common modifiers like `coreSlot`, `default`, `beamSpring`, `nodeWeight`, etc.

## Extra Features

- Comment toggling via `Ctrl+/` (line) and `Ctrl+Shift+/` (block)
- Dark and Light color schemes included

### Highlighted Section Keywords

These top-level object keys receive bold styling to help navigate large jBeam files:

`information` · `slotType` · `slots` · `slots2` · `flexbodies` · `props` · `nodes` · `beams` · `triangles` · `quads` · `rails` · `slidenodes` · `torsionbars` · `torsionHydros` · `hydros` · `rotators` · `commands` · `pressureWheels` · `powertrain` · `mainEngine` · `engine` · `gearbox` · `torqueConverter` · `turbocharger` · `supercharger` · `nitrousOxideInjection` · `controller` · `soundConfig` · `soundConfigExhaust` · `sounds` · `refNodes` · `cameraExternal` · `cameraChase` · `cameraDash` · `variables` · `globalsBehavior` · `managedStorage` · `triggers` · `electronicStability` · `tractionControl` · `antiLockBrakes` · `wheelAlignmentCoef` · `activeDiffControl` · `components` · `glowMap` · `input` · `energyStorage` · `clutch` · `transfercase` · `gauges` · `gauge` · `licenseplateFormat` · `events`



## Color Schemes (Optional)

You do not need these color schemes. The syntax uses standard scopes and should look fine with Sublime defaults, or whatever scheme you already like.

If you want them anyway:

- `Preferences → Select Color Scheme...` → pick `JBeam Dark` or `JBeam Light`

To apply only for `.jbeam` files, add this to your user settings:

```json
"file_settings": [
  {
    "selector": "source.jbeam",
    "settings": {
      "color_scheme": "Packages/JBeam/JBeam Dark.sublime-color-scheme"
    }
  }
]
```


## License

This repo is MIT (see `LICENSE`)
