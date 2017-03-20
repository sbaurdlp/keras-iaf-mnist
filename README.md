# keras-iaf-mnist
Implementation of Inverse Autoregressive Flows with Keras

This code is a modified version of https://github.com/fchollet/keras/blob/master/examples/variational_autoencoder.py, trying to include IAF in the model.
IAF is a technique introduced by DP Kingma et al. (see https://arxiv.org/pdf/1606.04934.pdf). It is supposed to give the latent variables a more flexible posterior, improving the modeling power of the model.
I used 2-layered MADE models (see https://arxiv.org/pdf/1502.03509.pdf) as auto-regressive networks.

A part of the loss is evaluated by Monte Carlo estimation

Unfortunately, adding more layers of latent variables makes the performance worse, something may be wrong in the code but I cannot see what
