# Intriguing Properties of Contrastive Losses paper
[![DOI](https://zenodo.org/badge/doi/10.5281/zenodo.8173662.svg)](https://zenodo.org/record/8173662)
Re-implementation of Intriguing Properties of Contrastive Losses [paper](https://proceedings.neurips.cc/paper/2021/hash/628f16b29939d1b060af49f66ae0f7f8-Abstract.html).

## Getting Started
- Download imagenette [here](https://github.com/fastai/imagenette) (click Full Size download) 

### Environment

#### Anaconda

```
conda create -n re-intriguing-properties pip
conda activate re-intriguing-properties
conda install -c anaconda jupyter
pip install -r requirements.txt
```

### Install the package

```
pip install -e .
```

## Experiments
### Linear Evaluation of SimCLR
[simclr-lineval.ipynb](https://github.com/mona251/Intriguing-Properties-of-Contrastive-Losses/blob/main/simclr-lineval.ipynb) performs the linear evaluation of SimCLR with specified number of epochs, batch size, and number of layers of the projection head. 

### SimCLR learns local features that exhibit hierarchical properties
- [raw_pixels.ipynb](https://github.com/mona251/Intriguing-Properties-of-Contrastive-Losses/blob/main/scripts/hierarchical_properties/raw_pixels.ipynb) visualizes the clustered pixels of raw input images.
- [simclr.ipynb](https://github.com/mona251/Intriguing-Properties-of-Contrastive-Losses/blob/main/simclr.ipynb) extracts features from block group 1, 2, 3, and 4 of SimCLR's base encoder. The extracted features can be then used in the following two Jupyter notebooks:
  - [simclr_different_blocks.ipynb](https://github.com/mona251/Intriguing-Properties-of-Contrastive-Losses/blob/main/scripts/hierarchical_properties/simclr_different_blocks.ipynb) shows SimCLR's learned features on single input images and that the learning of local features is also achieved with other clustering methods.
  - [simclr_different_blocks_batch.ipynb](https://github.com/mona251/Intriguing-Properties-of-Contrastive-Losses/blob/main/scripts/hierarchical_properties/simclr_different_blocks_batch.ipynb) shows SimCLR's learned features on batches of input images.

## Generating additional data
[scripts/data_generation/](https://github.com/mona251/Intriguing-Properties-of-Contrastive-Losses/tree/main/scripts/data_generation) contains Jupyter notebooks that  reproduce the construction of two out of three datasets of the original [paper](https://proceedings.neurips.cc/paper/2021/hash/628f16b29939d1b060af49f66ae0f7f8-Abstract.html) with explicit and controllable competing features that can be used to reproduce the
other experiments of the original work that we did not replicate.
