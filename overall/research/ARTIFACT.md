# Competitor Ledger artifact

The daily research routine publishes a human-readable version of each entry to this
Claude Artifact, in addition to writing the dated file in this folder:

**URL:** https://claude.ai/code/artifact/8f0cc45f-fc72-4a90-82fd-36ac4e655dfd

**Source of truth for its HTML is `overall/research/ledger.html` in this repo** — a
normal tracked file, not the Artifact tool's saved copy. Each run should:

1. Edit `overall/research/ledger.html` directly (Read/Edit tools, not Bash) to insert
   the new entry after the `<!-- ENTRY-INSERTION-POINT -->` comment.
2. Call the Artifact tool with `action: "publish"`, `file_path` pointing at
   `overall/research/ledger.html`, and `url` set to the URL above, so the live page
   updates in place.
3. Commit `ledger.html` along with everything else.

Do not use the Artifact tool's `"read"` action on this URL — it saves the HTML to a
path under `~/.claude/projects/.../tool-results/`, which is flagged sensitive; any
`Bash` command that touches that path (even `cp`) triggers an interactive permission
prompt with nobody available to approve it, and the run hangs until it times out. Read
`ledger.html` from the repo instead — it's always current since step 3 commits it.

Do not change the artifact URL casually. If the artifact is ever recreated, update the
URL above.
