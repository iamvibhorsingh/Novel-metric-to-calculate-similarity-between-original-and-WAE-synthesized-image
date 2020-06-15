## Requirements

- Python 3.x (tested with Python 3.6)
- TensorFlow v1.x (tested with 1.8)
- tqdm (for the progress bar) 

## Doing it yourself

### Training
Just run this command
```
python main.py
```

### How to run Inference 

Open the `MNIST Plot.ipynb` with Jupyter Notebook/Lab.

A pretrained model for MNIST is included in the repository [here](https://github.com/iamvibhorsingh/Novel-metric-to-calculate-similarity-between-original-and-WAE-synthesized-image/tree/master/assets/pretrained_models/mnist).
Please download the zip file and decompress it on `assets/pretrained_models/celeba/last*`. Or, you can easily modify a path at the first cell on the notebook.

## Results

### MNIST

- Learning statistics
  ![learning_stat](/assets/learning_stat.png)
- Reconstruction Results
  ![recon](/assets/recon.png)
  (top): original images from MNIST validation set, (bottom): reconstructed image
- As can be seen in the MNIST jupyter notebook, our novel implementation of quasi-euclidean metric gives a similarity score of 1 to WAE-MMD synthesized images and the ground truth (original) image. It is justifiable since WAE-MMD do a very well job at synthesizing MNIST data especially since the images only have a few amount of pixels as well as not a lot of features that the model has to recognize. 
- Random Sampled Images
  ![random_sample](/assets/random_sample.png)

## Acknowledgement

- The original TF implementation [link](https://github.com/tolstikhin/wae)
