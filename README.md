# SIMPLEST DEEPFAKES FACESWAP WITH TENSORFLOW
The Simplest version of Deepfakes Faceswap in Tensorflow

I've been looking for a simple implementation in pure tensorflow of this model and I didn't found a clue, so I though of made my own try here.

What I understand about this model is:
* There is two autoencoders sharing the same encoder (Encoder)
* Each autoencoder have it's own decoder (Decoder_A and Decoder_B) which is intended to learn how to draw a different face (In my case Trump and Cage faces)
* When all the system is trained you are able to switch decoders and draw a face of Cage with input of Trump

Is that incorrect?
I made exactly that process in a really simple way, but the problem is that my autoencoders do not learn how to draw faces, instead it looks that they learn how to compress and decompress an image focusing on the colors, So.. [in the last step (when I check the results) of my notebook](https://github.com/ianholing/simplest_faceswap_deepfakes_tensorflow/blob/master/simple_deepfakes_faceswap.ipynb) I expected to see Trump but the same Cage was the output.

![CAGE_NOT_TRUMPIFICATED](https://github.com/ianholing/simplest_faceswap_deepfakes_tensorflow/blob/master/git_images/cage_fail.png?raw=true)

I think Decoder_A and Decoder_B learns the same uncompress way :(

What am I doing wrong? This is a sketch of how it is done:

![FINAL DATASET 1](git_images/structure.jpg)
