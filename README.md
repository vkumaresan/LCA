# LCA
Duke BME590 Final Project

Loss Change Allocation (LCA) was originally developed by Uber Research (paper: https://arxiv.org/pdf/1909.01440.pdf) as a mechanism to further understand model training. Specifically, LCA allows for per-parameter loss calculations, which can then be used by the researcher to tune their model training. More information is explained in this blog post by Uber Engineering: https://eng.uber.com/loss-change-allocation/

We decided to replicate the LCA methodology on a simple FC 3 layer network. We trained this network both on the MNIST digits dataset and the [APTOS 2019 Diabetic Retinopathy dataset](https://www.kaggle.com/c/aptos2019-blindness-detection/overview). For visualizations, we adapted the original code from the Uber Research team, which can be found here: https://github.com/uber-research/loss-change-allocation

This repository contains Jupyter notebooks for the MNIST testing (LCA_MNIST.ipynb) and for the Diabetic Retinopathy testing (LCA_DR.ipynb). All visualizations can be found in these notebooks, as well as in the slides linked below.

We also wanted to create a Tensorboard wrapper for LCA, allowing anyone to plug in some simple code and visualize LCA for their model. While this remains a future task, we were able to integrate our MNIST visualizations as images within Tensorboard.

![overall_tensorboard](/images/overall_tensorboard.png)

With our current workflow, we separate the visualizations by layer so that the user can choose which layer they want to dig deeper into. In the future, we would like to automate this process so that the code can automatically run and separate the LCA visualizations for each layer in the specified model. 

![layer_in_detail](/images/layer_in_detail.png)

Clicking on a layer will drill down further into the relevant LCA visualizations for that layer. For now, these include Percent Helped histograms and LCA Trajectory by Neuron. 

![layer_image_in_detail](/images/layer_image_in_detail.png)

Clicking on an image will bring it to full size. These visualizations can serve as a guiding tool for researchers to modify their model training, allowing them to adjust layers and parameters and visualize how those changes affect model performance. 


[Slides](https://docs.google.com/presentation/d/1b3tWjkX3cKYalAdXrvfazeShByDK8hFO_5wyzRToxwc/edit?usp=sharing)

Colab Links:

[LCA_MNIST](https://colab.research.google.com/drive/1b5KCRToeyCA2Mg45V1iimZfd8D75Un-x)

[LCA_DR](https://colab.research.google.com/github/drwitt/BME_590_Tensorflow_Deep_Learning/blob/master/DR_LCA_application_version.ipynb)
