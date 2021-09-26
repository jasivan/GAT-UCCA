# GAT-UCCA
Sentence embedding using GAT and UCCA parsing

This code aims to improve sentence embeddings using the UCCA parser (https://universalconceptualcognitiveannotation.github.io/) and GAT (https://petar-v.com/GAT/) by strucutring them in a siamese network. The code uses mean squared error as the loss function.

The code outputs the mean square error (MSE), Person's correlation coeffiecient and Spearman's correlation coeffiecient between the predicted similarity score and target similarity using the SICK dataset. The architecture produces the sentence embeddings using the UCCA parser to add semantic information to the GAT, then it computes a similarity score between pairs of sentences to finally use a siamese network to compare these with the gold standard output.

To use this code, you need to download the two zip files that have the XML files of the paired sentences i.e. sentence-A-full.zip and sentence-B-full.zip. You will also need relatedness-score-full.txt in the same folder.

Before running the code from GAT-UCCA.ipynb, make sure to adjust the parameter for the size of the position and label embedding (0 if you wish not to use them) and the number of sets of 5 epochs that you wish to train the model on.
