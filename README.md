# Thinkies Marketplace

A curated collection of claude code skills designed to enhance reasoning.

## Installation

### Adding to Claude Code

1. Clone this repository or download the plugin you want
2. Copy the plugin directory to your `.claude/plugins/` folder:

   ```bash
   cp -r plugins/thinkies ~/.claude/plugins/
   ```

3. Restart Claude Code or reload your configuration

### Direct GitHub Installation

Add to your Claude Code settings:

```json
{
  "plugins": {
    "marketplaces": [
      "https://raw.githubusercontent.com/synapseradio/thinkies/master/marketplace.json"
    ]
  }
}
```

## Contributing

To add your plugin to this marketplace:

1. Fork this repository
2. Add your plugin to the `plugins/` directory
3. Update `marketplace.json` with your plugin information
4. Submit a pull request

## Plugin Requirements

Each plugin must include:

- `plugin.json` with metadata (name, version, description, author, skills, keywords, compatibility)
- Skills in the proper directory structure
- Clear documentation in a README

## License

See individual plugin directories for licensing information.
