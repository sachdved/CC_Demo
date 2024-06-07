This repository is a demo for VAE building for Curious Cirkits.

In order to insall the environment, you'll need to use anaconda, and then run
something like
`conda create --name <env> --file requirements.txt`
in your shell.

During th edemo, I stumbled in a few spots. Critically, the most important fix
I made after the presentation was changing the relative weights of reconstruction loss against ELBO loss. This is necessary, because if the loss on the Gaussian prior is too strong, you experience posterior collapse, and nothing is learned. This is what I was experiencing during the demo.

Feel free to tinker with it as you see fit.

The relevant places to look at:
Original model introduced in: D. Kingma, M. Welling. Autoencoding Variational Bayes. https://arxiv.org/abs/1312.6114
Data is from: X. Lian, N. Prajlak, ..., R. Ranganathan, A. Ferguson. Deep-learning enabled of synthetic orthologs of a signaling protein. https://www.biorxiv.org/content/10.1101/2022.12.21.521443v1

Good luck!
