This repository is a demo for VAE building for Curious Cirkits.

In order to insall the environment, you'll need to use anaconda, and then run
something like
`conda create --name <env> --file requirements.txt`
in your shell.

During th edemo, I stumbled in a few spots. Critically, the most important fix
I made after the presentation was changing the relative weights of reconstruction loss against ELBO loss. This is necessary, because if the loss on the Gaussian prior is too strong, you experience posterior collapse, and nothing is learned. This is what I was experiencing during the demo.

Feel free to tinker with it as you see fit.