# Local patches

This fork of ProgressPlanner/markdown-alternate 1.1.0 (base `0f72fb5`) carries patches
that upstream has not merged. Drop a patch when upstream merges it.

| Patch | Upstream | Why |
|---|---|---|
| Keep the site root out of the Yoast llms.txt `.md` rewrite | none (draft PR in the vault) | A static front page produced `https://example.com.md` in llms.txt |
| Stop page caches storing the Accept negotiation 303 | PR #31, issue #30 | Pantheon's edge ignored `Vary: Accept` and served the 303 to browsers for 10 minutes |
| Negotiate Accept only on singular views | issue #43 | `Accept: text/markdown` on a category, tag, author or date archive redirected to a `.md` URL that returns 404. Archives now fall through to the platform's edge converter, which answers them with Markdown |

Tag `1.1.0-cr.1` is the first patched release; `1.1.0-cr.2` adds the singular-only negotiation. The plugin header still says 1.1.0.
