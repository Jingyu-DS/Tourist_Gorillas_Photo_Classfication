## Tourist Gorillas Photo Classfication Project
### Team 1: Final Deliverables
#### Authors: Jingyu Wang, Jiarui Fan, Krittika Shahani, Ritesh Kasamsetty

There are several folders created for our implemented techniques and models built following different logics. Each folder contains an introduction file. You could regard the introduction file in each folder as a brief description of the contents of each notebook and their goals. 

### The folders can be referenced following our project logic:

#### Step 1 -> Folder "Image Augmentation": 

In our project, we face unevenly distributed training set. In another word, there are much more images in violation group than in non-violation group. We use data or image augmentation technique to generate more images for non-violation group in order to achieve an unbiased classification results. For further details, please check the introduction and notebook in the folder. 

#### Step 2 -> Folder "Object Detection and Feature Creation": 

After having evenly distributed training set, we use object detection state of arts, a pre-trained object detector EfficientDet-Lite, to detect the objects contained in each image. Those images with object detected would go into different models to train the classifiers. Also, because we are implementing multi-input model which train on non-image features and images at the same time, we also generate some features along the object detection process and store the features in a csv file. If you would like to have a look at our object detection code and feature creation process, please check this folder for more details.

#### Step 3 -> Different Model Implementations: Folders "Individual model", "Multi-input model" and "Ensemble model":

These three folders don't have a sequential order. We are experimenting on the models in parallel. For individual models, we use pre-trained image pre-processing models to train the classifier, such as Inception V3, Resnet, VGG. You could check this folder for more individual model introduction. For multi-input model, it includes the training on non-image features and image features: Multi-layer percpetron on the non-image features and well-performed individual model on image data. The folder contains more details about the implementations and visualization images to explain the model logic. For ensemble model, it combines several great individual models together to generate great results without just relying on an individual model. Similarly, the folder will contain more details. 

In a word, the multi-input model and ensemble model are built on the base of individual models with good performance but follow different logics to further improve or stablize the model. 

The stress testing folder contains all the stress tests we have done. The folder is organized to showcase the stress testing cases for multi-input models and ensemble models separately. Please check there for more details. 
