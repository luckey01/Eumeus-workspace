# HEARTBEAT tasks

## Token usage logging
Each heartbeat: run `session_status` and append an entry to `logs/token-usage.json`.
Entry format: `{ "ts": "<ISO date>", "model": "<model>", "cached_tokens": N, "new_input_tokens": N, "output_tokens": N }`
Pricing (claude-sonnet-4-6): input $3/M, cache read $0.30/M, output $15/M.
Only append if new_input_tokens > 0 (skip if nothing happened since last heartbeat).
