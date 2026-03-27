# Tutorial 01 — Backpropagation Mathematics in Depth

> **The Chain Rule That Trains Every Neural Network**  
> University of Hertfordshire | MLNN Assignment | 2025

---

## What This Tutorial Covers

This tutorial derives **backpropagation from first principles** using the chain rule of calculus. It works through a complete 2-layer MLP by hand, then verifies the result with a numerical gradient check on real **MNIST** (60,000 handwritten digit images).

**You will learn:**
- How the chain rule produces exact weight gradients
- Why softmax + cross-entropy gives such a clean gradient (`ŷ - y`)
- How ReLU's "gate" behaviour affects gradient flow
- How to verify any backprop implementation with a numerical gradient check
- What causes vanishing gradients and why it matters

---

## Files in This Folder

| File | Description |
|------|-------------|
| `backpropagation_tutorial.ipynb` | Full Jupyter notebook with all code, figures, and explanations |
| `backpropagation_tutorial.docx` | PDF tutorial document (under 2000 words) |
| `README.md` | This file |
| `LICENSE` | MIT Licence |

---

## How to Run the Notebook

### Requirements
```bash
pip install numpy matplotlib scikit-learn
```

### Steps
1. Clone or download this repository
2. Open a terminal in this folder
3. Run:
```bash
jupyter notebook backpropagation_tutorial.ipynb
```
4. Run all cells in order (Cell → Run All)

> **Note:** The notebook downloads MNIST automatically via `sklearn.datasets.fetch_openml`. This requires an internet connection on first run (~15MB download). If unavailable, the notebook falls back to synthetic data automatically.

---

## Figures Produced

| Figure | Description |
|--------|-------------|
| `fig1_activations.png` | Activation functions and their derivatives |
| `fig2_gradient_check.png` | Numerical gradient check results |
| `fig3_training_curves.png` | Loss and accuracy over 30 epochs on MNIST |
| `fig4_gradient_heatmaps.png` | Weight gradient magnitude heatmaps |

---

## Accessibility

All figures use:
- **Colourblind-safe palettes** (viridis heatmaps, CB-safe line colours)
- **Solid + dashed line styles** to distinguish series without relying on colour alone
- **Descriptive alt-text captions** in notebook markdown cells
- **Structured headings** (H1/H2/H3) for screen reader navigation

---

## References

1. Rumelhart, D.E., Hinton, G.E. and Williams, R.J. (1986) 'Learning representations by back-propagating errors', *Nature*, 323(6088), pp. 533–536. https://doi.org/10.1038/323533a0  
2. LeCun, Y., Bottou, L., Orr, G.B. and Müller, K.R. (1998) 'Efficient backprop', in *Neural Networks: Tricks of the Trade*. Springer, pp. 9–50.  
3. Goodfellow, I., Bengio, Y. and Courville, A. (2016) *Deep Learning*. MIT Press. https://www.deeplearningbook.org  
4. Baydin, A.G. et al. (2018) 'Automatic differentiation in machine learning: A survey', *JMLR*, 18(153). https://arxiv.org/abs/1502.05767  
5. LeCun, Y., Cortes, C. and Burges, C.J.C. (2010) MNIST handwritten digit database. http://yann.lecun.com/exdb/mnist/  

---

## Licence

This project is licensed under the **MIT Licence** — see [LICENSE](LICENSE) for details.  
You are free to use, modify, and distribute this code with attribution.

---
