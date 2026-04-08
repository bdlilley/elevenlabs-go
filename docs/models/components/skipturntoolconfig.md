# SkipTurnToolConfig

Allows the agent to explicitly skip its turn.

This tool should be invoked by the LLM when the user indicates they would like
to think or take a short pause before continuing the conversation—e.g. when
they say: "Give me a second", "Let me think", or "One moment please".  After
calling this tool, the assistant should not speak until the user speaks
again, or another normal turn-taking condition is met.  The tool itself has
no parameters and performs no side-effects other than informing the backend
that the current turn generation is complete.


## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `SystemToolType`   | `*string`          | :heavy_minus_sign: | N/A                |