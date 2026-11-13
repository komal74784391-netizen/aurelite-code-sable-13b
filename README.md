# Sable-13B — Official Code Release

**Accepted at NeurIPS 2025.** Official training, evaluation and inference code for Sable-13B.

This repository contains the complete training, evaluation and inference code that was
used to produce the results reported in the paper. Weights are released under Apache-2.0.

## Repository layout

- `src/model.py` — reference model implementation
- `src/train.py` — training loop and config loader
- `data/prepare.py` — corpus preparation utilities
- `experiments/base.yaml` — reference training configuration
- `notebooks/quickstart.ipynb` — end-to-end inference demo
- `results/metrics.json` — benchmark numbers from the paper
- `tests/test_smoke.py` — smoke tests
- `requirements.txt` — runtime dependencies

## Quick start

```bash
pip install -r requirements.txt
python -m src.train --config experiments/base.yaml --steps 200
```

## Reported metrics

```json
{
  "hellaswag": 81.9,
  "longbench": 41.2,
  "mmlu": 64.8
}
```

## Citation

```bibtex
@inproceedings{aurelite2025sable13b,
  title={Sable-13B: Long Context Without the Long Wait},
  author={Aurelite Labs},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2025}
}
```
