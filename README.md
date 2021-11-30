# NLP-Group-Project-WiC

The project consists in developing a model that given two sentences using the same word in different contexts can  say if their meaning is the same.
The code has the following structure:

Processing data:
        - First we import the data set, and parse the document. We store senteces in a list since RoBerta tokenizer works with lists. Then another function find the position of the words that we are comparing.
        - In the next function we process the data: locate words in the context and locating them, and then taking the corresponding label to the sentence

Definition of the model:
    - The innit function we are taking the RoBERTa model and we ar adding a layer. In the forward function we have the same parameters as RoBERTa. We get the embeddings and the see how different are the two words, and getting the result based on that.
    
Training loop:
    - We ahve set a minimum accuracy, and a maximum amaunt of times to train the model. We change the weights until we achieve tha desired accuracy or the maximum amount of times, and then freeze those weights.
    
Evaluation:
    - Now we evaluate the accuracy of our model using the weights that we obtained while training.
    


These are the sources we have used:

Information about BERT and implementing it:
https://www.youtube.com/watch?v=EPa98fyxZ-s

https://towardsdatascience.com/bert-to-the-rescue-17671379687f

https://www.youtube.com/watch?v=EMDax4OH_ps

BERT model and other transformers:

https://huggingface.co/transformers/installation.html

Examples of implementation:

https://jalammar.github.io/a-visual-guide-to-using-bert-for-the-first-time/

https://github.com/llightts/CSI5138_Project

https://github.com/orenmel/context2vec

Research paper about sense disambiguation:

https://aclanthology.org/2021.semeval-1.15.pdf


Natural Language Inference for word disambiguation:
https://www.analyticsvidhya.com/blog/2021/05/bert-for-natural-language-inference-simplified-in-pytorch/