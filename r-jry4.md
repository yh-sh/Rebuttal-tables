# Supp-tables

## Weakness #1 & Question #1

| **Latency (s)** | **Actor 0.6B** | **Actor 1.7B** | **Actor 4B** | **Actor 8B** | **Solver 14B** |
|---|---:|---:|---:|---:|---:|
| mean | 0.047 | 0.102 | 0.233 | 0.528 | 8.077 to 18.403 |
| p50 | 0.051 | 0.123 | 0.237 | 0.546 | 8.086 to 19.155 |
| p95 | 0.057 | 0.130 | 0.336 | 0.635 | 9.085 to 19.589 |

**Table:** Actor latency across model sizes. Solver latency varies by task.

## Weakness #2 & Question #2

| **Actor** | **Amazon-Beauty HR@10** | **Amazon-Beauty NDCG@10** | **HotpotQA EM** | **HotpotQA F1** |
|---|---:|---:|---:|---:|
| 0.6B | 0.02830 | 0.01521 | 0.593 | 0.721 |
| 1.7B | 0.02877 | 0.01587 | 0.597 | 0.728 |
| 4B | 0.02937 | 0.01620 | 0.606 | 0.741 |
| 8B | 0.02994 | 0.01648 | 0.609 | 0.742 |

**Table:** Actor size vs. performance across all tasks. Solver = Qwen3-14B.

## Weakness #3

| **Method** | **~2K (original)** | **~8K** | **~16K** | **~32K** |
|---|---:|---:|---:|---:|
| MI (EM) | 0.556 | 0.524 | 0.518 | 0.512 |
| HiLight (EM) | 0.606 | 0.550 | 0.542 | 0.532 |
| Δ | +9.0% | +5.0% | +4.6% | +3.9% |
| MI (F1) | 0.706 | 0.683 | 0.675 | 0.656 |
| HiLight (F1) | 0.741 | 0.710 | 0.693 | 0.682 |
| Δ | +5.0% | +4.0% | +2.7% | +4.0% |

**Table:** HotpotQA performance at increasing context lengths. Distractor documents are injected to extend context.





