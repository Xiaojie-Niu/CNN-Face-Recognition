# CNN-Face-Recognition
How to use CNN to recognize human face

## 1 Technology Background

Convolutional Neural Network (CNN) is a feed-forward neural network whose artificial neurons can respond to surrounding units in a part of the coverage area, and has excellent performance for large image processing. It consists of a convolutional layer and a pooling layer.

In the 1960s, Hubel and Wiesel discovered that the unique network structure of the neurons used for local sensitivity and orientation selection in the cat cerebral cortex could effectively reduce the complexity of the feedback neural network, and then proposed the Convolutional Neural Networks (CNN). Neural Networks (CNN for short). Nowadays, CNN has become one of the research hotspots in many scientific fields, especially in the field of pattern classification, where the network has been more widely used because it avoids complex pre-processing of images and can be directly input to the original images. The new recognition machine proposed by K. Fukushima in 1980 was the first implementation network of convolutional neural network. Subsequently, more researchers have improved the network. One of the representative research results is the "Improved Cognitive Machine" proposed by Alexander and Taylor, which combines the advantages of various improved methods and avoids the time-consuming error back propagation.

In general, the basic structure of CNN consists of two layers, one is the feature extraction layer, where the input of each neuron is connected to the local receptive domain of the previous layer and the local features are extracted. Once the local feature is extracted, the position relationship between it and other features is determined; the second is the feature mapping layer, where each computational layer of the network consists of multiple feature mappings, each of which is a plane with equal weights for all neurons on the plane. The feature mapping structure uses a sigmoid function with a small influence function kernel as the activation function of the convolutional network, which makes the feature mapping displacement invariant. In addition, the number of free parameters of the network is reduced because the neurons on a mapping plane share the weights. Each convolutional layer in the CNN is followed by a computational layer for local averaging and quadratic extraction, which reduces the feature resolution with the unique two-feature extraction structure.

CNNs are mainly used to recognize 2D graphics with displacement, scaling and other forms of distortion invariance. Since the feature detection layer of CNN learns through the training data, the displayed feature extraction is avoided when using CNN, and learning is done implicitly from the training data; furthermore, since the neurons on the same feature mapping surface have the same weights, the network can learn in parallel, which is a major advantage of convolutional networks over networks with neurons connected to each other. Convolutional neural network has a unique superiority in speech recognition and image processing with its special structure of local weight sharing, and its layout is closer to the actual biological neural network, and the weight sharing reduces the complexity of the network, especially the feature that images with multidimensional input vectors can be directly input to the network avoids the complexity of data reconstruction in the process of feature extraction and classification.

<img width="413" alt="image" src="https://user-images.githubusercontent.com/114042177/191447769-5425f6b7-49bf-4a6a-b422-ce5bfe91f141.png">

## 2 Technology Introduction
For the four PY files used in this experiment and their main functions are shown in the following table.

File name | Code amount | Program function
:---: | :---: |:---: 
get_my_faces.py | 67 lines | Turn on the camera to capture pictures of myself and save them to a local folder.
set_other_people.py | 50 lines | capturing a collection of images of other people's faces from a website and processing them.
train_faces.py | 173 lines| training the model using the convolutional neural network algorithm.
is_my_face.py |176 lines| calls the trained model for recognition.

The non-standard Python libraries used in this experiment are described below (open the command line and type pip install * to install them, where * is the name of the corresponding library.)

Python non-standard library name | Role
:---: | :---:
Tensorflow |deep learning library, open source by Google, can automatically derive functions defined on a Tensor (tensor)
Dlib |face recognition library, this experiment mainly uses its face alignment algorithm
Numpy |matrix library, which can handle matrix operations flexibly and avoid complex loop operations
Opencv |C++ library, used for real-time processing of computer vision problems, with two Python interfaces
Sklearn| machine learning algorithm library

Due to the time rush, there is no time to do the graphical interface, the order of each PY file execution is get_my_faces.py, set_other_people.py, train_faces.py, is_my_face.py.

Since this CNN model requires a large number of samples for training, the following are the individual samples and the time required for acquisition.

Sample | Number |Time
:---: | :---: |:---: 
My face set |10,000 images |1 hour or so
Other people's face image set |13,989 images |30 minutes or so
Convolution training process| --- | about 30 minutes

The final trained model has a correct recognition rate of 98% or more.

Reference: Zheng Zeyu and Gu Siyu "TensorFlow Practical Google Deep Learning Framework(郑泽宇、顾思宇《TensorFlow实战Google深度学习框架》)

Running environment introduction
This program uses Python 3.6.4 in Windows 10 environment for experimentation, and Sublime Text3 is used for editing software; the configuration of Python environment is not discussed here. The program will be executed in the above order and the final result will be judged.
