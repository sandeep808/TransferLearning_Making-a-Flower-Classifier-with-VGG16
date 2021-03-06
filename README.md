# TransferLearning_Making-a-Flower-Classifier-with-VGG16

Transfer Learning A Definition :

“Transfer learning and domain adaptation refer to the situation where what has been learned in one setting … is exploited to improve generalization in another setting”

Fine Tuning : 

● The concept of Fine Tuning is often and justifiably confused with Transfer Learning. However it is merely a type of Transfer Learning.
● Fine Tuning is where we take a pre-trained Deep CNN (ResNet50, Inception or VGG) and use the already trained (typically on ImageNet) Convolutional Layers to aid our new image classification task. Typically in fine tuning we are taking an already trained CNN and training it on our new dataset
● We then either Freeze these lower layers, and train the top or FC layers only. Sometimes we do go back and train the lower layers to improve our performance.
● In most deep CNN’s the first few CONV layers learn low level features (example color blobs) and as we progress through the network, it learns more mid/high level features or patterns.
● In Fine Tuning we keep or Freeze these trained low level features, and only train our high level features needed for our new image classification problem.

Transfer Learning : 

● As we’ve done in Fine Tuning, we have taken a pre-trained network and trained it (or segments/layers of it) on some new data for a new image classification task. (it doesn’t have to be new data or a new goal, Fine Tuning simply implies we further train an already trained network).
● Transfer Learning, is almost the same thing and is often used interchangeably with Fine Tuning.
● Transfer Learning though implies we are taking the ‘knowledge’ learned from a pre-trained network and applying to a similar task and therefore not re-training the network.


Flowers-17 Dataset : 
● Flowers-17 was created by the University of Oxford’s Visual Geometry Group at the Department of Engineering.
● It consists of 17 categories of flowers commonly found in the UK.
● There was 80 images of each flower in this dataset


Our Approach : 
● Use a pre-trained VGG16 with all it’s weights except the top layer frozen
● We only train the Fully Connected (FC) or Dense layers, with a final output of 17
