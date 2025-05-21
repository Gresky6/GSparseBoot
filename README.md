
# GSparseBoot <img src="https://www.r-project.org/logo/Rlogo.png" align="right" height="50" />

**Bootstrap Stability Assessment for Sparse Tensor Models**

`GSparseBoot` is an R package developed to evaluate the stability of sparse tensor decomposition models using bootstrap resampling techniques. It implements Elastic Net penalized Tucker decompositions and includes tools for fitting, resampling, support analysis, and visualization.

> 📦 Developed as part of a doctoral research project at the University of Salamanca.

---

## 🔧 Installation

The package is currently in development. To install from GitHub (once uploaded), use:

```r
# install.packages("devtools")
devtools::install_github("your-user-name/GSparseBoot")
```

---

## 📘 Features

- Penalized Tucker decomposition using Elastic Net
- Classical, residual, and parametric bootstrap
- Variable selection frequency, Jaccard index, support variance
- Visual tools: heatmaps and inclusion frequency plots
- Compatible with both simulated and real multidimensional datasets

---

## 🚀 Example Workflow

```r
# Load example tensor
load("data/sample_tensor_data.rda")

# Fit Elastic Net penalized Tucker model
fit <- elastic_net_tensor(tensor_data, lambda1 = 0.1, lambda2 = 0.05)

# Run bootstrap resampling
boot_results <- bootstrap_tensor(tensor_data, method = "tucker.enet", B = 100)

# Compute stability metrics
metrics <- stability_metrics(boot_results)

# Visualize results
plot_heatmap_support(metrics)
plot_frequency(metrics)
```

---

## 📂 Package Structure

- `R/`: Main source functions
- `data/`: Example datasets
- `man/`: Function documentation
- `vignettes/`: Full reproducible tutorial

---

## 📄 License

This package is distributed under the **GPL-3** license.

---

## ✉️ Contact

For questions, suggestions, or collaborations:

**Gresky Gutiérrez**  
Doctoral Candidate in Multivariate Statistics  
📧 greskygutierrez@usal.es

---

## 🧪 Status

The package is fully functional, validated on simulated and real datasets, and in the process of being deployed to GitHub and CRAN.
