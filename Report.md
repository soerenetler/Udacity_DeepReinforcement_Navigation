# Report
## The learning approach

To solve the descriped environment a Deep Q-Learning appraoch is used with an architecture consisting of three layers. The input dimensionality is 37 for the dimensionality of the state space and the first layer has 128 dimensional ouput. The second layer takes those 128 dimensions and reduces them to 64. In the third layer the output consists of four dimensions for the 4 possible action.

## Implementation
The implementation is very similar to the one in the privious project (https://github.com/udacity/deep-reinforcement-learning/blob/master/dqn/solution/Deep_Q_Network_Solution.ipynb). The hyperparameters are improved by increasing the output size of the first layer of the neural network.

## Learning Curve
![Reward curve](learning.png?raw=true)

## Further improvements
An interesting next step could be the implementation of prioritized Experience Replay. This technique ranks the importance of the expiriences based on the TD error.