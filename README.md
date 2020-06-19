# playground

The goal of this repo is to design a neual network (encoder-decoder model) which input is a series of image frames from surveillance video, and the network should be able do the following:
1 learn a global map knwoledge through the encode process.
2 the decode should be able to generate a global background map throught upsampleing & deconvolution.
3 the network should be able to give a relate location on for each input frame.
