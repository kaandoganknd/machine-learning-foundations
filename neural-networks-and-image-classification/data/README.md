# Data Notes

No raw image files are stored or redistributed in this project.

## Datasets

The notebook loads two documented datasets through TensorFlow/Keras:

- MNIST: 60,000 training images and 10,000 test images of handwritten digits, each 28 x 28
  pixels in greyscale.
- CIFAR-10: 50,000 training images and 10,000 test images across 10 classes, each 32 x 32
  pixels with three colour channels.

MNIST uses a reproducible 50,000/10,000 train-validation split. To keep the CIFAR-10 baseline
practical on CPU-only hardware, a stratified subset of 6,000 training and 1,000 validation
images is selected from its 50,000-image training pool. Both official 10,000-image test
partitions remain untouched until final evaluation.

## References

- [TensorFlow Datasets: MNIST](https://www.tensorflow.org/datasets/catalog/mnist)
- [TensorFlow Datasets: CIFAR-10](https://www.tensorflow.org/datasets/catalog/cifar10)
- [Keras MNIST loader](https://keras.io/api/datasets/mnist/)
- [Keras CIFAR-10 loader](https://keras.io/api/datasets/cifar10/)

The first run downloads the datasets to the user's local Keras cache. Dataset licensing and
source information should be checked through the linked official documentation before any
redistribution or commercial use.
