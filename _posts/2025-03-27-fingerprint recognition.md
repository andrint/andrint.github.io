# Fingerprint Recognition & Threshold Evaluation

This week I explored fingerprint recognition using classical image processing techniques combined with template matching.
I created a full system for:

- Registering fingerprints via a GUI

- Extracting minutiae and local descriptors

- Comparing fingerprints against a gallery of enrolled samples

- Evaluating performance with metrics like FPR, FNR, and error rate

- Fingerprint data was collected [here](http://bias.csr.unibo.it/fvc2000/download.asp)
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


## Plotting ROC curve and FNR and FPR
I plotted the error rate, false positive rate (FPR), and false negative rate (FNR) against the threshold:

![](/images/ErrorRate_vs_threshold.png "Error rate vs threshold")
![](/images/FNR_FPR.png "fast.ai's logo")
<details>
<summary>🧠 What is False Negative Rate (FNR)?</summary>
The False Negative Rate is the proportion of actual positives that were incorrectly predicted as negatives. It helps measure how many real matches the system misses.
</details>
<details>
<summary>🧠 What is False Positive Rate (FPR)?</summary>
The False Positive Rate is the proportion of actual negatives that were incorrectly predicted as negatives. 
</details>

From this, I found that while the error rate looks low at higher thresholds, the FNR increases to 100%, which means all true matches are missed.
    💡**Lesson learned** Accuracy is not enough — you must inspect FPR/FNR trade-offs.

## Observations 
- Performance varied depending on the fingerprint being tested.

- At thresholds ~0.70–0.76, I observed a balanced compromise between FPR and FNR.

- With just 80 samples, tuning is limited — more data would improve robustness.
## Basic formatting

You can use *italics*, **bold**, `code font text`, and create [links](https://www.markdownguide.org/cheat-sheet/). Here's a footnote [^1]. Here's a horizontal rule:

---

## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![](/images/logo.png "fast.ai's logo")

## Code

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |

## Footnotes

[^1]: This is the footnote.

