# BCU classification



[Standard lightweight NN using bias initialisation](./data_engg_classification.ipynb)



[Agarwal paper](https://iopscience.iop.org/article/10.3847/1538-4357/acbdfa/pdf)


# Model ranks


1) Lightweight bias initialised NN with soft voting (7/8 metrics outperformed when comparing with mean values of Agarwal NN; missclass rate: 7%, F1: 93.0)


2) Supervised greedy pretraining (6/8 metrics outperformed when comparing with mean values of Agarwal NN; missclass rate: 8.5%, F1: 91.7)


3) Unsupervised greedy pretraining(3/8 metrics outperformed when comparing with mean values of Agarwal NN; missclass rate: 11.4%, F1: 88.7, AUC: 95.56)


4) Self Supervised Learning(3/8 metrics outperformed when comparing with mean values of Agarwal NN; missclass rate: 11.4%, F1: 88.7, AUC: 95.37)



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
