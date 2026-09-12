# Socratic Shield

**Socratic Shield** is an experimental research prototype exploring a behavioral and conversational approach to mitigating jailbreak attempts in large language models.

## Project idea

The prototype separates two responsibilities:

- **Agent A — Answer System:** understands the request, retrieves relevant knowledge, and produces a response.
- **Agent B — Behavioral Monitor:** observes the conversation, tracks relevant behavioral signals, maintains topic-specific safety state, and decides when the Socratic Shield should activate.

The project explores whether conversation trajectory and behavioral signals can provide useful safety evidence in addition to analyzing individual prompts.

## Current prototype

The current public prototype is **v3.7**.

It demonstrates:

- Request understanding
- Topic-specific conversation state
- Separate attention and risk scores
- A defined safety-boundary trigger
- Socratic Shield activation
- Safe, non-operational responses after activation
- A second-boundary hard stop
- Thread-level hard-stop behavior
- Clean state in a new conversation
- Knowledge retrieval through a Wikipedia-based knowledge tool
- Local fallback behavior when the Gemini language tool is unavailable

### Live prototype

[Open the Socratic Shield v3.7 prototype](https://bhattseerat33-gif.github.io/Socratic-shield/prototype/socratic_shield_v3.7.html)

## Repository contents

- `prototype/` — public HTML prototype
- `Socratic_Shield_Research_Paper_Final.docx` — research paper
- `Socratic_Shield_Final_Evaluation_Results.xlsx` — evaluation results
- `README.md` — project overview

## Evaluation

The project includes a small manually constructed evaluation covering:

1. Benign educational questions
2. Topic switching
3. Ambiguous security questions
4. Authorized security questions
5. Unauthorized escalation
6. Repeated safety-boundary crossing
7. Thread-level hard stop
8. New-conversation state reset

The evaluation is a proof-of-concept test of the prototype, not a production safety benchmark or a statistically representative accuracy study.

## Research status

This project is an independent experimental prototype. The broad problem of multi-turn jailbreak detection and conversational safety monitoring has existing research. Socratic Shield is presented as a specific architecture and experimental implementation, not as a claim that the general idea of multi-turn behavioral detection is entirely new.

## Limitations

The current prototype is small and experimental. Its rule-based behavioral signals, topic detection, knowledge retrieval, and language-model integration can produce false positives, false negatives, classification inconsistencies, or retrieval errors.

The prototype should not be treated as a production-grade security system.

## Author

**Ahsan Mushtaq**  
Independent Researcher, India  
Email: bhattseerat33@gmail.com
