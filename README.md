# playground

The goal of this repo is to design a neual network (encoder-decoder model) which input is a series of image frames from surveillance video, and the network should be able do the following:  
  1 learn a global map knwoledge through the encode process.  
  2 the decode should be able to generate a global background map throught upsampleing & deconvolution.  
  3 the network should be able to give a relate location on for each input frame.  

An interesting doing puzzle network maybe the ideal solution to the problem above. The series of input frames could be viewed as the pieces of puzzle, and the output is a full view of the assambled picture, as well as an anchor point or coordinates for each image pieces in the picture. From the describtion of this network, we can image that the problem is hard at the start, and it may gets easier and easier as we mapped more pieces to the whole picture, just as when human doing the puzzle. However there is one additional infomation with the inpput - the images coordinates are usually continuous. Given these facts, a transformer or RNN network with attention layer may suit for this problem. 

Based on current popular nlp models, such as BERT, a simliar model can be proposed.  
