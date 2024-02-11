# Excel-Transformer
# Description
A Microsoft Excel demonstration of the transformer from the "Attention Is All You Need" paper. This Excel document implements a basic two example mini-batch of a the transformer from the aforementioned paper. The document aims to provide a basic numerical example which illustrate the internal workings of a transformer. The transformer contains two layers with each layer containing an encoder and decoder. The example utilizes two heads as well.
# Features
-The transformer contains two layers with each layer containing an encoder and decoder. The attention mechanism in every layer utilizes two heads.

-The excel doument outlines the full forward, backward pass and gradient update for a mini-batch containing two examples. 

# Usage / Instructions
-There is two sheets "Transformer EX1" and "Transformer EX2" these contain the forward and backward passes for and individual training examples. The contents of each of the example sheets is cotained within rows 1045-3219 and columns A-VT.

-The "inputs" to the encoder and decoder can be found at the middle bottom of the "DECODER 0" and "ENCODER 0" and are contained within the "Embedding" Layer

-The ouput and cost calculation is centred and above "DECODER 1"

-The "PARAMETER UPDATES" sheet contains the calculations involved in performing a gradient step using the ADAM optimizer for all the parameters within the example. This section does not use the learning rate scheduler that was used in the original "Attention is All You Need" paper.

-The Transformer has been broken down into modules. In these modules the green cells represent the flow of the forward pass and the red cells represent the flow of the backward pass.

-On other occasisions there is other coloured cells that represent the flow of the forward and backward passes in the model. In these cases the darker shades of the colour represent the forward pass and the lighter shades the backward pass. I have tried to keep the colours consistent and have them represent the same token position thorughout the Excel document however this was not always possible and I have prioritized readablity over strict adherance to these rules.

-On the two example sheets "Transformer EX1" and "Transformer EX2" the boxes with parameter gradients inside them that are coloured pink contain the parameter gradients acculumated total for that layer over the course of that particular layer. These gradient accumulations are then used in the "PARAMETER UPDATES" sheet in order to calculate the total parameter gradients acculumated total for two example mini-batch.

-As mentioned there is two heads per attention layer. The head calculations are seperated by cells forming a dashed line

-Many of the formulas within the document use Excel array / matrix forulas. Sometimes clicking on cells with these formulas in them can take away this formating which may lead to errors causing all cells with formulas dependent on that cell to throw an error which will be denoted by "#########" if this occurs locate the cell (trace back to where the formulas are no longer "########") and then when inside the cell hit "ctrl+shift+enter" this will cause excel to treat it as an array operation again.

