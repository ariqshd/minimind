# MiniMind Study Plan

Personal study branch: `study/progress-tracker`
Fork: `ariqshd/minimind` · Original: `jingyaogong/minimind`

## Goal

Build a tiny chat AI from scratch and understand every step. Follow the
project in order: read the code → run the model → train it → improve it.

## Progress tracker

### Stage 0 — Setup
- [x] Fork the repo and clone to `D:\minimind`
- [x] Create study branch `study/progress-tracker`
- [x] Install dependencies: `pip install -r requirements.txt`
- [x] Check GPU is seen: `python -c "import torch; print(torch.cuda.is_available())"`

### Stage 1 — Just run it
- [x] Download the ready-made model into `./minimind-3`
- [x] Chat in the terminal: `python eval_llm.py --load_from ./minimind-3`
- [x] Open the web chat: `cd scripts && streamlit run web_demo.py`
- [x] Write down 3 things the model does well and 3 things it gets wrong

### Stage 2 — Read the code
- [ ] `model/model_minimind.py` — how the model is built
- [ ] `model/tokenizer.json` — how text is split into pieces
- [ ] `trainer/trainer_utils.py` — shared training helpers
- [ ] `eval_llm.py` — how answers are generated

### Stage 3 — Train it yourself
- [ ] Download `pretrain_t2t_mini.jsonl` and `sft_t2t_mini.jsonl` into `./dataset`
- [ ] Teach it language: `python trainer/train_pretrain.py`
- [ ] Teach it to follow instructions: `python trainer/train_full_sft.py`
- [ ] Try the small-change method: `python trainer/train_lora.py`
- [ ] Practice saving and resuming with `--from_resume 1`

### Stage 4 — Make it better
- [ ] Learn from preferences: `trainer/train_dpo.py`
- [ ] Learn from feedback: `trainer/train_ppo.py`, `train_grpo.py`
- [ ] Teach it to use tools: `trainer/train_agent.py`
- [ ] Shrink a bigger model into it: `trainer/train_distillation.py`

### Stage 5 — Share it
- [ ] Run the OpenAI-style server: `python scripts/serve_openai_api.py`
- [ ] Test tool calls: `python scripts/eval_toolcall.py`
- [ ] Compare with others: C-Eval, C-MMLU, OpenBookQA
- [ ] Write a short summary of what was learned

## Study log

| Date | Stage | What I did | What I learned | Next |
| --- | --- | --- | --- | --- |
| 2026-11-25 | 0 | Forked, cloned to `D:\minimind`, created branch | Repo has `trainer/`, `model/`, `scripts/`, `dataset/` | Install dependencies |

## Notes

Add discoveries, command quirks, and "aha" moments here.

## Useful commands

```bash
git status                         # see what changed
git add STUDY_PLAN.md && git commit -m "study: update progress"
git push -u origin study/progress-tracker
git fetch upstream                  # get original repo updates
```
