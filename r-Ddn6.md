# Supp-tables

## Weakness 2


| **Setting** | **Qwen3-8B HR@10** | **Qwen3-8B NDCG@10** | **Qwen3-4B HR@10** | **Qwen3-4B NDCG@10** |
|---|---:|---:|---:|---:|
| MI baseline | 0.02312 | 0.01343 | 0.02144 | 0.01262 |
| Transfer | 0.02628 | 0.01510 | 0.02424 | 0.01369 |
| Δ_% | +13.67% | +12.43% | +13.06% | +8.48% |

**Table:** Cross-Solver transfer on Amazon-Beauty. Actor trained with Qwen3-14B and evaluated against each target Solver's own MI baseline.

## Weakness #4 & Question Q2


| **Task** | **Training Reward** $R(y, y^*)$ |
|---|---|
| Amazon-Beauty | $0.7 \times \text{HR@10} + 0.3 \times \text{NDCG@10}$ |
| HotpotQA | $0.5 \times F1 + 0.5 \times EM$ |
| SQuAD 2.0 | $0.5 \times F1 + 0.5 \times EM$ |
| PubMedQA | Accuracy (Yes/No/Maybe) |

## Weakness #5 & Questions Q3, Q4


| **Method** | **~2K (original)** | **~8K** | **~16K** | **~32K** |
|---|---:|---:|---:|---:|
| MI (EM) | 0.556 | 0.524 | 0.518 | 0.512 |
| HiLight (EM) | 0.606 | 0.550 | 0.542 | 0.532 |
| Δ | +9.0% | +5.0% | +4.6% | +3.9% |
| MI (F1) | 0.706 | 0.683 | 0.675 | 0.656 |
| HiLight (F1) | 0.741 | 0.710 | 0.693 | 0.682 |
| Δ | +5.0% | +4.0% | +2.7% | +4.0% |

**Table:** HotpotQA performance at increasing context lengths. Distractor documents injected to extend context.

| **Width** | **Greedy-TopK HR@10** | **Greedy-TopK NDCG@10** | **Softmax HR@10** | **Softmax NDCG@10** | **Gumbel-TopK HR@10** | **Gumbel-TopK NDCG@10** |
|---:|---:|---:|---:|---:|---:|---:|
| 4  | 0.0271 | 0.0150 | 0.0271 | 0.0147 | 0.0266 | 0.0147 |
| 6  | 0.0270 | 0.0152 | 0.0273 | 0.0150 | 0.0270 | 0.0152 |
| 8  | 0.0283 | 0.0157 | 0.0277 | 0.0153 | 0.0273 | 0.0152 |
| 10 | 0.0287 | 0.0158 | 0.0282 | 0.0155 | 0.0270 | 0.0150 |
| 12 | 0.0281 | 0.0158 | 0.0260 | 0.0149 | 0.0275 | 0.0153 |
| 14 | 0.0271 | 0.0154 | 0.0267 | 0.0150 | 0.0283 | 0.0152 |
| 16 | 0.0273 | 0.0155 | 0.0266 | 0.0149 | 0.0276 | 0.0154 |

**Table:** Span-coalescence width / gap-threshold and sampling-method ablation on Amazon-Beauty.

| $\lambda_{\text{len}}$ | $\beta_{\text{ent}}$ | **HR@10** | **NDCG@10** |
|---:|---:|---:|---:|
| 0.0   | 1.0 | 0.0267 | 0.0149 |
| 0.001 | 1.0 | 0.0271 | 0.0153 |
| 0.005 | 1.0 | 0.0284 | 0.0152 |
| 0.01  | 1.0 | 0.0287 | 0.0157 |
| 0.01  | 0.5 | 0.0276 | 0.0153 |
| 0.01  | 0.1 | 0.0278 | 0.0156 |
| 0.01  | 0.0 | 0.0268 | 0.0149 |

**Table:** Loss-coefficient ablation on Amazon-Beauty.

## Weakness #7

| **Actor Size** | **Precision** | **Recall** | **F1** |
|---|---:|---:|---:|
| 0.6B | 0.7275 | 0.6433 | 0.6828 |
| 1.7B | 0.7964 | 0.7016 | 0.7460 |
| 4B | 0.8367 | 0.7215 | 0.7748 |
| 8B | 0.8403 | 0.7307 | 0.7817 |

**Table:** Token-level overlap between Actor highlights and ground-truth supporting facts on HotpotQA (threshold = 0.5).

| **Actor** | **Amazon-Beauty HR@10** | **Amazon-Beauty NDCG@10** | **HotpotQA EM** | **HotpotQA F1** |
|---|---:|---:|---:|---:|
| 0.6B | 0.02830 | 0.01521 | 0.593 | 0.721 |
| 1.7B | 0.02877 | 0.01587 | 0.597 | 0.728 |
| 4B | 0.02937 | 0.01620 | 0.606 | 0.741 |
| 8B | 0.02994 | 0.01648 | 0.609 | 0.742 |

**Table:** Actor size vs. performance across all tasks. Solver = Qwen3-14B.



