# BCU classification


A collection of approaches to classify unidentified samples in the 4LAC-DR3 catalog with the help of Machine Learning.


# Web app installation 


```
git clone https://github.com/abhimanyu911/bcu-classification.git
pip install -r app/requirements.txt
streamlit run app/app.py
```


[Our deployed model](./data_engg_classification.ipynb)



[Agarwal et al - additional reference](https://iopscience.iop.org/article/10.3847/1538-4357/acbdfa/pdf)



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



# Web app Demo (AWS)


![](./aws_bcu_app.gif)


[AWS link](http://13.239.10.157:8501/)


[Streamlit link](https://bcu-classification-ml.streamlit.app/)

# Results


[results notebook](./plotting.ipynb)


# Please cite the manuscript incase you happen to use any of our code

[Manuscript](https://academic.oup.com/mnras/article/528/1/976/7512220)


```
@article{10.1093/mnras/stae028,
    author = {Bhatta, Gopal and Gharat, Sarvesh and Borthakur, Abhimanyu and Kumar, Aman},
    title = "{Gamma-ray blazar classification using machine learning with advanced weight initialization and self-supervised learning techniques}",
    journal = {Monthly Notices of the Royal Astronomical Society},
    volume = {528},
    number = {1},
    pages = {976-986},
    year = {2024},
    month = {01},
    abstract = "{Machine learning has emerged as a powerful tool in the field of gamma-ray astrophysics. The algorithms can distinguish between different source types, such as blazars and pulsars, and help uncover new insights into the high-energy universe. The Large Area Telescope onboard the Fermi gamma-ray telescope has significantly advanced our understanding of the Universe. The instrument has detected a large number of gamma-ray-emitting sources, among which a significant number of objects have been identified as active galactic nuclei. The sample is primarily composed of blazars; however, more than one-third of these sources are either of an unknown class or lack a definite association with a low-energy counterpart. In this work, we employ multiple machine learning algorithms to classify the sources based on their other physical properties. In particular, we utilized smart initialization techniques and self-supervised learning for classifying blazars into BL Lacertae (BL Lac, also BLL) objects and flat-spectrum radio quasars (FSRQs). The core advantage of the algorithm is its simplicity, usage of minimum number of features and easy deployment due to lesser number of parameters without compromising on the performance along with increase in inference speed (at least seven times more than existing algorithms). As a result, the best-performing model is deployed on multiple platforms so that any user irrespective of their coding background can use the tool. The model predicts that out of the 1115 sources of uncertain type in the 4FGL-DR3 catalogue, 820 can be classified as BL Lacs and 295 can be classified as FSRQs.}",
    issn = {0035-8711},
    doi = {10.1093/mnras/stae028},
    url = {https://doi.org/10.1093/mnras/stae028},
    eprint = {https://academic.oup.com/mnras/article-pdf/528/1/976/56334707/stae028.pdf},
}
```