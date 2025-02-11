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





# Neural Network


# A single Neuron (The perceptron or a single neuron)
- A single neuron/perceptron (Forward propagation) is the fundamental building block of a neural network. 
- It takes inputs, processes them using weights and a bias, applies an activation function, and produces an output.

The output of a single Neuron is

![alt text](assets/output_of_single_nuron.png)
![alt text](assets/output_of_single_nuron_2.png)
![alt text](assets/output_of_single_nuron_3.png)
![alt text](assets/output_of_single_nuron_4.png)
![alt text](assets/output_of_single_nuron_5.png)
![alt text](assets/output_of_single_nuron_6.png)
![alt text](assets/output_of_single_nuron_7.png)
![alt text](assets/output_of_single_nuron_8.png)
![alt text](assets/output_of_single_nuron_9.png)
![alt text](assets/output_of_single_nuron_10.png)
![alt text](assets/output_of_single_nuron_11.png)
![alt text](assets/output_of_single_nuron_12.png)
![alt text](assets/output_of_single_nuron_13.png)
![alt text](assets/output_of_single_nuron_14.png)



- A Neural Network is combinations of basic Neurons — also called perceptrons (A basic Unit shown in the above diagram- green circle in middle) 
- 
![Alt text](assets/multilayer.png)

# Activation Function
- An activation function is a mathematical function that determines whether a neuron should be activated or not by calculating weighted sum and adding bias
- mathematical functions applied to the output of a neuron.
- It introduces non-linearity into the output of  a neuron
- An Activation Function decides whether a neuron should be activated or not.
- Depending on the nature and intensity of these input signals, the brain processes them and decides whether the neuron should be activated (“fired”) or not. 

![alt text](assets/activation_function_depth.png)
![alt text](assets/activation_function_depth_2.png)
![alt text](assets/activation_function_depth_8.png)
![alt text](assets/activation_function_depth_9.png)


## 2 Types of Activation Functions

### Linear Activation: 
- No transformation between input and output. So, input will be output.
- The linear activation function, also known as "no activation," or "identity function" (multiplied x1.0), is where the activation is proportional to the input. 
- The function doesn't do anything to the weighted sum of the input, it simply spits out the value it was given

![Alt text](assets/linear_activation.png)
![Alt text](assets/linear_activation2.png)


### Non-Linear Activation Functions
- Non-linear activations increase the functional capacity of the neural network, because it allows it to present non-linear relationships between features in the input.
- 
![alt text](assets/activation_function_depth_3.png)
![alt text](assets/activation_function_depth_4.png)
![alt text](assets/activation_function_depth_5.png)
![alt text](assets/activation_function_depth_6.png)
![alt text](assets/activation_function_depth_7.png)
![alt text](assets/activation_function_depth_10.png)
![alt text](assets/activation_function_depth_11.png)
![alt text](assets/activation_function_depth_12.png)



## Loss Function
- some people also call it error function
- The loss function (or error) is for a single training example, while the cost function is over the entire training set (or mini-batch for mini-batch gradient descent).
![Alt text](assets/loss_function.png)
![Alt text](assets/mae.png)
![Alt text](assets/mse.png)

## Gradient descent (GD)
- Gradient descent (GD) is an iterative first-order optimisation algorithm used to find a local minimum/maximum of a given function. 
- This method is commonly used in machine learning (ML) and deep learning(DL) to minimise a cost/loss function.


--------
----
-----

# CNN (Convolutional Neural Network)

- **Convolutional Neural Network (CNN)**, or **ConvNet**, is a class of deep neural networks commonly used to analyze visual imagery, such as object detection, image recognition, image classification, face recognition, etc.
- CNNs classify an input image into certain categories (e.g., Dog, Cat, Tiger, Lion).
- An input image is represented as an array of pixels in the form of **h × w × d**, where:
  - **h** is the height,
  - **w** is the width,
  - **d** is the depth (or the number of channels, e.g., RGB channels).

An example of a **6 x 6 x 3** matrix for an RGB image is shown in **Fig. 1.21**.

Each input image passes through a series of layers, which include:
1. **Convolution Layers** with filters (kernels),
2. **Pooling Layers**,
3. A **Fully Connected (FC) Neural Network**, and
4. A **Softmax function** to classify the object, as shown in **Fig. 1.22**.

---

### The Core Components of a CNN:
1. **Convolution Layer**  
2. **Activation Function (ReLU)**  
3. **Pooling Layer**  
4. **Fully Connected Neural Network**


#### Rule: **CAP F**ull

![alt text](assets/cnn_rgb.png)


# Convolution Layer in CNNs

![Alt text](assets/CNN_layers.jpg)

The **Convolution Layer** is the first layer used in Convolutional Neural Networks (CNNs) to extract features from an input image. This layer is essential for learning spatial hierarchies by preserving relationships between pixels.

## Convolution Operation:
Convolution is a mathematical operation that involves two inputs:
1. **Image Matrix** (input data)
2. **Filter or Kernel** (a small matrix, e.g., \(3 \times 3\))

For example, let’s consider:
- **5 x 5 image matrix**: This is the input image with pixel values.
- **3 x 3 filter matrix**: This is the kernel used for convolution.

The **output** of this operation is called the **Feature Map**, which is a smaller matrix derived by applying the filter over the input image.

### Example:
For a \(5 \times 5\) image and a \(3 \times 3\) filter:
1. The filter moves over the image and performs an element-wise multiplication of the image and filter matrix.
2. The results are summed up to produce a value in the output (feature map).

This operation extracts features such as edges, textures, and patterns from the input image.

---

## Types of Filters:
Filters can be designed for various purposes:
- **Edge Detection**: Detects boundaries of objects in the image.
- **Blur**: Smooths out an image, reducing noise.
- **Sharpen**: Enhances edges to make them clearer.

### Example of Convolution with Different Filters:
- **Edge Detection Filter**: Detects the edges in the image.
- **Blur Filter**: Reduces sharpness and smooths the image.
- **Sharpen Filter**: Enhances the sharpness and detail of an image.

By applying different filters to the image, we can perform operations such as edge detection, blurring, and sharpening.

---

## Stride:
Stride refers to the number of pixels the filter moves over the input matrix during convolution.
- **Stride = 1**: The filter moves 1 pixel at a time.
- **Stride = 2**: The filter moves 2 pixels at a time.

The choice of stride affects the output feature map size. Larger strides result in smaller feature maps.

### Example of Convolution with Stride 2:
If the stride is set to 2, the filter will move 2 pixels at a time over the image, resulting in a smaller feature map than when the stride is set to 1.

---

## Padding:
Padding is used when the filter does not fit perfectly over the input image. It involves adding extra pixels around the image. Padding refers to adding extra pixels (usually zeros) around the input image before applying the convolution operation.

There are two main types of padding:

1. **Zero Padding**:  
   - Padding the image with zeros (or other values) around the borders so that the filter can fit. 
   - Zero padding is used to add extra rows and columns of zeros to the edges of an image. This technique is also known as “border padding” or “border mode”. The zeros are added to the borders of the image so that the size of the image is increased, but the original content remains unchanged. 
   - This ensures that the spatial dimensions of the output remain consistent, especially when using **same padding** to keep the output size the same as the input size.

   ![Alt text](assets/zero_padding.gif)
   ![Alt text](assets/zero_padding_2.gif)
   
2. **Valid Padding**:  
   In this case, parts of the image where the filter cannot fully fit are discarded, and the filter only operates where it can fully fit within the image bounds. This usually results in smaller output feature maps.


#### Why is padding required?
- Let’s look at an example to understand the need for padding. Consider a 5x5 input image and a 3x3 filter. When we perform a convolutional operation with this filter on the input image, we get a 3x3 feature map output.
![Alt text](assets/why_zero_padding.gif) 

This leads to two problems:

1. The output feature map is smaller (3x3) than the input image (5x5). As we apply more convolutional layers, the spatial dimensions keep decreasing, causing loss of information.
2. The pixels at the borders of the input are included in fewer convolutional operations compared to the center pixels. If important visual features are present at the edges, this can negatively impact performance.

To solve these issues, we apply padding to the input image before convolution.


### What is Padding?

Padding involves adding extra pixel rows/columns around the borders of an input image. For an nxn input image and an fxf filter, the shape of the output feature map without padding is (n-f+1)x(n-f+1). To maintain the same spatial dimensions after convolution, we set n-f+1=n, which means padding the input to size (n+f-1)x(n+f-1).

In the example above, the 5x5 image is padded to 7x7 by adding a single pixel row/column boundary with values of zero. This is called zero padding in frameworks like Keras.

![Alt text](assets/why_zero_padding_2.gif)

The formula for calculating output shape after padding is:

Output shape = (n + 2p — f + 1) x (n + 2p — f + 1) Where n is input size, f is filter size, and p is the padding amount.

Keras provides two padding options:

    ‘valid’: No padding is applied
    ‘same’: Pad input so output has same spatial dimensions as input
---

## Summary:
- **Convolution** extracts features from images by applying filters and generating feature maps.
- **Strides** control the step size when applying the filter to the image, influencing the output size.
- **Padding** ensures the filter fits perfectly over the image and preserves important features, with options for zero-padding or valid-padding.


![alt text](assets/Image_matrix_multiplies_kernel_or_filter_matrix.png)
![alt text](assets/convolutional_layer.gif)
![alt text](assets/convulation_layer2.png)





# Non-Linearity and Layers in CNN  

## **Non-Linearity (ReLU)**  
ReLU (**Rectified Linear Unit**) is an activation function used to introduce **non-linearity** in CNNs. It helps the model learn complex patterns beyond simple linear relationships.

The ReLU function is defined as:

```
f(x) = max(0, x)
```

This means:  
- If \( x \) is **positive**, it remains unchanged.  
- If \( x \) is **negative**, it becomes **zero**.  

ReLU is widely used because it helps mitigate the **vanishing gradient problem** and improves the training of deep networks.
 

---

![alt text](assets/activation_layer.png)


## **Pooling Layer**  
The **Pooling Layer** reduces the number of parameters in the images, making computations more efficient. This process is also known as **spatial pooling, subsampling, or downsampling**.  

### Types of Pooling:  
1. **Max Pooling** – Takes the largest element from the rectified feature map.  
2. **Average Pooling** – Takes the average of elements within a feature map.  
3. **Sum Pooling** – Computes the sum of all elements in the feature map.  

Pooling helps retain important features while reducing the spatial dimensions.
![alt text](assets/pooling.png)
---

## **Fully Connected (FC) Layer**  
- The **FC Layer** **flattens** the feature map matrix into a **vector**.  
- It combines the extracted features to form the final classification model.  
- Finally, an **activation function** such as **Softmax** or **Sigmoid** is used to classify the outputs into categories (e.g., cat, dog, car, truck).  

---

This structure enables **Convolutional Neural Networks (CNNs)** to learn meaningful patterns and classify images effectively.


![Alt text](assets/cnn.png)
![Alt text](assets/cnn2.png)
![Alt text](assets/cnn3.png)
![Alt text](assets/cnn4.gif)
![Alt text](assets/cnn5.png)