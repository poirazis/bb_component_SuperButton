# Super Button

A custom Budibase component that adds an enhanced button to the builder component panel.

## Features

- Label, size, type, and style variants
- Optional icon (Phosphor), tooltip, and quiet/disabled states
- Action modes: click, timer, loop, and conditional
- Confirmation prompt and working-state feedback

## Install in Budibase

1. Build the plugin (see below) or download the release `.tar.gz` from `dist/`.
2. In Budibase, open **Settings → Plugins → Add plugin**.
3. Upload `bb_component_SuperButton-1.0.0.tar.gz`.
4. In the builder, find **Super Button** in the components panel and drag it onto your screen.

## Development

```bash
bun install
bun run build      # outputs dist/bb_component_SuperButton-1.0.0.tar.gz
bun run watch      # rebuild on change
```

Built with Svelte 5. Requires a Budibase instance that supports Svelte 5 custom components.