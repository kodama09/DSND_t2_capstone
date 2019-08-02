# Dog Breed Identification

## Project Description
The purpose of this project is to create a neural net, specifically a Convolutional Neural Net, which is capable of differentiating between different breeds of dogs. This neural net is to live within an image processing pipeline which will accept an image as an input, determine if it contains humans and/or dogs, and if the image contains either a human or a dog it will attempt to guess the closest match of dog breed. For a dog this means guessing its breed, for a human this means guessing what kind of dog they resemble.

## Methods
Human face recognition is performed using the opencv3 library, and dog recognition is performed using keras's built-in ResNet50 network with weights trained on imagenet. Training, validation, and test images of 133 unique dog breeds were provided by Udacity.

Several methods were tested for dog breed recognition.
1. Entirely custom CNN architecture (trivial solution)
2. Dense Network built on Bottleneck features from keras models
3. Keras built-in model with custom dense output layers, trained on augmented image data

**[Full Description](https://medium.com/p/22d8ed0b16c5/edit)**

## Files
**dog-project**
├── **bottleneck_features**
. . . . . └── < empty > *(bottleneck features, downloaded)*
├── **dogImages**
. . . . . ├── **train**
. . . . . . . . . . └── *(training images)*
. . . . . ├── **test**
. . . . . . . . . . └── *(testing images)*
. . . . . └── **valid**
. . . . . . . . . . └── *(validation images)*
├── **haarcascades**
. . . . . └── haarcascade_frontalface_alt.xml *(opencv3 pretained params)*
├── **lfw**
. . . . . └── *(opencv3 face recognition testing images)*
├── **requirements** *(not used)*
├── **saved_models**
. . . . . └── weights.best.groundup_5.hdf5 *(augmented image pretrained params)*
├── dog_app.ipynb *(primary working file)*
├── dog_app.html *(html printout of similar ipynb)*
├── dog_breeds.yml *(conda environment)*
└── README.md *(you're reading it!)*

## Usage
In order to recreate the experiments I perform in dog_app.ipynb, you will need to recreate my conda environment using the 'dog_breeds.yml' file.

Requirements include:
+ tensorflow-gpu
+ jupyter
+ glob2
+ scikit-learn
+ keras
+ matplotlib
+ opencv
+ tqdm
+ pillow
+ seaborn

Testing just the final model is possible by running the import cell at the top, then some of the functions at the bottom which initialize a model and read in my pretrained parameters
