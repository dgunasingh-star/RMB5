# Sales Super-Agent (plugin)

Turns an account executive's Claude into a sales super-agent. This plugin is the client-side bundle;
it pairs with the remote sales gateway (the MCP server) that does the dynamic work.

## Components

- **Skills** (native, auto-triggered by description)
  - `para-method` — how to organize the PARA+I sales workspace: file by actionability, a live deal is
    a project, an account/territory is an area, and on close you archive **and** write an insight.
  - `deal-qualification` — a BANT/MEDDIC checklist for sizing up a new opportunity.
- **MCP server** — `sales-super-agent`: the remote gateway providing intent tools (e.g. get_deal_context),
  first-time workspace setup, and the `sync_check` update engine for writable workspace content.

## Setup

Install the plugin. The connector and the skills are wired up automatically — no manual connector setup.

## Notes

- The MCP server URL is currently a POC cloudflared tunnel and changes when the tunnel restarts;
  production uses a stable hosted endpoint (ideally an org directory entry referenced by name).
