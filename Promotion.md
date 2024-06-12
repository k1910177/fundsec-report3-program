# ex1

Please write me a python code to do a Side-Channel Simulation with 2 Steps.  The taraget is an AES encryption in which 16 S-boxes are calculated in parallel. 

For the 1st step, please generate some simulaited power traces.
The power trace should the Hamming weight of the first round's S-box output plus some Gaussian noise.
Please generate 5000 simulated traces for 5000 random plaintexts.
Save the generated traces and the plaintexts in to some file. 

For the 2nd step, read the file to get the plaintexts and traces to perform a side-channel attack key recovery. 
The key recovery should be performed byte by byte targeting the first subkey of AES. 
And the key recovery should use the Hamming weight leakage model.
As the result, please show how many key bytes are correct.

# ex2

Since 16 S-boxes are calculated in parallel, the simualted trace should be the summation of the leakage from 16 S-boxes. Please update your code.
Also, please draw the result of recoveryed key bytes vs the used number of traces. 

# ex3

Please try another key recovery method based on the original differential power analysis.
In the evalution function used in key recovery, please use the least significant bit of Sbox output to seperate the traces into 2 groups, then use the absolute value of the difference of means for these 2 groups as the score for the key guess. 

# ex2-1, ex3-1

Please change step 1 so that the lekage model is not a perfect Hamming weight model, the traces follows the trends of Hamming weight, but they are not exact value of its Hamming weight. Please update your code, and only show the updated part.  