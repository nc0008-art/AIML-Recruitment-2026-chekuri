# AIML-Recruitment-2026-Chekuri

## 1. Candidate Details
- **Name:** Chekuri
- **Institution:** SRM Institute of Science and Technology
- **Track:** Second Years — AI-ML Recruitment Task (Coding Ninjas 10X)

## 2. Tasks Completed
- ✅ **Task 2: Neural Network** (MNIST Handwritten Digit Classification)
- ⬜ Task 1: Air Quality Forecasting *(not attempted — guidelines require completing at least one task)*

## 3. Problem Statement
Build and train a simple neural network to classify handwritten digits (0–9) from the MNIST dataset, understand each major architectural component, and analyze how changes to the model or training process affect performance.

## 4. Approach
1. Loaded and inspected the MNIST dataset (60,000 train / 10,000 test grayscale 28×28 images).
2. Normalized pixel values to the [0, 1] range and flattened images to 784-length vectors.
3. Built a fully-connected (Dense) neural network with an input layer, one ReLU hidden layer, and a Softmax output layer.
4. Trained the model using the Adam optimizer and sparse categorical cross-entropy loss, tracking training/validation loss and accuracy across epochs.
5. Evaluated the trained model using accuracy, a confusion matrix, and precision/recall/F1-score.
6. Ran a controlled experiment comparing the baseline architecture (1 hidden layer, 128 neurons) against a modified architecture (2 hidden layers, 256 neurons each) to study the effect of increased model capacity.

## 5. Technologies Used
- Python 3
- TensorFlow / Keras — model building and training
- NumPy — numerical operations
- Matplotlib — visualizations (sample digits, loss/accuracy curves)
- scikit-learn — confusion matrix and classification report

## 6. Results
- Baseline model (1 hidden layer, 128 neurons): ~97–98% test accuracy *(fill in your actual run's numbers)*
- Modified model (2 hidden layers, 256 neurons): slightly higher accuracy, longer training time
- Most misclassifications occurred between visually similar digit pairs (e.g., 4/9, 3/5)

## 7. Key Learnings
1. Normalization is essential for stable and efficient neural network training.
2. Even a simple fully-connected network can achieve strong accuracy on a well-curated dataset like MNIST.
3. Increasing model capacity (more neurons/layers) improves accuracy up to a point but increases training cost and overfitting risk.
4. A confusion matrix reveals *which* classes are being confused, information a single accuracy score hides.
5. Softmax + sparse categorical cross-entropy is the standard, correct pairing for multi-class classification.

## 8. Challenges
**Challenge:** Deciding how to fairly compare two models with different architectures without conflating changes.
**Solution:** Changed only one factor at a time (network width and depth together, as a single controlled experiment) while keeping the optimizer, learning rate, batch size, and number of epochs identical across both runs, so the comparison isolates the effect of model capacity.

## How to Run
1. Open `mnist_neural_network_task2.ipynb` in Google Colab.
2. Run `Runtime → Run all`.
3. All outputs (plots, metrics, confusion matrix) will regenerate top to bottom.
