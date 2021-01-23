# playground

The goal of this repo is to design a neual network (encoder-decoder model) which input is a series of image frames from surveillance video, and the network should be able do the following:  
  1 learn a global map knwoledge through the encode process.  
  2 the decode should be able to generate a global background map throught upsampleing & deconvolution.  
  3 the network should be able to give a relate location on for each input frame.  

An interesting doing puzzle network maybe the ideal solution to the problem above. The series of input frames could be viewed as the pieces of puzzle, and the output is a full view of the assambled picture, as well as an anchor point or coordinates for each image pieces in the picture. From the describtion of this network, we can image that the problem is hard at the start, and it may gets easier and easier as we mapped more pieces to the whole picture, just as when human doing the puzzle. However there is one additional infomation with the inpput - the images coordinates are usually continuous. Given these facts, a transformer or RNN network with attention layer may suit for this problem. 

Based on current popular nlp models, such as BERT, a simliar model can be proposed. The embedding layer takes in the input images and added a 2D posistional encoding to each single image tensor. The attention layer perform a self-attention on each image frames and output the deeper presentation of the background. The attention layer can then connected to several decoder layers. One is to generate a high resolution background picture, two is to generate similer image frame based on different input positions. 

step 1:
train minGPT on small and low resolution dataset for functional validation 
step 2:
introduce cnn and complex structure for higher resolution or other purpose


After some further reflection on this previous idea. I figured out that something like a puzzle solver maybe not that direly needed in the real world as we usually have the  coordinating infomations of the scatter pieces for their original source. Nevertheless, I came up with another problem that, once solved, maybe more meaningful and magnificent to the ML field. The problem is that whether we can design a network, can be simple,  but can learn from the flow of image streams. It does not require lables, but it learns by purely doing comparision - comparision of the contents among the each frames, and by doing this, the network should be able the identify some "moving items" in the stream. conv com between frames
