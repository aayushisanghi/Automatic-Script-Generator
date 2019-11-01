# Automatic-Script-Generator


1) Generating batches for character-wise LSTM: 

There are 2 values here - 
a) the batch size is the number of rows or "sequences" in the batch.
b) the "sequence length" or "n_steps" is the look-back value. Hence if "sequence length" is 5 we uss 5 characters to predict the next 5. Hence, the number of characters in each batch will be batch size * sequence length. <since we only need to account for the characters which are in the features, not the predicted ones>
