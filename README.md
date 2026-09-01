# Invest Like a Girl Agent Plugin

Read-only access to the authenticated Invest Like a Girl community from Codex, ChatGPT, Claude, and other OAuth-capable MCP clients.

## Remote MCP

`https://www.investlikeagirl.com.br/mcp`

The server uses OAuth 2.1 with PKCE and dynamic client registration. An active ILG trial or membership is required to read community and learning content. The MCP exposes no write tools, attachments, member directory, email addresses, payment actions, or moderation controls.

## Available tools

- `get_my_ilg_context`
- `list_ilg_channels`
- `search_ilg_community`
- `get_ilg_thread`
- `list_my_ilg_questions`
- `search_ilg_library`

## Claude Code

Install this directory as a plugin or add the remote MCP URL directly. The included `.mcp.json` is discovered by the plugin.

## Claude custom connector

In Claude, open **Customize > Connectors**, select **Add custom connector**, and enter the remote MCP URL above. Connect your Invest Like a Girl account and approve the requested read-only scopes.

Setup, example prompts, limitations, and troubleshooting are documented at:

`https://www.investlikeagirl.com.br/integracoes/claude`

## ChatGPT and Codex

Connect the remote MCP URL and complete the Invest Like a Girl login and consent flow when prompted.

Community posts remain the words of their authors. Official staff content is marked `admin` or `fundadora`. All financial content is educational, not personalized investment advice.

Privacy policy: `https://www.investlikeagirl.com.br/legal/privacy`

Support: `contato@investlikeagirl.com.br`
