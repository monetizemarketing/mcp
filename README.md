<p align="center">
  <img src="https://raw.githubusercontent.com/monetizemarketing/.github/main/profile/assets/banner.png" alt="" width="100%">
</p>

# Monetize Marketing MCP

Connect the **Monetize Marketing App** to Claude, ChatGPT, Cursor, VS Code, Codex or any AI tool that speaks MCP. Your Brain, mission, training, skills, routines, Library and software mini-apps become tools inside the AI you already use.

**One URL, no key to paste or leak.** Sign in with your Monetize Marketing membership when the client asks.

```
https://app.monetizemarketing.com/api/mcp
```

Transport: Streamable HTTP · Auth: OAuth 2.1 with dynamic client registration · Spec versions: 2025-06-18, 2025-03-26, 2024-11-05 · Not a member yet? The sign-in page shows how to start the 14-day trial.

---

<p align="center"><img src="https://raw.githubusercontent.com/monetizemarketing/.github/main/profile/assets/connect.gif" alt="Claude Code: claude mcp add, /mcp, Authenticate, connected" width="100%"></p>

## 1 · Paste this into your AI

Works in any client that can add MCP servers by itself (Claude, ChatGPT in developer mode, Codex, Cursor's agent and most agent platforms). Copy the box, paste it as a message, approve the sign-in link.

```text
Add my Monetize Marketing connector:
https://app.monetizemarketing.com/api/mcp
- Setup: standard MCP over Streamable HTTP with OAuth 2.1 (dynamic client registration). Send me the sign-in link and I will approve it in my browser.
- If you cannot add MCP servers yourself, show me the exact steps for this client, taken from https://github.com/monetizemarketing/mcp.
- Once connected, run get_mission and tell me my next goal.
```

Your client is not listed below? The prompt above is the fallback for every MCP-capable tool.

## 2 · Or add it by hand

| Client | How |
|---|---|
| **Claude.ai** (web) | Settings → Connectors → **Add custom connector** → name `Monetize Marketing`, URL `https://app.monetizemarketing.com/api/mcp` → Connect → sign in. |
| **Claude Desktop** | Same path: Settings → Connectors → Add custom connector (connectors sync with claude.ai). |
| **Claude Code** (terminal) | `claude mcp add --transport http monetize-marketing https://app.monetizemarketing.com/api/mcp` then type `/mcp` and pick **Authenticate**. ([clients/claude-code.sh](clients/claude-code.sh)) |
| **ChatGPT** | Settings → Apps → Advanced settings → **Developer mode** on → Apps → **Create** → endpoint `https://app.monetizemarketing.com/api/mcp`, auth **OAuth** → Scan tools → Create. Full tools need a Business, Enterprise or Edu workspace; Pro connects read-only. |
| **Cursor** | [![Install in Cursor](https://cursor.com/deeplink/mcp-install-dark.png)](cursor://anysphere.cursor-deeplink/mcp/install?name=monetize-marketing&config=eyJ1cmwiOiJodHRwczovL2FwcC5tb25ldGl6ZW1hcmtldGluZy5jb20vYXBpL21jcCJ9) or drop [clients/cursor-mcp.json](clients/cursor-mcp.json) into `.cursor/mcp.json`. |
| **VS Code** (Copilot) | [Install in VS Code](vscode:mcp/install?%7B%22name%22%3A%20%22monetize-marketing%22%2C%20%22type%22%3A%20%22http%22%2C%20%22url%22%3A%20%22https%3A//app.monetizemarketing.com/api/mcp%22%7D) or add [clients/vscode-mcp.json](clients/vscode-mcp.json) to `.vscode/mcp.json`, then **Start** the server and sign in. |
| **OpenAI Codex** | `codex mcp add monetize-marketing --url https://app.monetizemarketing.com/api/mcp` then `codex mcp login monetize-marketing` ([clients/codex-config.toml](clients/codex-config.toml)). |

## 3 · First things to ask

```text
What is my mission and which goal should I work on next?
```
```text
Search my Brain for my core offer and the audience it serves.
```
```text
What is new in AI this week that matters for my niche?
```
```text
Save this plan to my Library as a document called "Q4 launch plan".
```

## 4 · What the tools do

| Group | Tools | Tier |
|---|---|---|
| Brain (memory) | `memory_search` · `memory_get_profile` · `memory_get_recent` · `memory_save` | every member |
| Mission + feed | `get_mission` · `update_goal_status` · `get_feed` · `decide_action` | every member |
| Training + prompts | `search_course_transcripts` · `search_prompt_library` · `get_prompt` · `get_brand_voice` · `get_product_sheet` | every member |
| Skills + routines | `list_skills` · `run_skill` · `run_catalog_skill` · `run_workflow` · `create_routine` · `list_routines` · `toggle_routine` · `list_routine_runs` | Gold and up |
| Research | `web_search` · `web_read` · `get_ai_news` · `radar_watch` · `instagram_scan` · `niche_scout` | Gold and up |
| Library + media | `save_document` · `list_files` · `generate_image` · `generate_video` · `get_credit_balance` · `get_brain_level` | every member (credits apply) |
| Shop Builder | `shop_get` · `shop_rename` · `shop_recolor` · `shop_set_logo` · `shop_add_design` · `shop_remove_design` · `shop_pause` · `shop_resume` | Platinum |

Every tool runs through the same routes the app uses, with the same tier gates, credit meter and rate limits. A scoped Brain key only sees the tools its scopes allow. Every call is audited.

## 5 · Troubleshooting

| You see | Paste this back to your AI |
|---|---|
| "This Brain key is not allowed to use that tool." | `My membership tier or key scope does not include that tool. Use only the tools in tools/list and tell me which one you tried.` |
| 401 after a while | `Re-authenticate the Monetize Marketing connector: start the OAuth flow again and send me the link.` |
| 429 | `Wait 60 seconds, then retry the last Monetize Marketing call once.` |
| The connector cannot be added by the client | `Follow the manual steps for this client from https://github.com/monetizemarketing/mcp#2--or-add-it-by-hand` |

## Privacy + security

- OAuth 2.1 with PKCE and dynamic client registration; tokens expire and are hashed at rest. [Authorization server metadata](https://app.monetizemarketing.com/.well-known/oauth-authorization-server) · [Protected resource metadata](https://app.monetizemarketing.com/.well-known/oauth-protected-resource).
- No tool can read another member's data. Failed sign-ins are throttled per credential.
- Terms, privacy and the data we keep: [monetizemarketing.com/legal](https://monetizemarketing.com/legal). Support: support@monetizemarketing.com.

---

Monetize Marketing, Charleroi, Belgium · VAT BE0782.725.563 · [monetizemarketing.com](https://monetizemarketing.com) · [@buziziclo](https://x.com/buziziclo)
