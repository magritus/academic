# Academic Project Memory

## Tools & Infrastructure
- **Zotero 8.0.3** installed via Homebrew (`brew install --cask zotero`)
- **zotero-mcp** (v0.1.2) installed via `uv tool install` from GitHub
- MCP server registered in Claude Code as `zotero` with `ZOTERO_LOCAL=true` (user scope)
- Zotero must be running for the MCP server to work (local API)
- To enable local API: Zotero > Settings > Advanced > "Allow other applications on this computer to communicate with Zotero"

## Academic Research MCP Stack (all user scope)
| MCP Server | Purpose | Command |
|---|---|---|
| `zotero` | Mevcut kütüphane yönetimi | `zotero-mcp serve` |
| `semanticscholar` | Atıf ağları, yazar h-index, makale detayları | `semanticscholar-mcp-server` |
| `paper-search` | 7+ kaynaktan makale arama (arXiv, PubMed, bioRxiv...) | `uv run --with paper-search-mcp python -m paper_search_mcp.server` |

- **semanticscholar-mcp-server** (v0.1.0) - `uv tool install semanticscholar-mcp-server`
- **paper-search-mcp** (v0.1.3) - no executable entry point, run as module via `uv run --with`

## Project Structure
- `/Users/ziyahan/academic/` - main academic workspace
- `/Users/ziyahan/academic/zotero-research/` - git repo for research notes/config

## Key Commands
- `zotero-mcp serve` - the MCP server command
- `claude mcp list` - verify MCP server status
- uv is at `/Users/ziyahan/.local/bin/uv` (v0.9.13)
