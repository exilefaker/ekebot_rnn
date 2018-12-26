# ekebot_rnn

Minimal files necessary to sample from the VGL language model

Main code is a slightly modified version of the Tensorflow implementation of char-ran:
https://github.com/sherjilozair/char-rnn-tensorflow/blob/master/model.py

So, requires tensorflow and numpy; also uses six

# model.py
Defines a neural network model and sample function based on stored data

# load_to_sample.py
Loads the model stored in save/ekelogs using load_model(args), where args are command line arguments (this is set up to use the defaults)

Contains a function sample(model, sess, chars, vocab, args) that samples from the loaded model, using the values obtained from load_model

# example

Running load_to_sample.py should load the model and produce a sample:

```
>>> execfile('load_to_sample.py')
2018-12-26 10:15:34.050694: I tensorflow/core/platform/cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA
INFO:tensorflow:Restoring parameters from save/ekelogs/model.ckpt-411

RyuYaStoat:	>>
Lord BBH:	@:)  Wha? ~ __
RyuYaStoat:	::^:)  Y_A=:
RyuYaStoat:	Want.
Kuru:	he were KoF 96 put it, but what's presentally arcade it tez
Lord BBH:	Have many Periodast fav too
MARIO26604:	and don't you give more thing :)
CyberVMage:	I liked I male, just for NOT yet!
Kuru:	LOL..the chance gades you send an work..
Kuru:	WaNg,Lab
Kuru:	Good do the unish
RyuYaStoat:	Feally... there's There!
RyuYaStoat:	So play Cuper?
Rukes Kewl:	Can't some thing pbus, and such this word for 
```

You can then sample again using
```
>>> sample(model, sess, chars, vocab, args)
```

