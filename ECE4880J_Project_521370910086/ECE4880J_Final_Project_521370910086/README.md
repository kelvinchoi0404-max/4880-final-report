# ECE4880J Final Project Submission

**Title:** A ResNet-18 Baseline Study of Distortion-Aware Training for Robust AI-Generated Image Detection  
**Author:** Junxuan Cai  
**Student ID:** 521370910086  
**Course:** ECE4880J Computer Vision  

## Submission files

- `main.pdf`: compiled IEEE-style final report.
- `main.tex`: LaTeX source.
- `references.bib`: bibliography used by the report.
- `figures/`: vector figures referenced by `main.tex`.
- `evidence/`: CSV exports behind the numerical tables and plots.

The report is seven pages including references. It contains seven figures,
four tables, and 17 cited research references.

## Experimental scope

The study uses 27,643 labeled source images from official NTIRE 2026 training
shard 5. The baseline is an ImageNet-pretrained ResNet-18 trained with crop,
flip, and color augmentation. The controlled comparison keeps the model,
source split, loss, optimizer, schedule, checkpoint rule, and evaluation sets
fixed, then adds JPEG compression, Gaussian blur, and Gaussian noise during
distortion-aware training.

Across seeds 42, 43, and 44, distortion-aware training increases pooled
transformed ROC AUC by 0.95 percentage points and reduces the
clean-to-transformed gap by 1.74 points, with a 0.79-point reduction in clean
AUC. Generator identities are absent from the shard labels, so the reported
evaluation concerns post-processing shift rather than held-out generators.

## Compilation

Upload the folder or ZIP directly to Overleaf, or compile locally with:

```text
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Tectonic can compile the project with:

```text
tectonic main.tex
```
