#### Purpose of performing stress tesing on multi-input model
Multi-input model with Inception V3 has achieved outstanding results on pure gorilla images. The stress testing is to make sure the model has the potential to be generalized into more scenarios.

#### Introduction of stress testing
For the stress testing on multi-input model, we use campus statue images and mixed data which contains both gorilla images and campus statue images to figure out whether the model can be generalized. 

Then, we would like to add more stress on the model: We add several images for other animal categories into the testing data and implement the tranfer learning to see whether the model works to detect the violation or non-violation correctly. The animal categories we use are real tiger and lion, giraffe, panda and elephant for this model. More details about the stress testing resutls would be shown in the folder as well. 

Also, we add human distancing images to perform the same task described. Then, we add several human-distancing images to the training dataset to see whether the model can be enhanced. 
