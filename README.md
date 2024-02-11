# Excel-Transformer
# Description
A Microsoft Excel demonstration of the transformer from the "Attention Is All You Need" paper. This Excel document implements a basic two example mini-batch of a the transformer from the aforementioned paper. The document aims to provide a basic numerical example which illustrate the internal workings of a transformer. The transformer contains two layers with each layer containing a two headed encoder and decoder. 
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

# Contributions
# License
-This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

-The layer normilization portions of this work are derived from "Understanding the backward pass through Batch Normalization Layer" by Dean Attali, licensed under the MIT License (MIT). Copyright (c) 2016 Dean Attali.
# Acknowledgments
-I'm thankful to Dean Attali for his clear and practical explanation of Batch Normalization(Which I then adapted into layer normilization), particularly through his discussion on "Understanding the backward pass through Batch Normalization Layer." His work has been a valuable resource in understanding complex machine learning concepts and implementing them in this project. Frederik's contributions, along with the CS231n course material, have significantly enhanced my learning journey in machine learning. Check out more of his insights on [his blog](https://kratzert.github.io/).

-Special thanks to Jay Alammar for his enlightening work, particularly "The Illustrated Transformer," which has greatly informed this project. His clear visual explanations of complex machine learning concepts have been invaluable. Check out his insights on his blog (https://jalammar.github.io/illustrated-transformer/) and [YouTube channel] (https://www.youtube.com/@arp_ai) for more transformative content.

-I would like to express my gratitude to Josh Starmer for their exceptional series of videos on deep learning, especially their insights on transformers and cross entropy loss which have significantly influenced this project. Their expertise and clear explanations have been invaluable. For anyone interested in deepening their understanding of deep learning or statistics, I highly recommend exploring their content at https://www.youtube.com/@statquest.

-The concepts presented here are based on the concepts outlined by the seminal paper "Attention Is All You Need" by Ashish Vaswani et al. This work has been foundational in understanding the Transformer model's architecture and its applications in natural language processing. For a comprehensive dive into these groundbreaking ideas, the original paper is accessible at [https://arxiv.org/abs/1706.03762](https://arxiv.org/abs/1706.03762). I am grateful for the authors’ contributions to the field.

-This project benefited from the use of OpenAI's ChatGPT, which provided assistance with gaining an undertanding of the transformers underlying architecture. The AI's input was invaluable for refining ideas and enhancing the quality of the work presented.




