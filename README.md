## RNN VAE

This is a straightforward implementation of "Generating Sentences from a Continuous Space", mostly as a baseline/reference.
Actually, it's a checkpoint from a few weeks ago, and likely not very useful to the wider community, but the reason to open
source it is for `data.py`, which builds on `torchtext` and supplies `seq2seq` iterators for use in language modeling. 

NOTE: the iterators work correctly, but are not very efficient - in particular it would be useful to cache the text processing
for larger datasets and save to an HDF5 file. I'll do that later and merge upstream.

Unfortunately, I think there's some hyperparameter magic necessary to reproduce the results exactly, and I don't have 
enough GPU time to do it at the moment. 

Based on the framework of https://github.com/salesforce/awd-lstm-lm

### Bibliography
Bowman, Samuel R., et al. "Generating sentences from a continuous space." arXiv preprint arXiv:1511.06349 (2015).
