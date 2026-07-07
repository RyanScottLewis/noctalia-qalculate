# Noctalia Qalculate

A Noctalia plugin that provides a quick calculator panel powered by qalculate.

<p align="center">
  <img src="/assets/preview.png" alt="Screenshot of the calculator panel with an input text box and history entries visible" />
</p>

## Features

- Uses amazing [libqalculate](https://github.com/qalculate/libqalculate)
- Persistent expression history
- ~~Copy results to clipboard~~

## Requirements

- [noctalia v5](https://github.com/noctalia-dev/noctalia)
- [qalc](https://github.com/qalculate/libqalculate)

## Installation

1. Clone this repository into your Noctalia plugins directory:

```sh
mkdir -p ~/.local/share/noctalia/plugins
cd ~/.local/share/noctalia/plugins
git clone https://github.com/shadr/noctalia-qalculate
```

3. (Optional) If Noctalia doesn't see the plugin, then add that `plugins` directory as a plugins source for Noctalia

   `Noctalia Settings > Plugins > Add source > Path`

4. Enable the plugin in Noctalia settings

5. Bind a key to open the calculator panel

## Usage

### IPC Command

The plugin uses built-in Noctalia messages to trigger the calculator panel

```sh
noctalia msg panel-toggle shadr/noctalia-qalculate:panel
```

### Keyboard Shortcuts

Once the panel is open:

- **Enter** - Save current calculation to history
- ~~**Ctrl+C** - Copy result to the clipboard~~ currently not supported in Noctalia v5
- **Esc** - Close panel

## Key Binding Examples

#### Niri

```
binds {
    Mod+A { spawn "noctalia" "msg" "panel-toggle" "shadr/noctalia-qalculate:panel"; }
}
```

#### Hyprland

```
bind = Mod+A, exec, noctalia msg panel-toggle shadr/noctalia-qalculate:panel
```

## Legacy Noctalia v4
You can find quickshell based version of this plugin in [another](https://github.com/shadr/noctalia-qalculate/tree/noctalia-v4) branch.


## License

MIT License - See [LICENSE](LICENSE) for details.
