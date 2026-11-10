# Local patches

This fork of ProgressPlanner/markdown-alternate 1.1.0 (base `0f72fb5`) carries patches
that upstream has not merged. Drop a patch when upstream merges it.

| Patch | Upstream | Why |
|---|---|---|
| Keep the site root out of the Yoast llms.txt `.md` rewrite | none (draft PR in the vault) | A static front page produced `https://example.com.md` in llms.txt |
| Stop page caches storing the Accept negotiation 303 | PR #31, issue #30 | Pantheon's edge ignored `Vary: Accept` and served the 303 to browsers for 10 minutes |

Tag `1.1.0-cr.1` is the first patched release. The plugin header still says 1.1.0.
