# VideoSR
Video Super-resolution project using CNN and baseline transformer image SR model

When approached naively, video superresolution (SR) can be achieved by having an image SR model and applying the model to each frame of a given video. This method is valid given that each frame fundamentally is an image. However, this approach does not take the temporal relationship between the frames. For example, a frame is a slight permutation of a frame right before (and so on with the recursive definition).

To address this and experiment with approaches to incorporate this temporal relationships, I incorporated another CNN model that runs on previous frames, extract any useful features, and applying the resulting feature vector to the baseline upscaled frames via a fully connected layer.

The dataset used was REDS dataset. The training was done via COLAB PRO+. Please check out the Jupyter notebook for more info.

For this project, I plan on trying out other non-ML approaches from signal processing realm to see if I can observe a better performance.
