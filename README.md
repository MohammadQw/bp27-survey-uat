# BP-27 Transactional Survey in App — Staging (UAT / QA)

Part of the **AKB — ADI Knowledge Based** delivery workflow for project **BP27**
(https://akb.diyardemo.com). AKB tracks three separate repositories, one per environment:

| Environment | Repository | Branches |
|---|---|---|
| Development | [bp27-survey-dev](https://github.com/MohammadQw/bp27-survey-dev) | `develop`, `feature/TASK-NNN-*` |
| Staging (UAT / QA) | [bp27-survey-uat](https://github.com/MohammadQw/bp27-survey-uat) | `uat`, `release/*` |
| Production | [bp27-survey](https://github.com/MohammadQw/bp27-survey) | `main` only |

**This repository: Staging (UAT / QA).** QA and user acceptance: `uat` plus release candidates. Code arrives here only by human promotion from Development.

## Working here with Claude Code

1. `claude mcp add --transport http akb https://akb.diyardemo.com/api/mcp`, then `/mcp` → akb →
   Authenticate (sign in to the AKB portal and click Allow).
2. Ask Claude to *sync BP27 from AKB* — it downloads the approved `knowledge/`, `CLAUDE.md`, the
   agents and the hooks. Then run `python3 .akb/akb_hook.py install` once.
3. Follow `CLAUDE.md`. Only APPROVED documents are authoritative; agents never approve their own work.
