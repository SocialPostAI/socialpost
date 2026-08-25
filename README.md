# SocialPost.ai MCP Server

Connect the AI you already use — Claude, ChatGPT, or Grok — to your [SocialPost.ai](https://socialpost.ai/?utm_source=github&utm_medium=mcp-repo&utm_campaign=mcp-directory) workspace. Your AI writes the post; SocialPost.ai makes it look like your brand, schedules it, and publishes it — like having a marketing team on LinkedIn.

This is a **remote MCP server**. There is nothing to install and no code in this repository to run: add the URL below as a custom connector in your AI app and sign in.

```
https://api.socialpostai.com/api/mcp/
```

## Set it up

You need a SocialPost.ai account ([free to start](https://socialpost.ai/?utm_source=github&utm_medium=mcp-repo&utm_campaign=mcp-directory)).

**Claude** (claude.ai, Desktop, or Code) — Settings → Connectors → *Add custom connector* → paste the URL → sign in and authorize.

**ChatGPT** (web only, paid plan) — Settings → Connectors → *Advanced settings* → turn on **Developer mode**. Then Settings → Connectors → *Create*, paste the URL, keep OAuth, sign in. In a chat, enable SocialPost.ai from the **+** menu before asking.

**Grok** — Settings → Connectors → add a custom connector → paste the URL → sign in.

On a Team/Business/Enterprise plan, an admin usually has to add or allow the connector first — full per-platform steps live on the **Connect your AI** page inside the app.

## What your AI can do with it

- See your workspace: plan, team, connected accounts, this month's usage
- Check your calendar and history: what's queued, what went out, what failed
- Save drafts, with different text per network
- Generate posts in your brand voice and tone, or from a link you paste
- Create a branded image for a post: your logo and colors over an AI background
- Schedule to X, LinkedIn, Facebook, Instagram, YouTube and Threads, in your timezone
- Preview exactly what each network will get, then publish on your say-so
- Cancel anything that hasn't gone out yet

## You stay in control

- Nothing publishes without your explicit approval in the chat
- Scheduled posts are set at least 10 minutes out and can be cancelled
- Connecting your social accounts happens only in the web app
- To disconnect, remove the connector in your AI app — access ends at once

## Technical notes

- Transport: MCP **Streamable HTTP**, stateless. OAuth 2.1 (authorization code + PKCE) with dynamic client registration, or a static API token via the `Authorization` header.
- Discovery: `/.well-known/oauth-protected-resource/api/mcp` and `/.well-known/oauth-authorization-server` on the same host.
- The server itself is part of the SocialPost.ai product and is not open source; this repository is its public documentation and registry manifest.

## Support

Questions or issues: [socialpost.ai](https://socialpost.ai/?utm_source=github&utm_medium=mcp-repo&utm_campaign=mcp-directory) → support, or open an issue here.
