# Self Driving Car (End to End CNN/Dave-2)

* Used convolutional neural networks (CNN) to map the raw pixels from a front-facing camera to the steering commands for a self-driving car. This powerful end-to-end approach means that with minimum training data from humans, the system learns to steer, with or without lane markings, on both local roads and highways. The system can also operate in areas with unclear visual guidance such as parking lots or unpaved roads.
* The system is trained to automatically learn the internal representations of necessary processing steps, such as detecting useful road features, with only the human steering angle as the training signal. We do not need to explicitly trained it to detect, for example, the outline of roads.
* End-to-end learning leads to better performance and smaller systems. Better performance results because the internal components self-optimize to maximize overall system performance, instead of optimizing human-selected intermediate criteria, e. g., lane detection. Such criteria understandably are selected for ease of human interpretation which doesn’t automatically guarantee maximum system performance. Smaller networks are possible because the system learns to solve the problem with the minimal number of processing steps.

### Conclusions from the paper
* This demonstrated that CNN are able to learn the entire task of lane and road following without manual decomposition into road or lane marking detection, semantic abstraction, path planning, and control.The system learns for example to detect the outline of a road without the need of explicit labels during training. 
* A small amount of training data from less than a hundred hours of driving was sufficient to train the car to operate in diverse conditions, on highways, local and residential roads in sunny, cloudy, and rainy conditions. 
* The CNN is able to learn meaningful road features from a very sparse training signal (steering alone).
* More work is needed to improve the robustness of the network, to find methods to verify the robust- ness, and to improve visualization of the network-internal processing steps.

### Demo
![alt img](./self_driving_car_gif.gif)<br>

### How to Use
Download Dataset: [https://drive.google.com/file/d/0B-KJCaaF7elleG1RbzVPZWV4Tlk/view]
Size: 25 minutes = 25{min} x 60{1 min = 60 sec} x 30{fps} = 45,000 images (45,569 images) ~ 2.3 GB

Few more samples can be downloaded from [here](http://data.apollo.auto/?locale=en-us&lang=en)

Even you can run without training using the pretrained model by running below commands

Use `python3 train.py`   --- To train the model

Use `python3 run.py`     --- To run the model

Use `python3 run_dataset.py`   --- To run the model on the dataset

For visualizing training dataset, using Tensorboard use `tensorboard --logdir=./logs`, then open http://0.0.0.0:6006/ into your web browser.


Article for reference:
<b>A TensorFlow/Keras implementation of this [Nvidia paper](https://arxiv.org/pdf/1604.07316.pdf) with many changes.</b>

