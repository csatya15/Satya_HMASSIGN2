# Satya Bhaskar Chaliki
# 700769823


# Question 1: Convolution Operations with Different Parameters

# Objective:
To understand the effect of stride and padding in convolution operations on feature map dimensions and values.

# Explanation:
Convolution is a fundamental operation in CNNs, where a kernel (filter) slides over the input image to produce feature maps. The amount by which the filter moves is called stride, and padding refers to how the borders are treated.

We use a fixed 5×5 matrix and a 3×3 kernel. Four convolution operations are performed:

Stride = 1, Padding = VALID: Output shrinks, as no padding is added.

Stride = 1, Padding = SAME: Output size is preserved; zero-padding is applied.

Stride = 2, Padding = VALID: Feature map is smaller due to larger stride and no padding.

Stride = 2, Padding = SAME: Zero-padding offsets stride shrinkage partially.

# Conclusion:
Padding determines output size retention.

Stride controls resolution of the output.

Combining both allows CNNs to balance computation and feature extraction.

# Question 2: CNN Feature Extraction with Filters and Pooling
▶
Task 1: Edge Detection Using Sobel Filters

# Objective:
To implement edge detection using 2D convolution with Sobel filters.

# Explanation:
Edge detection is crucial in feature extraction for detecting object boundaries. Sobel filters approximate gradients:

Sobel X highlights vertical edges.

Sobel Y highlights horizontal edges.

Using OpenCV, we applied each filter separately and visualized the results. This mimics early layers of a CNN that learn edge features from raw pixels.

# Conclusion:
Sobel filters are essential in understanding spatial structure, enabling CNNs to identify shapes and patterns.

▶ Task 2: Max and Average Pooling

# Objective:
To demonstrate how Max and Average Pooling reduce spatial dimensions in feature maps.

# Explanation:
Pooling is a downsampling operation that helps reduce the size of feature maps and controls overfitting:

Max Pooling retains the strongest feature (maximum value).

Average Pooling computes the mean of values in a region.

We applied both on a random 4×4 matrix using a 2×2 kernel.

# Conclusion:
Pooling adds spatial invariance to CNNs.

Max pooling is more commonly used in modern CNNs due to better feature retention.

# Question 3: Data Preprocessing – Standardization vs Normalization

 # Objective:
To explore how preprocessing techniques like normalization and standardization affect model training and accuracy.

# Explanation:
Neural networks are sensitive to input data scale. To ensure stable and efficient learning, inputs must be preprocessed:

Min-Max Normalization rescales data to [0, 1], ensuring bounded input.

Z-score Standardization shifts data to have a mean of 0 and standard deviation of 1.

We applied both techniques on the Iris dataset, visualized feature distributions, and trained a Logistic Regression model.

# Results:
Raw data led to acceptable accuracy.

Normalized and standardized data improved accuracy due to better optimization convergence.

# When to Use:
Normalization is preferred when input data is bounded or using sigmoid/tanh activation.

Standardization is preferred in deep learning (especially with ReLU or batch normalization), as it stabilizes gradients and improves convergence.

# Conclusion:
Preprocessing plays a critical role in model performance. Choosing the right technique based on data distribution and model type is essential for optimal training.
