| Version | Accuracy | Macro-F1 |
|---|---|---|
| v1: poora abstract | 0.673 | 0.664 |
| v2: MiniLM top-3 | 0.636 | 0.635 |
| Fine-tuned + MiniLM top-3 | 0.676 | 0.672 |
| Fine-tuned + CE top-1 | 0.691 | 0.633 |
| Fine-tuned + CE top-2 | 0.733 | 0.716 |

Note: sab 450 validation pairs par, single run.
## Clean run (validation, 450 pairs, single run)

| top-k | Accuracy | Macro-F1 | NOINFO recall |
|---|---|---|---|
| 1 | 0.684 | 0.619 | 0.268 |
| 2 | 0.698 | 0.686 | 0.741 |
| 3 | 0.636 | 0.640 | 0.946 |

## Threshold experiment (held-out half B, ~225 pairs)

| Method | Macro-F1 | Accuracy |
|---|---|---|
| Fixed top-2 | 0.670 | 0.696 |
| Score threshold (t = -3) | 0.716 | 0.737 |

Notes: reranker AUC (evidence vs NOINFO) = 0.893. Threshold chosen on half A, measured on half B.
Single run, validation only. Not yet measured on test set.