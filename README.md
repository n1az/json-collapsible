# JSON Collapsible Plugin for Obsidian

Display JSON data as beautiful, interactive collapsible trees in your Obsidian notes.

## Features

- 🌳 **Collapsible JSON Trees**: View JSON data with expandable/collapsible nodes
- 🎨 **Syntax Highlighting**: Color-coded values (strings, numbers, booleans, null)
- 📱 **Mobile & Desktop**: Works on all Obsidian platforms
- ⚡ **Lightweight**: Fast rendering with minimal overhead
- 🎯 **Simple Usage**: Just use standard JSON code blocks

## Installation

### Manual Installation

1. **Download the plugin files**
   - Download the latest release files from the [releases page](https://github.com/n1az/JSON-viewer/releases)
   - Or download these files directly from the `json-collapsible` folder in the repository:
     - `main.js` (required)
     - `manifest.json` (required)
     - `style.css` (optional - can be empty, styles are embedded in main.js)

2. **Locate your Obsidian vault**
   - Open Obsidian
   - Go to Settings → About → Vault
   - Note the vault folder location on your system

3. **Create the plugin folder**
   - Navigate to your vault folder
   - Go to `.obsidian/plugins/` (create the `plugins` folder if it doesn't exist)
   - Create a new folder called `json-collapsible`

4. **Copy the plugin files**
   - Copy the downloaded files into the `json-collapsible` folder
   - At minimum, you need `main.js` and `manifest.json`
   - Your folder structure should look like:
     ```
     YourVault/
     └── .obsidian/
         └── plugins/
             └── json-collapsible/
                 ├── main.js
                 ├── manifest.json
                 └── style.css (optional)
     ```

5. **Enable the plugin**
   - Restart Obsidian or reload the vault
   - Go to Settings → Community plugins
   - You should see "JSON Collapsible" in the list
   - Toggle it on to enable the plugin

## Usage

Once installed, you can display JSON data in your notes using JSON code blocks:

### Basic Example

````markdown
```json
{
  "name": "John Doe",
  "age": 30,
  "email": "john@example.com"
}
```
````

### Complex Example

````markdown
```json
{
  "users": [
    {
      "id": 1,
      "name": "Alice",
      "active": true,
      "roles": ["admin", "user"]
    },
    {
      "id": 2,
      "name": "Bob",
      "active": false,
      "roles": ["user"]
    }
  ],
  "metadata": {
    "total": 2,
    "page": 1,
    "lastUpdated": "2024-01-01"
  }
}
```
````

### Features in Action

- **Click the ▼ icon** to collapse a node
- **Click the ▶ icon** to expand a collapsed node
- **Item count** is shown when a node is collapsed
- **Color coding**:
  - 🟢 Green for strings
  - 🟡 Yellow for numbers
  - 🔵 Blue for booleans
  - Gray for null values

## Troubleshooting

### Plugin doesn't appear in the list

- Make sure the required files (`main.js` and `manifest.json`) are in the correct folder
- Check that the folder is named exactly `json-collapsible`
- Try restarting Obsidian completely

### JSON not rendering properly

- Verify your JSON is valid (you can use a JSON validator like [JSONLint](https://jsonlint.com/))
- Make sure you're using triple backticks with `json` language identifier
- Check that the plugin is enabled in Settings → Community plugins

### Invalid JSON error

If you see an "Invalid JSON" message, your JSON syntax has an error. Common issues:
- Missing commas between properties
- Trailing commas (not allowed in JSON)
- Unquoted keys
- Single quotes instead of double quotes

## Requirements

- Obsidian v0.15.0 or higher

## Support

If you encounter any issues or have suggestions:
- Open an issue on [GitHub](https://github.com/n1az/JSON-viewer/issues)
- Provide details about your Obsidian version and the issue you're experiencing

## License

This project is open source and available under the MIT License.

## Development

To build or modify the plugin:

1. Clone the repository
2. Navigate to the repository root
3. Make your changes to the files in the `json-collapsible` folder:
   - `main.js` - Main plugin code and embedded styles
   - `manifest.json` - Plugin metadata
   - `style.css` - Optional (currently unused, styles are in main.js)
4. Copy the modified files from `json-collapsible/` to your vault's `.obsidian/plugins/json-collapsible/` folder for testing
5. Restart Obsidian or reload the vault to see your changes

**Note**: This plugin embeds styles directly in `main.js` using the `addStyles()` method, so `style.css` is not currently used.

---

**Enjoy visualizing your JSON data in Obsidian! 🎉**
