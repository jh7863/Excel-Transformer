# Excel-Transformer
A Microsoft Excel demonstration of the transformer from the "Attention Is All You Need" paper. This Excel document implements a basic two example mini-batch of a the transformer from the aforementioned paper. The document aims to provide a basic numerical example which illustrate the internal workings of a transformer. The transformer contains two layers with each layer containing an encoder and decoder. The example utilizes two heads as well.
# Instructions
-There is two sheets "Transformer EX1" and "Transformer EX2" these contain the forward and backward passes for and individual training examples. The contents of each of the example sheets is cotained within rows 1045-3219 and columns A-VT.

-The "inputs" to the encoder and decoder can be found at the middle bottom of the "DECODER 0" and "ENCODER 0" and are contained within the "Embedding" Layer

-The ouput and cost calculation is centred and above "DECODER 1"

-The "PARAMETER UPDATES" sheet contains the calculations involved in performing a gradient step using the ADAM optimizer for all the parameters within the example. This section does not use the learning rate scheduler that was used in the original "Attention is All You Need" paper.
