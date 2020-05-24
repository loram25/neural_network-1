# Neural Network
## Module 19


## Summary

### How many neurons and layers did you select for your neural network model? Why?

I elected to desin a 2 layer neural network, with a branched first hidden layer. I noticed a huge skew in the ASK_AMT column (a majority of the amounts are $5000). I designed one branch to be a sigmoid with 2 neurons, hoping the model will pick up on this binning. The second branch was a traditional ReLu layer with 1.25 times the amount of input neurons (456). I then combined these branches and sent them into a second hidden layer with half the amount of input neurons. I outputed this to a simple single neuron with a sigmoid function.

### Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

I was able to achieve target performance, demonstrating **79.2%** accuracy on test data. I tried lots of steps to improve model performance. Important hyper-parameter tuning was set up for early stopping and reducing learning rate on plateau. This allowed me to run simulations faster. I tried a lot slicing with input data - different thresholds for binning the classification, name and application type categories. I tried dropping different columns and encoding columns (like INCOME_AMT) different ways.

### If you were to implement a different model to solve this classification problem, which would you choose? Why?
I would use Random Forest. With the limited features (before encoding), it is well suited to decision style parsing (i.e. what is application type? what is ask amount). I included a random forest model simulation in the challenge file and achieved **78.8%** accuracy. This accuracy is nearly identical to the NN with much less processing time. The input data may not be complex enough for a neural network to outperform more traditional supervised machine learning algorithms.        
