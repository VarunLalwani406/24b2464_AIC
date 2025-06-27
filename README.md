# 24b2464_AIC
<br>

<br>
<br>
this project uses a pretrained resnet50 model to classify images from the fashion-mnist dataset
<br>
<br>
Setup steps for local execution :
<br>
1. installing dependencies - pytorch, numpy  , pandas , torchvision  <br>
2. downloading train.csv and test.csv files and place them in the same directory as the notebook<br>
3. run the cells sequentially<br>
<br>
Detailed documentation of analysis, experiments, and final comments :<br>
1. data loading and preprocessing <br>
- loaded csv files into pandas dataframes <br>
- created a custom pytorch dataset to convert flattened image arrays into 28x28 images and transform them into 3-channel rgb images compatible with pretrained resnet50<br>
- applied transformations to resize images to 224x224, normalize pixel values, and convert to tensor <br> <br>
2.model setup : <br>
- loaded pretrained resnet50 with frozen weights <br>
- replaced the final fully connected layer to output 10 classes for fashion-mnist <br>
- later unfroze the last resnet block (layer4) for fine-tuning with a smaller learning rate and learning rate scheduler <br> <br>
3. training and evaluation  <br>
-  trained the model for 5 epochs with frozen backbone, printing loss periodically <br>
- evaluated accuracy on the test set after each epoch <br>
- fine tuned the last resnet block for 3 epochs with adjusted optimizer and learning rate scheduler <br>
- monitored validation accuracy improvements after fine-tuning <br> <br>
4.  final comment <br>
- training on gpu drastically reduced training time  <br> <br> 
references : <br>
1. pytorch  <br>
2. torchvision models   <br>
3. fashion-mnist dataset - https://drive.google.com/drive/folders/1qZNwYOW53GZYZjpmsSpZMBNh1PEQumnb  <br> <br>
error handling <br>
1.verifying csv files are correctly downloaded and in correct paths  <br>
2.interrupt or restart kernel whenever stuck <br>








