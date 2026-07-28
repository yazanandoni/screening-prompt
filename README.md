# Screening Prompt for a Survey of Decentralized LLM-based Multi-agent Systems

This repository accompanies a survey paper on decentralized LLM-based multi-agent systems.
It contains the system prompt used in the LLM-assisted screening stage of the literature
review.

## Contents

- `screening-prompt.md` — the system prompt passed to GPT-5 during title and abstract
  screening.

## How the prompt was used

Each of the 2671 deduplicated records was sent as a separate user message containing the
paper's title and abstract. The model returned a JSON object with a relevance score from 1
to 10, any failed inclusion or triggered exclusion criteria, and a short justification.
Papers scoring at least 7 were retained for manual abstract review by human researchers.
The automated score was used to prioritize papers, not to make the final selection.
