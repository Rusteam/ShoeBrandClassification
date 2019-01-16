# Shoe Brand Recognition Convolutional Neural Net

_Jan 5, 2018_

``Goal:`` This classification model was build simply to learn how pyTorch works.

``Result:`` Best result was achieved using a pre-trained DenseNet121 with a modified fully-connected layer. Top-1 accuracy after training for {} epochs is **{}%** (although with noticeable overfit). The training took {} minutes on 1 Tesla P100 gpu.

### Data

Dataset consists of real shoe images for 14 brand categories.
There were 6161 images in total. After removing invalid and spliting into train/test folders, there are 5722 and 413 images, respectively.
[Download link](https://drive.google.com/file/d/0B05wqMLeCbG-blZpVTlEZWQ3NWs/view)

##### Image samples
![alt text](./Images/274-puma.jpg 'Puma')
![alt text](./Images/12-converse.jpg 'Converse')
![alt text](./Images/180-newbalance.jpg 'New Balance')

### Convnet

##### Architecture

A pre-trained DenseNet121 beat other models. One classification layer was added to match the number of classes in the shoes dataset.

##### Training

Cross-entropy loss was selected as a loss function and Adam was used to optimize weights and biases.

##### Results

86% validation accuracy was achieved after 10 epochs. Training accuracy reached 95%.

### Further improvements

- Add Dropout layer to fight overfit
- Continue training for more epochs
- Try cyclical learning rate