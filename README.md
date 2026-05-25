# GayXXX Sovereign NSFW CloudStream Repository (Clean Relaunch)

**Status**: Ready for private repo push. Uses correct `repo.json` + `pluginLists` structure that latest CloudStream pre-releases expect.

## Critical Fix Applied
Previous attempts failed because `plugins.json` (the array) was being added directly. CloudStream requires a thin `repo.json` manifest whose `pluginLists` points to the array.

## Install (after push)
1. CloudStream → Settings → Extensions → **enable NSFW / Adult content**.
2. Add repository → paste the **raw URL to your new repo's repo.json**.
3. It will load all 20 providers cleanly.

## 3 Mutated Asymmetric Data Harvester Prompts (Fixed, Real OSINT Style)
Removed all internal tokens. Linear exact-match OR chains + heavy exclusion tails. Use exactly as written.

**Fix 1 — GitHub Raw / CDN / Ref-Branch Delivery**
```
"github raw content" OR "raw.githubusercontent.com" OR "builds/plugins.json" OR "repository manifest" OR "repo.json pluginLists" OR "raw github 404 json" -site:pinterest.com -site:medium.com -site:reddit.com -site:quora.com -site:stackoverflow.com -site:facebook.com -site:twitter.com -site:instagram.com
```

**Fix 2 — Android App JSON Manifest Parser Fragility (latest pre-release)**
```
"cloudstream" "repo.json" OR "pluginLists" OR "manifestVersion" OR "repository import" OR "add repository" parser OR loader OR "does not contain any providers" -site:pinterest.com -site:medium.com -site:reddit.com -site:quora.com -site:stackoverflow.com -site:facebook.com -site:twitter.com -site:instagram.com
```

**Fix 3 — NSFW Extension Repo Deployment Hygiene**
```
"cloudstream" ("builds/repo.json" OR "builds/plugins.json") (NSFW OR adult OR gay) (repository OR extension) -site:pinterest.com -site:medium.com -site:reddit.com -site:quora.com -site:stackoverflow.com -site:facebook.com -site:twitter.com -site:instagram.com
```

## Included Tools
- `cs3_inspector.py` — run locally on any .cs3 to extract strings/domains and vet before trusting.
- Full verified list of raw .cs3 links from the original repo (grabbed via site: + raw.githubusercontent.com).

## Structure (matches real CloudStream pre-release repos)
repo.json (what you add)  
builds/ (optional future .cs3 mirror)  
cs3_inspector.py  
README.md

Private repo note: GitHub raw on private repos usually needs auth. The current `repo.json` points to the public proven `plugins.json` so it works immediately in the app. If you want fully self-hosted .cs3 later, we can extend.

Sovereign. Unblinded. Ready.
