<h1 align="center">Joint Velocity-Growth Flow Matching for Single-Cell Dynamics Modeling (NeurIPS 2025)</h1>

<div align="center">

[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/pdf/2505.13413)

</div>

## Introduction

Learning the underlying dynamics of single cells from snapshot data has gained increasing attention in scientific and machine learning research. The destructive measurement technique and cell proliferation/death result in unpaired and unbalanced data between snapshots, making the learning of the underlying dynamics challenging. In this paper, we propose joint Velocity-Growth Flow Matching (VGFM), a novel paradigm that jointly learns state transition and mass growth of single-cell populations via flow matching. VGFM builds an ideal single-cell dynamics containing velocity of state and growth of mass, driven by a presented two-period dynamic understanding of the static semi-relaxed optimal transport, a mathematical tool that seeks the coupling between unpaired and unbalanced data. To enable practical usage, we approximate the ideal dynamics using neural networks, forming our joint velocity and growth matching framework. A distribution fitting loss is also employed in VGFM to further improve the fitting performance for snapshot data. Extensive experimental results on both synthetic and real datasets.

![Overview](figs/overview.png)

## How to use

Follow the steps below to set up and run VGFM locally.

1. Clone this repository

```vim
git clone https://github.com/DongyiWang-66/VGFM.git
```

2. Create a new conda environment (VGFM) using

```vim
conda create -n VGFM python=3.10 ipykernel -y
conda activate VGFM
```

3. Install requirements

```vim
cd path_to_VGFM
pip install -r requirements.txt
```

## Datasets

All datasets used in this project are publicly available. The files in the `/data` directory have been uniformly processed and converted to CSV format for consistency and ease of use.

For the 2000-dimensional pancreas dataset:

- **Source**: Download `GSE132188_adata.h5ad.h5` from [NCBI GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE132188)
- **Preprocessing**: Follow the data processing pipeline in `notebooks/preprocess_pancreas.ipynb` to reproduce the formatted dataset.

## Tutorials

We currently provide the following tutorials, which can be easily followed in the `notebooks` directory:

- Simulation gene data
- Dyngen
- Gaussian 1000D
- Mouse hematopoiesis
- Hold-out experiments for EB 5D, CITE 5D, and CITE 50D
- EB 50D
- Pancreas 2000D dataset (gene space) and deeper analysis

These notebooks demonstrate how to reproduce our main experiments and can serve as practical starting points for applying VGFM to new datasets.

## Contact

If you encounter any problems or have questions about VGFM, feel free to reach out to **Dongyi Wang** at [dongyiwang@stu.xjtu.edu.cn](mailto:dongyiwang@stu.xjtu.edu.cn).

## Citation

If you find VGFM helpful for your research, please consider citing our work:

```bibtex
@inproceedings{
wang2025joint,
title={Joint Velocity-Growth Flow Matching for Single-Cell Dynamics Modeling},
author={Dongyi Wang and Yuanwei Jiang and Zhenyi Zhang and Xiang Gu and Peijie Zhou and Jian Sun},
booktitle={NeurIPS},
year={2025}
}
```

## Acknowledgments

This project has greatly benefited from the following open-source repositories. We extend our sincere gratitude to the authors and contributors for sharing their valuable work:

- [DeepRUOT](https://github.com/zhenyiizhang/DeepRUOT)
- [conditional-flow-matching](https://github.com/atong01/conditional-flow-matching)
- [MIOFlow](https://github.com/KrishnaswamyLab/MIOFlow)
