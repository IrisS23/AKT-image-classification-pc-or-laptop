# Laptop or PC

Using tensorflow a classifier should be created that can categorize images as either laptops or PCs.

## Docker
- Navigate to main directory of the repository
- Run command:  
`docker run -it --rm -v ${PWD}:/home/jovyan/work -p 8888:8888 jupyter/tensorflow-notebook`


(docker image `tensorflow/tensorflow:latest-jupyter` does not work because `scipy` is not installed)

## Tests
### What happens when the learning-rate is increased/decreased?
TODO

## What happens when layers are added/removed?
TODO

## What happens when parameters from the ImageDataGenerator are changed?
TODO

## Examples

### Loss And Accuracy

test_loss, test_accuracy = model.evaluate(x_test,  y_test, verbose=2)
print('\nTest accuracy:', test_accuracy)

### ROC-Curve

tf.keras.metrics.AUC(
    num_thresholds=200, curve='ROC', summation_method='interpolation', name=None,
    dtype=None, thresholds=None, multi_label=False, label_weights=None
)

Source:
https://www.tensorflow.org/api_docs/python/tf/keras/metrics/AUC
