# HorizonX plugin for AI coding agents

Search [HorizonX](https://horizonx.so) in plain language and drop the result straight into your code: animated UI components, image textures and WebGL shaders exported as HTML, Svelte or React with no dependencies, plus landing pages, UI kits and design systems as files.

The plugin bundles two things:

- **The HorizonX MCP server** (`https://horizonx.so/api/mcp`). You sign in with your HorizonX account the first time your agent uses it; there is no key to copy.
- **The `horizonx` skill**, which teaches the agent the workflow: search, inspect the parameters, export in your project's framework and place the file where similar components live.

An active HorizonX membership is required.

## Install

### Claude Code

```
/plugin marketplace add Mdx2025/horizonx-agent-plugin
/plugin install horizonx@horizonx
```

Then run `/mcp`, pick `horizonx` and sign in.

### Codex

```
codex plugin marketplace add Mdx2025/horizonx-agent-plugin
codex plugin add horizonx@horizonx
codex mcp login horizonx
```

### Cursor

Cursor reads this plugin as an [Agent Plugin](https://agent-plugins.org). Until it is listed in the Cursor Marketplace, copy `plugins/horizonx` to `~/.cursor/plugins/local/horizonx`, reload the window and sign in when Cursor asks. To add only the MCP server, use the **Add to Cursor** button on [horizonx.so/mcp](https://horizonx.so/mcp).

### Gemini CLI

```
gemini extensions install https://github.com/Mdx2025/horizonx-agent-plugin
```

### Claude.ai and ChatGPT

HorizonX is listed in the [Claude connectors directory](https://claude.ai/directory/horizonx) and in [ChatGPT apps](https://chatgpt.com/plugins/plugin_asdk_app_6ad2d15c798481919ffe2ec242b81cf3). Open the listing, connect it and sign in with your HorizonX account.

### Any other MCP client

[horizonx.so/mcp](https://horizonx.so/mcp) has the setup for VS Code, Windsurf, Gemini CLI, Claude.ai, ChatGPT and others.

## Try it

- "Use HorizonX to add an animated hero background to this page."
- "Use HorizonX to find a before-and-after image slider and add it as a React component."
- "Use HorizonX to find a SaaS landing page template."
- "Use HorizonX to build this dashboard in the style of a HorizonX design system, following its DESIGN.md."

## Layout

```
.claude-plugin/marketplace.json      Claude Code marketplace
.agents/plugins/marketplace.json     Codex marketplace
.cursor-plugin/marketplace.json      Cursor marketplace (points at plugins/horizonx)
gemini-extension.json                Gemini CLI extension (MCP server only)
server.json                          Official MCP Registry entry
plugins/horizonx/
  plugin.json, mcp.json              Agent Plugins manifest (Codex, Cursor, OpenAI listing and review cases)
  .claude-plugin/plugin.json, .mcp.json   Claude Code manifest
  skills/horizonx/SKILL.md           The skill
  README.md                          Tools and the data the plugin sends
  assets/icon.png
```

`mcp.json` has no `extensions["com.openai"].auth` block on purpose: Codex 0.163.0 drops a plugin MCP server that carries any `extensions` key. Codex discovers HorizonX's OAuth from the server, so nothing is lost.

## Support

support@horizonx.so · [Privacy](https://horizonx.so/privacy) · [Terms](https://horizonx.so/terms)
