# Ensemble CNN Classification with Data Augmentation

Simple ensemble with data augmentation that achieves about **95% classification accuracy** with test data. 
Each model takes about 5 minutes to train with these parameters, so you can train about 12 models in an hour to achieve 95% accuracy. Set nModels to the desired number of models.

* Data source: [FashionMNIST](https://research.zalando.com/welcome/mission/research-projects/fashion-mnist/)

* Contains a training set of 60,000 examples and a test set of 10,000 examples.

* Each example is a 28x28 grayscale image, associated with a label from 10 classes:

|Label|	Description   |
|:----:|  :----:      |
|0	  |T-shirt/top    |
|1	  |Trouser        |
|2	  |Pullover       |
|3	  |Dress          |    
|4	  |Coat           |
|5	  |Sandal         |
|6	  |Shirt          |
|7	  |Sneaker        |
|8	  |Bag            |
|9	  |Ankle boot     |


A convolution neural network (CNN) with judiciously selected architecture and parameters may achieve a classification accuracy of around 92% with test examples. 
This [notebook](https://github.com/GSukr/Ensemble_CNN_Classification_with_Data_Augmentation/blob/master/FMimageClassification.ipynb) investigates some simple mechanisms to improve classification accuracy. Specifically, it explores whether:

* **Data augmentation** by distorting training images (using ImageDataGenerator) helps with generalization, and
* An **ensemble** of similar CNN models does better than its constituent models.

Aggregate class probabilties of the constituent models for prediction. Trained models are saved and may be used to investigate alternate ensemble mechanisms.
