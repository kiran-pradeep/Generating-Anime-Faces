# Generating-Anime-Faces

Trained a Variational Autoencoder (VAE) using the [anime faces dataset by MckInsey666](https://github.com/bchao1/Anime-Face-Dataset).
VAE follow an encoder-decoder architecture and can be summarized by the figure below.

<img src="https://drive.google.com/uc?export=view&id=1YAZAeMGEJ1KgieYk1ju-S9DoshpMREeC" width="60%" height="60%"/>

A custom Sampling layer to provide the Gaussian noise input along with the mean (mu) and standard deviation (sigma) of the encoder's output. The equation to combine these:

<img src="https://render.githubusercontent.com/render/math?math=z = \mu + e^{0.5\sigma} * \epsilon">

where <img src="https://render.githubusercontent.com/render/math?math=\mu"> = mean, <img src="https://render.githubusercontent.com/render/math?math=\sigma"> = standard deviation, and <img src="https://render.githubusercontent.com/render/math?math=\epsilon"> = random sample

Output from the encoider layer is fed to the `Sampling layer` . That will have the latent representations that is then fed to the decoder network later.
