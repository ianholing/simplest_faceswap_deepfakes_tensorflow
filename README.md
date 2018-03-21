# SIMPLEST DEEPFAKES FACESWAP WITH TENSORFLOW
The Simplest version of Deepfakes Faceswap in Tensorflow

I've been looking for a simple implementation in pure tensorflow of this model and I didn't found a clue, so I though of made my own try here.

What I understand about this model is:
* There is two autoencoders sharing the same encoder (Encoder)
* Each autoencoder have it's own decoder (Decoder_A and Decoder_B) which is intended to learn how to draw a different face (In my case Trump and Cage faces)
* When all the system is trained you are able to switch decoders and draw a face of Cage with input of Trump

It's starting to work now, but it looks like a bit underfitting or undertrained. I assume I want to keep it simple, but I think I can get better results without make it much more difficult  [You can check my ATM results in the Jupyter Notebook](https://github.com/ianholing/simplest_faceswap_deepfakes_tensorflow/blob/master/simple_deepfakes_faceswap.ipynb) I expected to improve it soon when I had some time, any help would be appreciated.

![CAGE_TRUMPIFICATED](https://github.com/ianholing/simplest_faceswap_deepfakes_tensorflow/blob/master/git_images/cage_works_0.1.png?raw=true)

![FINAL DATASET 1](git_images/structure.jpg)
