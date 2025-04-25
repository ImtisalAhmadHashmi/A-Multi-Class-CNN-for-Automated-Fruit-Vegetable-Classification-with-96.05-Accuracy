# A-Multi-Class-CNN-for-Automated-Fruit-Vegetable-Classification-with-96.05-Accuracy
🍎🥦 Project Description
This project implements a Convolutional Neural Network (CNN) to classify 36 different types of fruits and vegetables from images. The model achieves high accuracy in distinguishing between similar-looking produce items, making it useful for applications in grocery automation, dietary tracking apps, or agricultural sorting systems.
🔍 What's Happening in This Code
1. Data Preparation
•	Downloads the "Fruit and Vegetable Image Recognition" dataset from Kaggle using kagglehub
•	Loads training, validation, and test sets using TensorFlow's image_dataset_from_directory
•	Images are resized to 256x256 pixels and batched for efficient processing
2. Data Augmentation
•	Implements custom augmentation techniques to improve model generalization:
o	Random brightness adjustment (Bright layer)
o	Random contrast variation
o	Center cropping (80% of original size)
•	Combines original and augmented data for richer training
3. Model Architecture
•	Builds a CNN with:
o	Three convolutional blocks (32, 64, 32 filters) with BatchNorm and MaxPooling
o	Two dense layers (4096 and 512 units) with Dropout for regularization
o	Final softmax output layer for 36-class classification
•	Uses Adam optimizer with learning rate scheduling
4. Hyperparameter Tuning
•	Experiments with different dense layer configurations:
o	Set A: 7200 units → [1800, 900, 512]
o	Set B: 4096 units → [1800, 900, 512]
•	Tracks performance metrics using TensorBoard's HParams plugin
5. Training Infrastructure
•	Implements robust training with:
o	Model checkpointing to Google Drive
o	Epoch tracking to resume training
o	Early stopping to prevent overfitting
o	Learning rate scheduling
o	TensorBoard logging for visualization
6. Evaluation
•	Generates a confusion matrix to analyze model performance
•	Calculates both standard accuracy and top-2 accuracy
•	Visualizes classification results on test images
🌟 Key Features
•	Data Augmentation Pipeline: Custom brightness/contrast adjustments improve model robustness
•	Hyperparameter Exploration: Systematic testing of network architectures
•	Training Resilience: Automatic resume capability from checkpoints
•	Comprehensive Evaluation: Includes both quantitative metrics and visual analysis
🍏 36-Class Classification Capability
The model can distinguish between:
Fruits: apple, banana, grapes, kiwi, lemon, mango, orange, pear, pineapple, pomegranate, watermelon
Vegetables: beetroot, bell pepper, cabbage, capsicum, carrot, cauliflower, chilli pepper, corn, cucumber, eggplant, garlic, ginger, jalepeno, lettuce, onion, paprika, peas, potato, raddish, soy beans, spinach, sweetcorn, sweetpotato, tomato, turnip
📊 Performance Metrics
The model achieves:
•	High categorical accuracy on test set
•	Excellent top-2 accuracy (model usually includes correct answer in top 2 guesses)
•	Balanced performance across all 36 classes (visible in confusion matrix)
🛠️ Technical Stack
•	TensorFlow/Keras for model building
•	KaggleHub for dataset access
•	Google Colab for cloud execution
•	TensorBoard for visualization
•	Matplotlib/Seaborn for plotting
