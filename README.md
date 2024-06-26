# Rainfall_prediction_using_ANN_and_Advanced_AI_Models

Data Handling
I have utilized data from the IMD Pune website, a public and reliable source of daily rainfall data in India. The dataset includes gridded data at a 0.25° x 0.25° resolution, gathered from approximately 7000 rain gauge stations across the country from 1900-2010. Before quality checking and interpolation, I verified the location information of the stations and corrected any coding and typographic errors. Standard quality control tests were applied to the daily station point rainfall data, including checks for typing and coding errors, missing data, duplicate stations, and extreme values. After these quality checks, the data were interpolated to fixed spatial grid points of 0.25° x 0.25° resolution.

To convert station rainfall data into grid point data, I used spatial interpolation, which assumes spatially distributed station rainfall values are spatially correlated. The daily rainfall over various spatial regions was computed as the area-weighted rainfall over all grid boxes in the region. The area weight assigned to each grid box was the fractional grid box area enclosed by the outer boundaries of the reference region, multiplied by a cosine factor (the cosine of the latitude of the center point of the grid box). This cosine factor accounts for the convergence of the meridians, which lessens the impact of high-latitude grid points representing a smaller area of the globe.

The data from IMD was in netCDF file format, so I converted it to CSV format and analyzed the variables: Rainfall, Latitude, Longitude, and Time. Using various Python libraries, I created an animation depicting rainfall as a heat map for a year. This required marking a rectangular area using the upper right and lower left coordinates.

Artificial Neural Network (ANN)
An Artificial Neural Network (ANN) is a computational model inspired by the human brain’s neural structure. It consists of interconnected nodes (neurons) organized into layers. Information flows through these nodes, and the network adjusts the connection strengths (weights) during training to learn from data, enabling it to recognize patterns, make predictions, and solve various tasks in machine learning and artificial intelligence.

ANN Structure
The ANN consists of multiple layers: input, hidden, and output layers.

Input Layer: Contains all the input nodes (e.g., pixels of an image).
Hidden Layer: Nodes in this layer are calculated using the formula: weights * f(x) + bias. Each node in one layer is linked to each node in the next layer by a weight, and every node in the next layer has a bias. Initially, weights are chosen randomly and optimized as the model runs.
Output Layer: Provides the final prediction or output.
Mathematics of ANN
Loss Matrix: The squared sum of the predicted value and the actual value. After each iteration, the goal is to minimize the cost matrix by manipulating weights and biases.
Gradient Descent: This algorithm minimizes the cost function by iteratively calculating the next point using the gradient at the current position, scaling it by a learning rate, and subtracting the obtained value from the current position. The learning rate (η) controls the step size and has a strong influence on performance. The function must be differentiable and convex for gradient descent to work effectively.
Activation Functions and Optimizers
Activation Layer: Applied at every layer to help make the data unbiased and smooth.
Optimizers: Used to avoid overfitting and ensure the model converges quickly.
This methodology enables efficient handling and prediction of daily rainfall data using advanced AI models and ANN techniques.
