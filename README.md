# explore-guardrails

Evaluates Llama Guard 3 (8B) against a binary safe/unsafe test set.

## Setup

1. Request access to `meta-llama/Llama-Guard-3-8B` on Hugging Face (gated by Meta)
2. Create a HF token at `huggingface.co/settings/tokens` and run `huggingface-cli login`
3. Install dependencies: `pip install -r requirements.txt`
4. Update `DATA_PATH` in the notebook to point to your test set

## Run

Open `llama_guard.ipynb` and run all cells top to bottom.
Results save live to `results_llama_guard.csv` as inference runs.

## Notes
- GPU strongly recommended, CPU inference is very slow for 8B model
- 403 error = HF access still pending Meta approval
- AttributeError on input_ids = run `pip install accelerate` and restart kernel