# MODEL DEPLOYMENT DEMONSTRATION
- We used ResNet-50 v1.5 https://huggingface.co/microsoft/resnet-50 pretrained model to get the inference.
- ResNet model pre-trained on ImageNet-1k at resolution 224x224. It was introduced in the paper Deep Residual Learning for Image Recognition by He et al.
- This is a image classification model using resnet-50 backbone.
- The output of this application is the form of string displaying the class/es of detected objects in the image.
- Model is used to classify an image of the COCO 2017 dataset into one of the 1,000 ImageNet classes.

Execution:
- Create a conda environment using following command:
  `conda create -n <Your Conda Env Name> python=3.8`

- activate your env using:
  `conda activate <Your Conda Env Name>`
- install ipykernal package using command:
  `pip install ipykernel`

- Direct to folder /MDD/app and open jupyter notebook "image_classification.ipynb".
- Make sure your Linux-64 supports docker, docker-compose, and curl command.
- Check the terminal path from your application(e.g., jupyter notebook, vscode) to make sure your
  working directory is /MDD/app.
- Execute all the cells in "image_classification.ipynb" file one by one. This notebook will create
  docker and containers for nginx and python application.
- To send a request and get response from python application, open "send_request.ipynb" file and run cells one by one. This file uses a CURL request to process your image and return the name of detected classes.
- ResNet (Residual Network) is a convolutional neural network that democratized the concepts of residual learning and skip connections. This enables to train much deeper models. Also, it is trained on a million images of 1000 categories from the ImageNet database. Supporting 1000 classes increase the chance of getting a closer class detection to the real category of object.
