# 24b2464_AIC
<br>
this project uses a pretrained resnet50 model to classify images from the fashion-mnist dataset
<br>
<br>
Setup steps for local execution
<br>
1. installing dependencies - pytorch, numpy  , pandas , torchvision  <br>
2. downloading train.csv and test.csv files and place them in the same directory as the notebook<br>
3. run the cells sequentially<br>
<br>
Detailed documentation of analysis, experiments, and final comments <br>
1. data loading and preprocessing <br>
- loaded csv files into pandas dataframes <br>
- created a custom pytorch dataset to convert flattened image arrays into 28x28 images and transform them into 3-channel rgb images compatible with pretrained resnet50<br>
- applied transformations to resize images to 224x224, normalize pixel values, and convert to tensor <br>
2.

