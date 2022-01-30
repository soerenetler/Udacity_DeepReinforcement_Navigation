# Report
## The learning approach

To solve the descriped environment a Deep Q-Learning appraoch. This approach is very similar to normal Q-Learning. In Q-Learning a table (so called Q-table) is initialized which contains the Q-Value for all state action pairs. The Q-Value describes the Quality of an action `a` at a state `s` and is defined as the best cumolated future reward when continueing optimally onward afterwards. The algorithem then choses an action from the Q-table (based on the epsilon-greedy policy), performs that action, measures the rewards and updates the Q-table accordingly.

In Deep Q-Learning this Q-table is approximated using a deep neural network, because number of possible states are enormous. 

This convolutional neural network (CNN) takes the state representation as its input and approximates the Q-Value for all possible actions: `Q(st, a)`

An architecture consisting of three layers is used. The input dimensionality is 37 for the dimensionality of the state space and the first layer has 128 dimensional ouput. The second layer takes those 128 dimensions and reduces them to 64. In the third layer the output consists of four dimensions for the 4 possible action.

## Implementation
The implementation is very similar to the one in the privious project (https://github.com/udacity/deep-reinforcement-learning/blob/master/dqn/solution/Deep_Q_Network_Solution.ipynb). The hyperparameters are improved by increasing the output size of the first layer of the neural network.

## Hyperparameter
The model contains the following hyperparamter. the parameter value are based on the previous project in the nanodegree and yield good results.

### Layers of the CNN
The dimensionality of the hidden layer of the CNN is evaluated. Both 64, 128, 256 dimensions are tested.

### Epsilon
The epsilon value for the epsilon-greedy policy defines how mus the much the model chooses the best possible action based on the result of the CNN or tries out other potentially worse action for exploration. This value is 1 in the beginning and decreases by 0.005 per episode until reaching 0.01.

### Other Parameters
 - BUFFER_SIZE = int(1e5)  # replay buffer size
 - BATCH_SIZE = 64         # minibatch size
 - GAMMA = 0.99            # discount factor
 - TAU = 1e-3              # for soft update of target parameters
 - LR = 5e-4               # learning rate 
 - UPDATE_EVERY = 4        # how often to update the network

## Learning Curve
![Reward curve](learning.png?raw=true)

## Further improvements
An interesting next step could be the implementation of prioritized Experience Replay. This technique ranks the importance of the expiriences based on the TD error.