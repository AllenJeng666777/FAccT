# Healthy by Assertion: Auditing Evidence-Judgment Consistency in LLM-Generated Recipes

Code supplement for the paper submitted to ACM FAccT 2027.

## Repository contents

| File | Purpose |
|---|---|
| `script/generate_recipes.py` | Recipe generation script including the full prompt template sent to all six models |
| `src/nutrition/who.py` | WHO-derived seven-criterion scoring |
| `src/nutrition/fsa.py` | FSA-derived composite scoring (fat, saturated fat, sugar, salt per 100 g) |
| `data/meal_list.py` | The 207 meal types used as generation anchors (30 breakfast, 124 dinner, 53 dessert) |
| `requirements.txt` | Python dependencies |

## Prompt

The full prompt is in `script/generate_recipes.py` (lines 188-260). Each call requested one recipe in JSON format with ingredient list, total nutrients, FSA score and category, and WHO score. The prompt named the scoring frameworks but did not supply their complete rubrics, approximating an ordinary consumer request.

