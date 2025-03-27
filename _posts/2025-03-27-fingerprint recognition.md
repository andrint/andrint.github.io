# Fingerprint Recognition & Threshold Evaluation

This week I explored fingerprint recognition using classical image processing techniques combined with template matching.
I created a full system for:

- Registering fingerprints via a GUI

- Extracting minutiae and local descriptors

- Comparing fingerprints against a gallery of enrolled samples

- Evaluating performance with metrics like FPR, FNR, and error rate


1. TOC
{:toc}

## Threshold tuning 

<details> <summary>Click to expand raw threshold statistics</summary>
Threshold: 0.62 | FNR: 0.00 | TP: 7 | FP: 56 | FN: 0 | TN: 4 | Error Rate: 0.836
Threshold: 0.64 | FNR: 0.00 | TP: 7 | FP: 51 | FN: 0 | TN: 9 | Error Rate: 0.761
Threshold: 0.66 | FNR: 0.14 | TP: 6 | FP: 45 | FN: 1 | TN: 15 | Error Rate: 0.687
Threshold: 0.68 | FNR: 0.29 | TP: 5 | FP: 40 | FN: 2 | TN: 20 | Error Rate: 0.627
Threshold: 0.70 | FNR: 0.29 | TP: 5 | FP: 28 | FN: 2 | TN: 32 | Error Rate: 0.448
Threshold: 0.72 | FNR: 0.57 | TP: 3 | FP: 17 | FN: 4 | TN: 43 | Error Rate: 0.313
Threshold: 0.74 | FNR: 0.57 | TP: 3 | FP: 5  | FN: 4 | TN: 55 | Error Rate: 0.134
Threshold: 0.76 | FNR: 0.57 | TP: 3 | FP: 0  | FN: 4 | TN: 60 | Error Rate: 0.060
Threshold: 0.78 | FNR: 0.71 | TP: 2 | FP: 0  | FN: 5 | TN: 60 | Error Rate: 0.075
Threshold: 0.80 | FNR: 1.00 | TP: 0 | FP: 0  | FN: 7 | TN: 60 | Error Rate: 0.104
Threshold: 0.82 | FNR: 1.00 | TP: 0 | FP: 0  | FN: 7 | TN: 60 | Error Rate: 0.104
Threshold: 0.84 | FNR: 1.00 | TP: 0 | FP: 0  | FN: 7 | TN: 60 | Error Rate: 0.104
Threshold: 0.86 | FNR: 1.00 | TP: 0 | FP: 0  | FN: 7 | TN: 60 | Error Rate: 0.104
Threshold: 0.88 | FNR: 1.00 | TP: 0 | FP: 0  | FN: 7 | TN: 60 | Error Rate: 0.104
</details>

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

