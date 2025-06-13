# CelebA GAN Lab (AIGC5504 Lab 04 & 05)

This project demonstrates training a Generative Adversarial Network (GAN) on the CelebA dataset using TensorFlow and TensorFlow Datasets. The notebook covers data preprocessing, model building, training, and visualization of results.

## Features

- Loads and preprocesses the CelebA dataset.
- Implements a simple DCGAN (Deep Convolutional GAN) with Keras.
- Trains the GAN and visualizes generator/discriminator losses.
- Compares the distribution of real and generated images using PCA.

## Setup

### 1. Environment

We recommend using [Miniconda](https://docs.conda.io/en/latest/miniconda.html):

```bash
conda create -n ganlab python=3.10
conda activate ganlab
pip install tensorflow tensorflow-datasets matplotlib scikit-learn
```

### 2. Download CelebA Dataset

Due to Google Drive download restrictions, you must manually download the CelebA dataset:

- Download `img_align_celeba.zip` from [this link](https://drive.google.com/uc?export=download&id=1_ee_0u7vcNLOfNLegJRHmolfH5ICW-XS).
- Move the file to the TensorFlow Datasets manual directory:

    ```bash
    mkdir -p ~/tensorflow_datasets/downloads/manual/
    mv /path/to/img_align_celeba.zip ~/tensorflow_datasets/downloads/manual/
    ```

- If you use a custom data directory, specify it in your code with the `data_dir` argument in `tfds.load`.

### 3. Running the Notebook

- Open the notebook `lab04and05_MinhNhat_Mai_AIGC5504.ipynb` in VS Code or Jupyter.
- Run all cells to train the GAN and visualize results.

## Usage

- **Training Loss Plot:** After training, the notebook plots generator and discriminator losses per epoch.
- **PCA Visualization:** The notebook compares the distribution of real and generated images in 2D using PCA.

## Notes

- Training GANs can be computationally intensive. Using a GPU is recommended.
- If you encounter issues with dataset loading, ensure the dataset zip is in the correct manual directory.

## License

For academic use