# Laptop or PC

Using tensorflow a classifier should be created that can categorize images as either laptops or PCs.

## Docker
- Navigate to main directory of the repository
- Run command:  
`docker run -it --rm -v ${PWD}:/home/jovyan/work -p 8888:8888 jupyter/tensorflow-notebook`


(docker image `tensorflow/tensorflow:latest-jupyter` does not work because `scipy` is not installed)

## Tests
## What happens when layers are added/removed?
Three different models were tested with different layers: The model with 8 layers always performed best: 
```
 {'loss': 0.3668879568576813, 'accuracy': 0.8818181753158569}
True Negatives:  41.0
True Positives:  28.0
False Negatives:  19.0
False Positives:  22.0
AUC:  0.6232692
```

From the current run the model with 6 layers performs second-best and the model with 10 layers performs worst. But in different runs the results were fliped and the model with 10 layers performed better. Therfore we cannot really say which layer-configuration is better suited for this problem.

## What happens if an ImageGenerator is used?
With the image-generator we were not able to achive an accuracy > 0.5. 

## How to different optimizer and loss functions perform?
### Adam and SparseCategoricalCrossentropy
```
 {'loss': 0.3475894629955292, 'accuracy': 0.8727272748947144}
True Negatives:  25.0
True Positives:  25.0
False Negatives:  35.0
False Positives:  25.0
AUC:  0.4583333
```
### Adam and MSE
```
 {'loss': 0.18702112138271332, 'accuracy': 0.8636363744735718}
True Negatives:  33.0
True Positives:  26.0
False Negatives:  27.0
False Positives:  24.0
AUC:  0.5347567
```

### SGD and CategoricalHinge
```
 {'loss': 0.3111439347267151, 'accuracy': 0.8818181753158569}
True Negatives:  35.0
True Positives:  28.0
False Negatives:  25.0
False Positives:  22.0
AUC:  0.57116854
```

### Adadelta and SparseCategoricalCrossentropy
```
 {'loss': 0.5709546804428101, 'accuracy': 0.8818181753158569}
True Negatives:  32.0
True Positives:  25.0
False Negatives:  28.0
False Positives:  25.0
AUC:  0.5165508
```
