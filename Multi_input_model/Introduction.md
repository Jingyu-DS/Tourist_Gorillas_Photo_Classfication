### Description of Multi-input Model
When performing the object detection on images, we have rectangles bounded around the objects in the images. For those rectangles, it is possible to get the four coordinates. We are interested on the animal and human pair with the closest distance. Thus, when obtaining the features, we have two main targets of the interests, which means we get the features from only two rectangles bounding the pair with the closest distance.

After getting those coordinates, more features can be further generated. For example, width, length and area of rectangles, the centroid coordinates of rectangles, pixel distance between the centroids. Some of them can be valuable in training the classifier because they have the potential to provide useful information.

The multi-input model is trained on image data and non-image data features at the same time. Before training, we use feature selection method, RFE, to select the most significant features related to the image label in advance. The most important parameter we need to decide is the number of features we would like to train on. This is tested by several trials to find the most optimal number.

Then, we start the training process. The multi-layer perceptron is trained on non-image features. Well-performed image processing pre-trained models are trained on image data. None of them generates the final prediction at this time. In another word, we stop them before the final several layers and then concatenate the layers to generate the final predictions.

This folder is created to store all the experienments done by using multi input logic. Multi-input model, compared to the individual models, further improves the model performance and reduces the overfitting issue as well.

### Introduction of File Content in the Folder
The files overall are about the gorrila image datasets, gorilla feature csv files and notebook with code included.

Multi_input_with_inception_model_try_Feature_Selection_Multi_input_classifier.ipynb: notebook contains code for multi-input model using data introduced below

Violation-training-detected(-continued): folders of images for training in violation group

Violation-validation-detected: folder of images for validation for violation group

Violation-testing-detected: folder of images for testing for violation group

Non-violation-training-detected(-continued): folders of images for training for non-violation group

Non-violation-validation-detected: folder of images for validation for non-violation group

Non-violation-testing-detected: folder of images for testing for non-violation group

Violation-training.csv: CSV file of features for training in violation group

Violation-validation.csv: CSV file of features for validation in violation group

Violation-testing.csv: CSV file of features for testing in violation group

Non-violation-training.csv: CSV file of features for training in non-violation group

Non-violation-validation.csv: CSV file of features for validation in non-violation group

Non-violation-testing.csv: CSV file of features for testing in non-violation group

### Purpose of performing stress tesing on multi-input model
Multi-input model with Inception V3 has achieved outstanding results on pure gorilla images. The stress testing is to make sure the model has the potential to be generalized into more scenarios.

### Introduction of stress testing
For the stress testing on multi-input model, we use campus statue images and mixed data which contains both gorilla images and campus statue images to figure out whether the model can be generalized.

Then, we would like to add more stress on the model: We add several images for other animal categories into the testing data and implement the tranfer learning to see whether the model works to detect the violation or non-violation correctly. The animal categories we use are real tiger and lion, giraffe, panda and elephant for this model. More details about the stress testing resutls would be shown in the folder as well.

Also, we add human distancing images to perform the same task described. Then, we add several human-distancing images to the training dataset to see whether the model can be enhanced.


