# Home-Assignment-1

Name:Sushma Veluru
700#: 700765390
CRN: 23848



MNIST Model Training with Adam & SGD Optimizers

**Overview**
This project demonstrates training a neural network on the MNIST dataset using two different optimizers: Adam and SGD. It logs training performance using TensorBoard and provides accuracy comparisons.

Steps to Run the Project

1. Load and Preprocess the MNIST Dataset
- The dataset is automatically loaded using `tensorflow.keras.datasets.mnist`.
- The images are normalized by dividing pixel values by 255.0.

2. Build the Neural Network Model
- The model consists of:
  - A `Flatten` layer to convert 28x28 images into a 1D array.
  - A `Dense` layer with 128 neurons and ReLU activation.
  - A final `Dense` layer with 10 neurons (one per digit) using softmax activation.

3. Create a TensorBoard Logging Callback
- Logs are stored in the `logs/fit/` directory with timestamps.
- TensorBoard is configured to record histograms for better visualization.

4. Train the Model with Adam Optimizer
- The model is compiled with:
  - Loss: `sparse_categorical_crossentropy`
  - Optimizer: `Adam`
  - Metric: `accuracy`
- The model is trained for 5 epochs with validation data.

5. Train the Model with SGD Optimizer
- The same model architecture is used.
- The optimizer is changed to `SGD`.
- The model is trained for 5 epochs with validation data.

6. Compare Training and Validation Accuracy
- The accuracy curves for Adam and SGD optimizers are plotted using Matplotlib.
- The trends help assess which optimizer performs better.

7. Analyze Results Using TensorBoard
- Run the following command to launch TensorBoard:
  ```sh
  tensorboard --logdir=logs/fit
  ```
- This enables visualization of loss and accuracy trends.
- Overfitting can be detected if validation accuracy diverges from training accuracy.

Expected Outcome
- The model should train for 5 epochs and store logs in `logs/fit/`.
- The TensorBoard dashboard should show training vs. validation accuracy and loss.
- The accuracy plot should illustrate performance differences between Adam and SGD.

Notes
- Increasing the number of epochs may improve training accuracy but risks overfitting.
- Regularization techniques (e.g., dropout) can help mitigate overfitting.
- The choice of optimizer significantly impacts model convergence speed and final accuracy.

Requirements
- TensorFlow
- Matplotlib
- TensorBoard

To install missing dependencies, run:
```sh
pip install tensorflow matplotlib
```
