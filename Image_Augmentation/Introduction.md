### Introduction of Image Augmentation
  Image augmentation in our project is to solve the unevenly distributed datasets. When we collected data, we discovered that images with violation behavious are easier to obtain than those with non-violation behavious. Intuitively, when people are far from animals, they only take photos of animals rather than both animals and themselves. 
  However, in the classifier training, we intend to have evenly distributed data to train a great classifier. If one group is dominated, the classifier tends to classify
the images into the dominated group, which is not optimal. Thus, image augmentation comes in to solve the issue here. We use this technique to rotate, zoom in or out, vertical or horizontal flip to generate more non-violation images to make the data set evenly distributed. 

### Introduction of the folder
The folder contains notebook to illustrate how the image augmentation works. You can change the parameters in the image generator, for example, changing rotation angles, to generate images by yourselves. Also, the folder contains the original non-violation images and some examples of the augmented images we use in our project. 

### File name and corresponding content of each file
Data_Augmentation.ipynb: notebook contains code to perform image augmentation in our project

Image_Augmentation_Examples: folder contains image examples generated by the code in the notebook above.
