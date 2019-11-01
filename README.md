# Automatic-Script-Generator


1) Generating batches for character-wise LSTM: 

There are 2 values here - 
a) the batch size is the number of rows or "sequences" in the batch.
b) the "sequence length" or "n_steps" is the look-back value. Hence if "sequence length" is 5 we uss 5 characters to predict the next 5. Hence, the number of characters in each batch will be batch size * sequence length. <since we only need to account for the characters which are in the features, not the predicted ones>

When we do reshape(no_of_rows, -1) it makes the 1D array into a matrix with no_of_rows that we have specified. The reason this works in our code is that we have let go of the additional characters before rehaping, so we have a perfect multiple of the "sequence length". 

Reference code(?): https://adventuresinmachinelearning.com/recurrent-neural-networks-lstm-tutorial-tensorflow/
