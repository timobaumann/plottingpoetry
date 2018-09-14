# plottingpoetry
Introduction to neural networks for poetry analysis (and similar tasks)

Run the examples in a jupyter notebook in your browser by clicking on the binder link:
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/timobaumann/plottingpoetry/master)

Neural networks are based on the analogy to the human brain. Like the natural example, "neurons" in an NN take as input the weighted output from many other neurons, aggregate them, and decide if they should "fire" if a given threshold is surpassed:

![Depiction of an artificial neuron, Wikipedia](https://upload.wikimedia.org/wikipedia/commons/7/7f/ArtificialNeuronModel_deutsch.png)

Artificial neural networks are always organized in layers an each neuron in a layer is connected to *all* neurons on the preceding layer. However, weights can be zero which is equivalent to no connection. The necessary computations for all neurons in one layer can be integrated into one (or few) large matrix operations. This is why you don't see many summations in the code to follow. You simply see ```Matrix * Input + bias```. Trust the mathematicians that the matrix product takes care of this.

The first layer of a network is the input layer and could be compared to sensory neurons. 
The final layer of a network indicates the output of the network. For classification with N classes, we typically use N output neurons and check which one is most active.
