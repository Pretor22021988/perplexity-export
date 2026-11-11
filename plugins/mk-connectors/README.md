# mk-connectors

Коннекторы рабочего контура: практика РФ и США, научные базы, медицина, веб-доступ, документация. Только адреса, без ключей: вход в каждый сервис делается в каждом аккаунте.

| Коннектор | Адрес |
|---|---|
| `amazingcat` | https://mcp.amazingcat.net/mcp |
| `courtlistener` | https://mcp.courtlistener.com |
| `consensus` | https://mcp.consensus.app/mcp |
| `elicit` | https://elicit.com/api/mcp |
| `scite` | https://api.scite.ai/mcp |
| `scholar-gateway` | https://connector.scholargateway.ai/mcp |
| `pubmed` | https://pubmed.mcp.claude.com/mcp |
| `clinical-trials` | https://hcls.mcp.claude.com/clinical_trials/mcp |
| `firecrawl` | https://mcp.firecrawl.dev/v2/mcp-search |
| `semantica` | https://mcp.ai-semantica.com/mcp |
| `context7` | https://mcp.context7.com/mcp |
| `cloudflare` | https://bindings.mcp.cloudflare.com/mcp |
| `composio` | https://connect.composio.dev/mcp — 500+ приложений через Composio; доступ к каждому приложению выдаётся внутри Composio отдельно |

## В каждом аккаунте

Customize → Plugins → mk-connectors → вкладка **Connectors** → у каждой строки **Add** (если «Not added»), затем **Connect** и вход в сервис в браузере. Коннектор, уже подключённый в аккаунте по тому же адресу, показывается как **Connected** и второй раз не добавляется.

## В Claude Code

Серверы загружаются вместе с плагином. Вход: `claude` → `/mcp` → у каждого сервера Authenticate.

## Чего здесь нет и почему

- Google Drive — встроенный коннектор Anthropic, подключается из каталога Customize → Connectors в каждом аккаунте.
- Серверы с ключом в адресе или в заголовке — ключ попал бы в файлы каждого, кто ставит плагин; такие подключаются вручную.
- casus.legal — нет учётной записи у сервиса.

Установка в Claude Code (2.1.275+): `/plugin install mk-connectors --marketplace Pretor22021988/monakhov-skills`
