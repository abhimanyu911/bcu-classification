# BCU classification



[Standard lightweight NN using bias initialisation](./data_engg_classification.ipynb)



[Agarwal paper](https://iopscience.iop.org/article/10.3847/1538-4357/acbdfa/pdf)


# Best model


Lightweight bias initialised NN with soft voting



# Inference


[How to calculate inference time of a model ?](https://www.thinkautonomous.ai/blog/deep-learning-optimization/#how-to-calculate-the-inference-time-of-a-model)


FLOPs = Floating Point Operations


FLOPS = Floating Point Operations per Second


Agarwal model FLOPs = 2 x 7 x 64 + 2 x 64 x 32 + 2 x 32 x 1 = 5056


Our model FLOPs = 2 x 7 x 42 + 2 x 42 x 1 = 672


GPU FLOPS (GTX 1660 Ti) = 5.4 TFLOPS 


Inference speed = FLOPs/ FLOPS


Agarwal model inference speed = 5056/(5.4 x 10^12) = 936.296 x 10^(-12) = 936.296 pico seconds


Our model inference speed = 672/(5.4 x 10^12) = 124.44 pico seconds
