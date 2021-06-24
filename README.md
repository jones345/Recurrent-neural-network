# Recurrent-neural-network
Recurrent neural network case study and project
 Recurrent neural network(RNN)

What is a Neural Network?

Neural networks, also known as artificial neural networks (ANNs) or simulated neural networks (SNNs), are a subset of machine learning that form the foundation of deep learning algorithms. Neural Networks are a collection of algorithms that are designed to recognize patterns and are modeled after the human brain. They interpret sensory data by labeling or clustering raw input using machine perception. They can recognize numerical patterns contained in vectors, which must be translated into all real-world data (images, sound, text, or time series).

ANNs consist of a node layers, which contain an input layer, one or more hidden layers and an output layer. Every node, or artificial neuron, has a weight and threshold and is connected to a different one. When the output of a single node exceeds the specified threshold, the node is turned on and the data is sent to the next network layer. Otherwise, the next network layer will not receive data.



Neural networks use training data for the development and over time improvement of their accuracy. But once these algorithms are accurately targeted, they are powerful tools in computer science and artificial intelligence that enable us to high-speed classify and compile data. Speech recognition or image recognition tasks may take minutes to hours compared to human experts' manual identification. The search algorithm from Google is one of the most well-known neural networks.

How a Neural Network Works?
There are many layers in a neural network. A specific function is performed in each layer, and the complex the network, the more the layers. That is why a multilayer perception is also known as a neural network.

The purest form of a neural network has three layers:
Input layer — initial data for the neural network.
Hidden layers — intermediate layer between input and output layer and place where all the computation is done.
Output layer — produce the result for given inputs.




On the picture above there are 3 yellow circles. They show the input layer and are typically marked as vector X. The hidden layers are composed of four blue and four green circles. The "activation" nodes in these circles are normally noted as W or θ. The red circle is the output layer (or the values for several output classes/types) or the predicted value.

The next layer has every node and weight of each connection (black arrow). Each node is connected with each node. The impact of this node on the next layer of the node can be seen in weight. So if we look at a node it looks like:



 
 
What is a Recurrent Neural Network (RNN)?


A recurring neural network (RNN, or "Recurrent Neural Networks") is a kind of neural network that uses sequential data or time series data. It is a profoundly-learned algorithm that can be used as a linguistic translation, natural speech processing (NLP), speech recognition and image captioning. Recurring neural networks use training data, like feedforward and convolutionary neural networks (CNNs). It is distinguished by its "memory" because it uses previous inputs to influence the current input and output. Traditional deep-neural networks assume that each input and output is independent.Recurring neural network output depends on prior sequence elements. While future events would also help in determining the output of a particular sequence, these events are not taken into account in their predictions by the unidirectional recurring neural networks.


Recurrent Neural Network vs. Feedforward Neural Network

Comparison of Recurrent Neural Networks (on the left) and Feedforward Neural Networks (on the right)

Recurrent neural networks differ from feedforward neural networks because they include a feedback loop, whereby output from step n-1 is fed back to the net to affect the outcome of step n, and so forth for each subsequent step. For example, if a network is exposed to a word letter by letter, and it is asked to guess each following letter, the first letter of a word will help determine what a recurrent net thinks the second letter will be, for example Let’s take an idiom, such as “feeling under the weather”, which is commonly used when someone is ill, to aid us in the explanation of RNNs. In order for the idiom to make sense, it needs to be expressed in that specific order. As a result, recurrent networks need to account for the position of each word in the idiom and they use that information to predict the next word in the sequence.


Looking at the visual below, the “rolled” visual of the RNN represents the whole neural network, or rather the entire predicted phrase, like “feeling under the weather.” The “unrolled” visual represents the individual layers, or time steps, of the neural network. Each layer maps to a single word in that phrase, such as “weather”. Prior inputs, such as “feeling” and “under”, would be represented as a hidden state in the third timestep to predict the output in the sequence, “the”.



Another distinguishing characteristic of recurrent networks is that they share parameters across each layer of the network. While feedforward networks have different weights across each node, recurrent neural networks share the same weight parameter within each layer of the network. That said, these weights are still adjusted through the processes of backpropagation and gradient descent to facilitate reinforcement learning.

Recurrent neural networks leverage backpropagation through time (BPTT) algorithm to determine the gradients, which is slightly different from traditional backpropagation as it is specific to sequence data. The principles of BPTT are the same as traditional backpropagation, where the model trains itself by calculating errors from its output layer to its input layer. These calculations allow us to adjust and fit the parameters of the 

model appropriately. BPTT differs from the traditional approach in that BPTT sums errors at each time step whereas feedforward networks do not need to sum errors as they do not share parameters across each layer.

Through this process, RNNs tend to run into two problems, known as exploding gradients and vanishing gradients. These issues are defined by the size of the gradient, which is the slope of the loss function along the error curve. When the gradient is too small, it continues to become smaller, updating the weight parameters until they become insignificant—i.e. 0. When that occurs, the algorithm is no longer learning. Exploding gradients occur when the gradient is too large, creating an unstable model. In this case, the model weights will grow too large, and they will eventually be represented as NaN. One solution to these issues is to reduce the number of hidden layers within the neural network, eliminating some of the complexity in the RNN model.

Commonly used activation functions
an activation function determines whether a neuron should be activated. The nonlinear functions typically convert the output of a given neuron to a value between 0 and 1 or -1 and 1
Sigmoid Function



 


 



