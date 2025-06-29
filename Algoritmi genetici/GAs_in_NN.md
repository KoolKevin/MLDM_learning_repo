"""
Instead of using traditional backpropagation and/or a policy, and a reward function in caso of RL, neuroevolution applies principles of GAs and natural selection to train the weights in a neural network. This technique unleashes many neural networks on a problem at once. Periodically, the best-performing neural networks are “selected,” and their “genes” (the network connection weights) are combined and mutated to create the next generation of networks. **Neuroevolution is especially effective in environments where the learning rules aren’t precisely defined or the task is complex, with numerous potential solutions**.

One of the first examples of neuroevolution can be found in the 1994 paper “Genetic Lander: An Experiment in Accurate Neuro-genetic Control” by Edmund Ronald and Marc Schoenauer. In the 1990s, traditional neural network training methods were still nascent, and this work explored an alternative approach. The paper describes how a simulated spacecraft—in a game aptly named Lunar Lander—can learn how to safely descend and land on a surface. 
**Rather than use handcrafted rules or labeled datasets**, the researchers opted to use GAs to evolve and train neural networks over multiple generations. And it worked!
"""

Super interessante! Se non ho un labeled dataset per fare supervised learning, ho gli algoritmi genetici come alternativa!