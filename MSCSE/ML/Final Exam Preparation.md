# Adaboost
![alt text](assets/adaboost.png)

## Working of AdaBoost

    Initialize Weights:
        Assign equal weights to all training samples/instances/row/records.

    Train Weak Classifiers:
        Train a weak classifier (e.g., Decision Stump) using weighted training data.
        Calculate the classifier's error rate.

    Update Weights:
        Increase the weights of misclassified samples so that the next classifier focuses more on these.
        Decrease the weights of correctly classified samples.

    Combine Weak Classifiers:
        Assign a weight to each weak classifier based on its accuracy.
        The final prediction is made using a weighted majority vote of all classifiers.



## 
![alt text](assets/adaboost_example.png)
![alt text](assets/adaboost_example_2.png)
![alt text](assets/adaboost_example_3.png)
![alt text](assets/adaboost_example_4.png)
![alt text](assets/adaboost_example_5.png)
![alt text](assets/adaboost_example_6.png)
![alt text](assets/adaboost_example_7.png)
![alt text](assets/adaboost_example_8.png)
![alt text](assets/adaboost_example_9.png)
![alt text](assets/adaboost_example_10.png)



# Clustering

## Ensemble Clustering
Ensemble clustering is a process of integrating multiple clustering
algorithms to form a single strong clustering approach that usually
provides better clustering results. It generates a set of clusters from a
given unlabelled data set and then combines the clusters into final
clusters to improve the quality of individual clustering.

- No single cluster analysis method is optimal.
- Different clustering methods may produce different clusters, because
they impose different structure on the data set.
- Ensemble clustering performs more effectively in high dimensional
complex data.
- It’s a good alternative when facing cluster analysis problems.


Generally three strategies are applied in ensemble clustering:
1. Using different clustering algorithms on the same data set to create
heterogeneous clusters. (different clustering algorithm + same dataset) => heterogeneous clusters
2. Using different samples/ subsets of the data with different clustering
algorithms to cluster them to produce component clusters.  (different clustering algorithm + different samples/ subsets of the data) => component clusters 
3. Running the same clustering algorithm many times on same data set
with different parameters or initialisations to create homogeneous
clusters. (((same clustering algorithm + same dataset) many times) differet parameters) =>  homogeneous clusters

The main goal of the ensemble clustering is to integrate component
clustering into one final clustering with a higher accuracy.



# A single Neuron
- A single neuron/perceptron (Forward propagation) is the fundamental building block of a neural network. It takes inputs, processes them using weights and a bias, applies an activation function, and produces an output.

The output of a single Neuron is

![alt text](assets/output_of_single_nuron.png)
![alt text](assets/output_of_single_nuron_2.png)
![alt text](assets/output_of_single_nuron_3.png)
![alt text](assets/output_of_single_nuron_4.png)

# Activation Function
- An activation function is a mathematical function that determines whether a neuron should be activated or not by calculating weighted sum and adding bias
- mathematical functions applied to the output of a neuron.
- It introduces non-linearity into the output of  a neuron

![alt text](assets/activation_function_depth.png)
![alt text](assets/activation_function_depth_2.png)




## 2 Types of Activation Functions

### Linear Activation: 
- No transformation between input and output. So, input will be output.

### Non-Linear Activation Functions
- Non-linear activations increase the functional capacity of the neural network, because it allows it to present non-linear relationships between features in the input.
- 
![alt text](assets/activation_function_depth_3.png)
![alt text](assets/activation_function_depth_4.png)
![alt text](assets/activation_function_depth_5.png)
![alt text](assets/activation_function_depth_6.png)
![alt text](assets/activation_function_depth_7.png)
 