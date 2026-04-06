# Model Routing Strategy

## Default: Ollama (Local Llama 3)
- Endpoint: http://localhost:11434/api/generate
- Cost: $0
- Speed: Fast (local)
- Quality: Good for conversation, summarization, data tasks
- Use for: Calendar lookups, data fetching, formatting, casual conversation, brainstorming

## Upgrade to Haiku when:
- Complex reasoning or multi-step logic needed
- Writing in Luckey's voice (Bets, Pitches, important messages)
- Technical analysis or detailed explanations
- Anything flagged as high-stakes

## Upgrade to Sonnet when:
- Extremely complex problem-solving
- Strategic analysis
- Code review or architecture decisions
- When explicitly requested

## Manual Override
User can force a model with `/model haiku` or `/model sonnet` during conversation.

## Cost Optimization
- Ollama: $0 per token (local compute only)
- Haiku: $1/M input, $5/M output
- Sonnet: $3/M input, $15/M output

Default routing saves ~90% on API costs.
