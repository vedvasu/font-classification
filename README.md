# Font Classification
Train a model to classify different fonts by self generating training data

## Steps for training
- Add relevant .ttf files for fonts in the /fonts folder
- Part A - Generate Dataset.ipynb - Generation of dataset
- Part B - Preprocess Dataset.ipynb - Preprocessing of generated images
- Part C - Extract Features.ipynb - Extraction of Image features
- Part D - Train Model and Evaluate.ipynb - Train and evaluate models
- Note: Skin Parts A, B, C if already added data folder in the working directory. 
  - Download Link to trained models

## Steps for prediction
- Add models folder in the working directiory. 
  - Download Link to trained models
- Part E - Predictions Pipeline.ipynb - Predict single image with multiple fonts

## Representation of the training process

![alt text](https://github.com/vedvasu/font-classification/blob/main/pipeline_diagram.jpg)

## Conclusions
- LR performed with 94% precision on the limited distribution of "Hello World text"
- While SVM was 90% precision but was also able to capture font from other phrases
- For the augumented data - LR was 83% precise


## Scope of improvements
- Better data curation: Add data for more phrases to build more training data. Currently experimented with -
  - Hello World
  - Design Lead
  - Co-founder & CEO
- Better preprocessing: Maybe try with resizing image with padding on top and bottom
- Better feature extraction: Experiment with other features extractors trained on Imagenet data
- Better modelling:
  - Hyperparameter optimisations for XGB, SVM
  - Currently, for flattening, maxpooled RESNET features from last layer are used. We can use 3D features from RESNET and train CNNs
  - We can train a good capacity Neural Network (1-3 dense layers + Relu + Softmax) to capture complex patterns