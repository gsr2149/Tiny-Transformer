# Tiny-Transformer
The goal for this assignment is to implement the core logic of a Transformer block from scratch and train this tiny Transformer on the Shakespeare Tiny Corpus dataset. It is a common corpus used for training and experimenting with different language models. Given the previous tokens can the transformer essentially predict the next token in the set.

In order to do this, we have to begin by using tokenization to split the text. For this assignment, I used Byte-Pair Encoding (BPE) with the help
of chat GPT. I chose Byte Pair encoding over WordPiece and SentencePiece, but they are really
similar in nature. Byte Pair encoding relies on a pre-tokenizer that splits the training data into
words while WordPiece initializes the vocabulary to include every character present in the
training data and learns the number of merge rules. After tokenization I split the text into
overlapping sequences of inputs and targets and split up the data. Now it was time to begin
building the transformer.
Building the transformer from scratch took me some time even with the help of chat
GPT. I ran into a lot of issues which I wasn’t aware of until I began the visualization phase. I
began with the positional encoding class which gives the transformer the information about the
order of tokens in a sequence. Positional encoding goes before the self-attention model because x
needs to contain its positional information. Although a model can function without assigning
explicit positional encodings to each token, the model’s ability to understand data can become
impaired so I thought it better not to take that risk since without it is losses the order of
information. Then I worked with Multi-Head Self Attention.
