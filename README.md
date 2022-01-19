# Neural_Network_
___
Overview of the loan prediction risk analysis:
---

The purpose of this analysis is to use Nueral Networks to try to predict if a proposals are likely to be successful. This is accomplished using Tensor Flow's Keras to train and test existing data.

Results:
---
1)Our IS_SUCCESSFUL column was our target for our model.
Before encoding the columns that were object datatypes, our features used were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. For the columns that were object datatypes, we encoded these columns using the OneHotEncoder() function.
2)The columns that were neither targets nor features were dropped. These were the EIN, NAME, and the original columns that were encoded.

Compiling, Training, and Evaluating the Model;
---

3)For our neaural network, we used two hidden layers with 80 and 30 neurons, respectively. The activation function for the hidden layers used was ReLU, and Sigmoid for the output layer. ReLU is computationally efficient, and other activation functions did not improve the accuracy and Sigmoid works well for binary classification problems.
4)The target accuracy was 75%, and our initial neural network was only able to achieve less than the targeted 75% accuracy.
5)To try to reach 75% accuracy, we removed noisy variables from features, added additional neurons and layers and tested different activation functions and optimizers. After this, we were still unable to reach 75% accuracy, so we used the KerasTuner to try to get a set of hyperparameters that would reach 75% accuracy. 6)This also could not reach our target accuracy, so we instead attempted to intentially overfit the model. Using two layers with 300 and 250 neurons,(after trying many different variations, I concluded that this is the best combo I can get to reach the intented 75%) respectively, and training on 99% of the dataset we were able to achieve 76.9% accuracy. Although this model is overfit, learning how to overfit will help to avoid overfitting in the future.

Summary:

The results of the deep learning model imply that it was most likely not the best solution for this problem. Even after intentionally overfitting, the accuracy of the model only slightly improved. 
However, maybe it would be recomended, despite each one's pro's and cons:
1)support vector machiens, 
2)decision trees, 
3)k-nearest neighbors.
