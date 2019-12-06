# LCA
Duke BME590 Final Project

Loss Change Allocation (LCA) was originally developed by Uber Research (paper: https://arxiv.org/pdf/1909.01440.pdf) as a mechanism to further understand model training. Specifically, LCA allows for per-parameter loss calculations, which can then be used by the researcher to tune their model training. More information is explained in this blog post by Uber Engineering: https://eng.uber.com/loss-change-allocation/

In this repository, we decided to replicate the LCA methodology on a simple FC 3 layer network trained on the MNIST digits dataset. For visualizations, we adapted the original code from the Uber Research team, which can be found here: https://github.com/uber-research/loss-change-allocation

[Slides](https://docs.google.com/presentation/d/1b3tWjkX3cKYalAdXrvfazeShByDK8hFO_5wyzRToxwc/edit?usp=sharing)

Colab Links:

[MNIST LCA](https://colab.research.google.com/drive/1b5KCRToeyCA2Mg45V1iimZfd8D75Un-x)
