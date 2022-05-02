### Purpose of doing stress tesing
Most of our models have the potential to achieve high performance on pure gorilla images. Then, we start thinking about whether the model can be generalized into other scenarios or can be used as a special model for distance detecting and measuring. 

### Components of stress testing
There are two main logics implementing stress testing: The first one is via transfer learning. The second one is to train on other data set directly and do the testing following the same logic. 

### Via transfer learning
The model will be trained on pure gorilla images and validated on pure gorilla images. The testing is performed on the gorilla images as well as images of other animal categories. In our cases, we have tested on giraffe, real lion and tiger, panda, elephant. Through the process, we have discovered there is some level of generlization of our model on the animals which are more similar to gorilla, for example, the body structure or size. When the animal is too different from gorilla, the model cannot perform well.

### Via training directly
We have taken the photos by using the lion statue on campus for the stress testing usage. We trained on the lion statue images directly, validates using the images taken with the lion statues and tested on those images as well. The model performs quite well. 

### About the popular topic -- human distancing
We also tried to apply the method to detect the violation in human distancing images. For this stress testing case, we first use the transfer learning, but the model cannot perform well. Then, we retrain the model by adding several human distancing images to train together. The performance has been increased a lot. This can show, to some extent, the model can be generelized but probably not via transfer learning. Instead, when those images can be trained together, the model can perform well. 
