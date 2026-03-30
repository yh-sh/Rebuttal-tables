# Supp-tables

## Weakness 4

| **Mode** | **Amazon-Beauty** | **HotpotQA** |
|---|---:|---:|
| Total success cases (MI Incorrect → HiLight correct) | 168 | 63 |
| Total failure cases (MI correct → HiLight incorrect) | 28 | 20 |
| Total test samples | 1000 | 1000 |

**Table:** Failure-case breakdown for instances where HiLight changes a correct MI prediction into an incorrect one, compared with the success cases.

| **Actor Size** | **Precision** | **Recall** | **F1** |
|---|---:|---:|---:|
| 0.6B | 0.7275 | 0.6433 | 0.6828 |
| 1.7B | 0.7964 | 0.7016 | 0.7460 |
| 4B | 0.8367 | 0.7215 | 0.7748 |
| 8B | 0.8403 | 0.7307 | 0.7817 |

**Table:** Token-level overlap between Actor highlights and ground-truth supporting facts on HotpotQA.