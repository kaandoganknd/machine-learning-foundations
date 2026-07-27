# Data Notes

No raw image or CSV data is stored or redistributed in this repository.

## Digit CSV Files

The supplied local files contain:

- `train.csv`: 42,000 labelled rows with `label` plus `pixel0`–`pixel783`.
- `test.csv`: 28,000 unlabelled rows with `pixel0`–`pixel783`.

Both files have pixel values from 0 to 255 and no missing values. Their schema matches the
common Kaggle Digit Recognizer format. Because original download provenance and redistribution
rights were not supplied, the files remain local.

## Fashion-MNIST

Fashion-MNIST is loaded through TensorFlow/Keras and contains 60,000 training images and
10,000 test images across 10 clothing classes.

## References

- [Kaggle Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer)
- [Keras Fashion-MNIST loader](https://keras.io/api/datasets/fashion_mnist/)
- [TensorFlow CNN tutorial](https://www.tensorflow.org/tutorials/images/cnn)
