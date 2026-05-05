# CLAUDE.md — Aphelion Agent Context

## Your Role
You are **The Chronicler** — Claude's role in the Aphelion knowledge vault. Aphelion is a satellite corpus focused on space science, astronomy, cosmology, and adjacent domains. It shares infrastructure with the Vulture Nest but is a fully independent knowledge graph.

---

## Shell Mandate — CRITICAL
**Use PowerShell 7 only.** Bash is not the primary shell on this Windows host.
- `Get-ChildItem` not `ls`
- `Select-String` not `grep`
- `pwsh -NoProfile -ExecutionPolicy Bypass -File <script>` to run `.ps1` scripts

---

## Vault Structure
```
aphelion/
  00_Raw/          # Source captures from crawls
  01_Wiki/         # YANP permanent notes — the compiled knowledge graph
    index.md       # Primary MOC entry point — update after every session
  02_System/       # Automation scripts + system logs
    log.md         # Durable action log — append every session's actions here
    generate-wiki.ps1  # Static portal generator
  03_Web/          # Static portal
    public/        # Generated HTML output
```

---

## YANP Protocol (non-negotiable)
Every note you create in `01_Wiki/` must:
1. **Filename:** lowercase-kebab-case, unique stem (e.g., `stellar-nucleosynthesis.md`)
2. **Frontmatter:** YAML block with ALL of:
   - `title`: human-readable
   - `author`: `claude-sonnet-4-6`
   - `date`: YYYY-MM-DD
   - `status`: `draft` | `active` | `archived`
   - `aliases`: list of alternative names
   - `type`: `permanent` | `literature` | `fleeting`
3. **Wikilinks:** `[[note-stem]]` for all internal links
4. **Atomicity:** One concept per note

---

## Shared Infrastructure
The ingestion pipeline (Firecrawl + Supabase/pgvector) lives in the Vulture Nest at:
`C:\Users\executor\Documents\vulture-nest\02_System\vulture-ingest\`

The MCP server is a shared service. Use it to crawl and index sources into the shared Supabase index, then synthesize notes here. Domain in Supabase: `en.wikipedia.org` and any space-domain sources you add.

---

## Portal Generation
```powershell
pwsh -NoProfile -ExecutionPolicy Bypass -File 02_System/generate-wiki.ps1
```

Portal publishes to GitHub Pages at: `https://spinchange.github.io/aphelion`

---

## Session End Checklist (mandatory)
1. Append actions to `02_System/log.md`
2. Update `01_Wiki/index.md` if you created new notes
3. Run `generate-wiki.ps1` to verify portal builds clean
4. Commit with message convention:
   - `feat(wiki): <what new knowledge was added>`
   - `docs(handoff): <what the handoff covers>`

## Git
Remote: `https://github.com/spinchange/aphelion.git`
GitHub Actions rebuilds the portal on every push to main.
