1. Which strategy won, and on what dimension? (Accuracy?Parse rate? Cost?)
CONCISE was the top performer for accuracy (mean = 1.0) and also had the highest judge score in the run (20.0). Parse rate was 1.0 for all strategies under the course JSON-parse rule; costs were all micro-sized and similar, with CONCISE slightly lower in total cost.

2. What surprised you? Either a strategy worked better thanexpected, or worse, or a specific snippet failed in a wayyou didn't predict.
Parse success was uniformly high (parse_success = 1.0) once we required only JSON-parseability after stripping fences, which made judge scores and accuracy the main discriminators. Also, a small rounding choice (.round(3)) originally hid real per-call costs — increasing to .round(6) revealed micro-cost differences.

3. For *your* capstone domain, which strategy would you reachfor first? Justify in 2-3 sentences.
I would start with an EXPLICIT_JSON prompt (clear system instruction + minimal schema). It minimizes downstream parsing/validation work, forces consistent keys and nulls for missing fields, and is easy to extend with a couple of targeted few-shot examples for edge cases.

4. If you had another day, what would you try next? (Differentmodel? More snippets? Different prompts?)
Add more and more diverse snippets (edge cases) and run the extraction with a stronger model or with carefully tuned few-shot examples; normalize or re-prompt the judge to a fixed 1–4 rubric and re-evaluate; persist SCORED and rerun analyses for statistical stability.