# Ghostty Config

This repo contains a macOS Ghostty configuration and a bundled set of cursor shaders.

## Install Location on macOS

Place the files in Ghostty's macOS application support directory:

```text
/Users/<your-user>/Library/Application Support/com.mitchellh.ghostty/
```

The resulting layout should look like this:

```text
/Users/<your-user>/Library/Application Support/com.mitchellh.ghostty/
├── config
└── ghostty-cursor-shaders/
    ├── cursor_tail.glsl
    ├── cursor_warp.glsl
    ├── cursor_sweep.glsl
    └── ...
```

If you prefer `~` notation, that is:

```text
~/Library/Application Support/com.mitchellh.ghostty/
```

## What This Config Provides

- `TokyoNight Night` theme
- Semi-transparent background with blur
- Compact default window size: `110 x 30`
- Window title set to `Terminal`
- `Iosevka` font at size `14`
- Ligatures disabled with slightly thicker font rendering
- Global `Cmd + \`` shortcut to toggle Ghostty quick terminal
- Centered quick terminal at `80%` size
- Animated cursor shader via `ghostty-cursor-shaders/cursor_tail.glsl`

## Install Steps

1. Copy `config` to:

```text
~/Library/Application Support/com.mitchellh.ghostty/config
```

2. Copy the `ghostty-cursor-shaders` folder to:

```text
~/Library/Application Support/com.mitchellh.ghostty/ghostty-cursor-shaders
```

3. Restart Ghostty, or reload the config from Ghostty.

## Notes

- The shader path in `config` is relative:

```text
custom-shader = ghostty-cursor-shaders/cursor_tail.glsl
```

- Because of that, the `ghostty-cursor-shaders` folder must stay next to the `config` file.
- The shader files include other cursor effects if you want to switch from `cursor_tail.glsl` later.
