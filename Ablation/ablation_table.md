| Variant | Params | Params saved | Test acc. (%) | Δ acc. (pp) | Verdict |
|---|---:|---:|---:|---:|---|
| full model | 2,967,228 | — | 95.95 | — | baseline |
| without texture attention | 2,917,254 | 1.7% | 95.91 | -0.05 | no detectable effect |
| without color module | 2,738,334 | 7.7% | 96.18 | +0.23 | no detectable effect |
| without bark pattern convs | 1,436,004 | 51.6% | 96.28 | +0.33 | no detectable effect |
| without mixup cutmix | 2,967,228 | 0.0% | 96.84 | +0.88 | apparent GAIN - verify with seeds |
| without dual pooling | 2,819,772 | 5.0% | 96.79 | +0.84 | apparent GAIN - verify with seeds |