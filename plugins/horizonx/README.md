# HorizonX

Search [HorizonX](https://horizonx.so) in plain language and add the result to your project: animated UI components, device mockups, image textures and WebGL shaders exported as HTML, Svelte or React, plus landing page templates, UI kits, design systems, 3D models and open-source icon libraries from the HorizonX Library.

This plugin contains:

- **The HorizonX MCP server** at `https://horizonx.so/api/mcp`. You sign in with your HorizonX account (OAuth) the first time your agent uses it. An active HorizonX membership is required.
- **The `horizonx` skill**, which tells the agent how to search, inspect a component's parameters, export it in your project's framework and place the file next to similar components, and how to build UI that follows a HorizonX design system.

To use HorizonX in a chat app instead, it is listed in the [Claude connectors directory](https://claude.ai/directory/horizonx) and in [ChatGPT apps](https://chatgpt.com/plugins/plugin_asdk_app_6ad2d15c798481919ffe2ec242b81cf3).

## Tools

| Tool | What it does | Changes anything? |
| --- | --- | --- |
| `search_components` | Searches components, mockups, textures and shaders | No |
| `get_component` | Shows one component and its parameters | No |
| `export_component` | Returns code for a component | Uses one daily export the first time |
| `search_library` | Searches templates, UI kits, design systems, images, videos, 3D models and icon libraries | No |
| `get_library_item` | Shows one Library product | No |
| `download_library_item` | Returns short-lived download links | Uses one download the first time that day |
| `get_design_md` | Returns a design system's DESIGN.md: its tokens and the rules for using them | No |

## Data the plugin sends

The plugin sends only what you ask the agent to look up: your search text, the component or product slug, the chosen framework and any parameter overrides. These go to HorizonX over HTTPS, together with the OAuth token that identifies your account. It does not read or upload your project files. HorizonX logs tool calls to count exports and downloads against your plan. See the [privacy policy](https://horizonx.so/privacy).

## Support

[horizonx.so/support](https://horizonx.so/support) · support@horizonx.so · [Terms](https://horizonx.so/terms)
