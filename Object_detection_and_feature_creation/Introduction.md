### Introduction of Object Detection
In order to train the classifier, we have put some constraints on the images used: we require the images to contain animals and people at the same time. Thus, the first thing we have done is to detect the objects in the images to make sure the animal and person can both be detected in each image. The state of art we have implemented is EfficientDet-Lite which is a pre-trained object detector. This is trained on COCO 2017 eval set and achieves mAP 41.5. There is definitely other state of art that can achieve even better result on the same data, but EfficientDet-Lite has provided pretty good results in our case to locate the animals and people in the images. After detecting, green rectangles will be used to denote where objects are in each image. Finally, those images with objects detected would go into the model to train the classifier. 

### Feature Creation in Object Dectection Process
In some images, there can be more than one person and more than one animal in the image. In another word, there is more than one pair of person and animal. However, we would like to focus on the pair of person and animal with the closest distance. Thus, we think about soome informative features that can be trained along with the image data. When objects are being detected, the rectangles are generated. For each rectangle, it is possible to get the width, length, centroids or mid-points of sides for each rectangle. Then, during the detection, we generata a dataframe to contain those features and save as csv files for the potential use in the model. 

### Logics of Models
There are two main logics of models we have implemented. The first type model only trains on the image data (seen in the individual model folder and ensemble model folder). So after getting the images with object detected, those models can be trained using only the images. The second type model trains on the non-image features and image data at the same time and generate results together (seen in multi-input model folder). In a word, not all models we have implemented have used the csv files containing non-image features. 

###  Brief Introduction of Files in the Folder

