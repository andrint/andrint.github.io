# Fingerprint Recognition & Threshold Evaluation

This week I explored fingerprint recognition using classical image processing techniques combined with template matching.
I created a full system for:

- Registering fingerprints via a GUI

- Extracting minutiae and local descriptors

- Comparing fingerprints against a gallery of enrolled samples

- Evaluating performance with metrics like FPR, FNR, and error rate


1. TOC
{:toc}

## Threshold tuning and error rates
I evaluated system performance by comparing several fingerprints and manually labeling which were matches. Using a loop over multiple thresholds (from 0.62 to 0.88), I collected statistics:
| Threshold | FNR   | TP | FP | FN | TN | Error Rate |
|-----------|-------|----|----|----|----|-------------|
| 0.62      | 0.00  | 7  | 56 | 0  | 4  | 0.836       |
| 0.64      | 0.00  | 7  | 51 | 0  | 9  | 0.761       |
| 0.66      | 0.14  | 6  | 45 | 1  | 15 | 0.687       |
| 0.68      | 0.29  | 5  | 40 | 2  | 20 | 0.627       |
| 0.70      | 0.29  | 5  | 28 | 2  | 32 | 0.448       |
| 0.72      | 0.57  | 3  | 17 | 4  | 43 | 0.313       |
| 0.74      | 0.57  | 3  | 5  | 4  | 55 | 0.134       |
| 0.76      | 0.57  | 3  | 0  | 4  | 60 | 0.060       |
| 0.78      | 0.71  | 2  | 0  | 5  | 60 | 0.075       |
| 0.80      | 1.00  | 0  | 0  | 7  | 60 | 0.104       |
| 0.82      | 1.00  | 0  | 0  | 7  | 60 | 0.104       |
| 0.84      | 1.00  | 0  | 0  | 7  | 60 | 0.104       |
| 0.86      | 1.00  | 0  | 0  | 7  | 60 | 0.104       |
| 0.88      | 1.00  | 0  | 0  | 7  | 60 | 0.104       |

