# TradingRL


So, what we are going to do in this notebook is to build a deep reinforcement algorithm to develop trading strategies. This notebook is divided by different parts:

    Import and downloading of the data -> Where we are going to install the OHLCV (Close, High, Low, Close, Volume) financial data from the yahoo finance library ib the form of a pandas DataFrame and install a few dependencies that we are going to need.

    Feature Engineering -> In this chapter, we are going to use the ta (technical analysis) library to biuld some feature for this dataframe. We are going to study the correlation between these features, removing some of the features which have more correlation between them.

    Train/Test Partition -> In this chapter we are going to divide the dataset between train and test dataset in the slicing fashioned way, without randomize the data, because we need the serialization nature of this dataframe to get the patterns of the financial data that we are handling.

    Gym Environment Creation -> In the world of reinforcement learning, there are some basic things that we are going to need froam a environment for training a reinforcemet algorithm, some of them are: action variables and space, observation variables and space and reward. The action space is the set of actions that our algorithm could take to interact with the environment, the observation space is the data that our agent is going to see in every step of the training. With the help of the gym library, we are going to create a trading environment for the later training of our deep reinforcement algorithm.

In this environment environment, we are going to implement a method to render the performance of the model every time our model ends the trading session or gets bankrupt.

    Training parameter optimization -> In this chapter, we are performing bayesian optimization to get some optimal hyperparameters for the reinforcement learning algorithm.

    Training -> With the help of the environment we created before and the sb3 (stables baselines 3) library, we are going to train our deep reinforcement learning algorithm, saving some information of the training with the help of tensorboard for the later visualization of this training performance with some metrics such as Policy Loss, Mean Reward, Episode Length... What we are going to do is to save the model every 10k steps of training.

    Test and performance renderization -> After training, we will visualize the performance of the model through the training with tensorboard, and we are going to load the model wihch gets the best Mean Reward in the training processwith the help of tensorboard. Then, we are going to visualize the performance of this model in the test data partition.

    Model Performance visualization trough the training process -> Last, we are going to use the render method of our environment to visualize the performance of the model every 10k steps of training, in the training partition of our dataset.


