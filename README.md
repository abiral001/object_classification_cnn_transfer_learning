## Object Detection Comparison between multiple main stream models

# Steps to Reproduce

1. Take your train and test images and place it into the root directory of this project. 
    The folder structure should be the one shown below:
    
        --- 01-classify.ipynb
         |- 02-final-test.ipynb
         |- test_images/
         |          |- test-images/
         |          |       |- images ... (.jpg)
         |- train_images/
         |          |- train-images/
         |          |       |- images ... (.jpg)
         |- models/
         |- inet/
         |- rnet/
         |- enet/
         |- train-labels.csv
    

2. Install the python packages mentioned in requirements.txt either through pip directly or using virtual environment (recommended)
3. Run the classify.ipynb for generating the model using each of the algorithm (each of the algorithm should be commented out before runnning another one)
   The Trained model will have each of its checkpoint saved inside the /models/ folder. Copy the final model into the respective model folder (inet for Inception Net, rnet for ResNet50 and enet for Efficient Net) [NOTE: the model is trained using train set and validation set generated through the images inside train_images]
4. Run the final-test.ipynb to test the images from the folder test_images. The predictions are saved in the root directory as predictions.pt as a sequence of categories sequentially corresponding to the test-files sorted by ascending order.

This file content will also be placed inside the classify.ipynb file for instructions.
