# Image Classification with MobileNetV2

## Project Overview
This project demonstrates how to build and train an image classification model using transfer learning with a pre-trained MobileNetV2 model. The goal is to classify images into different categories based on a custom dataset.

## Dataset Details
- **Base Path**: /content/drive/MyDrive/Datasets/ML Datasets/dataset
- **Image Size**: (224, 224)
- **Classes**: 4 classes: 100, 1000, 50, 500
- **Training Samples**: 10112 (approx)
- **Validation Samples**: 2176 (approx)
- **Test Samples**: 2176 (approx)

## Model Architecture
- **Base Model**: MobileNetV2 (pre-trained on ImageNet)
- **Input Shape**: (224, 224, 3)
- **Top Layers**: Removed MobileNetV2's original classification head.
- **Custom Classification Head**: 
  - GlobalAveragePooling2D
  - Dropout (0.5)
  - Dense layer with 4 units and 'softmax' activation.
- **Trainable Layers**: Only the custom classification head was trained; the base MobileNetV2 layers were frozen.

## Training Configuration
- **Epochs**: 10
- **Optimizer**: Adam (learning_rate=0.0001)
- **Loss Function**: SparseCategoricalCrossentropy
- **Metrics**: Accuracy

## Evaluation Metrics
After training for 10 epochs, the model achieved the following performance on the test dataset:
- **Test Loss**: 0.9028
- **Test Accuracy**: 0.6733

### Classification Report
```
              precision    recall  f1-score   support

         100       0.68      0.71      0.70       537
        1000       0.60      0.57      0.58       542
          50       0.75      0.77      0.76       544
         500       0.66      0.65      0.65       544

    accuracy                           0.67      2167
   macro avg       0.67      0.67      0.67      2167
weighted avg       0.67      0.67      0.67      2167

```

## Visualizations
The following performance visualizations have been generated and saved as image files:
- `performance_plot.png`: Displays the training and validation accuracy and loss curves over epochs.
- `confusion_matrix.png`: Shows the confusion matrix of the model's predictions on the test set.
- `single_prediction.png`: Illustrates an example prediction on a single test image.

## How to Use the Trained Model
1. Load the model:
   ```python
   import tensorflow as tf
   model = tf.keras.models.load_model('/content/drive/MyDrive/mobilenetv2_trained_model.keras')
   ```
2. Preprocess an image and make a prediction:
   ```python
   import numpy as np
   from PIL import Image
   
   # Assuming 'image_path' is the path to your new image
   img = Image.open(image_path).resize((224, 224))
   img_array = tf.keras.utils.img_to_array(img)
   img_array = tf.expand_dims(img_array, 0) # Create a batch
   
   # Preprocess for MobileNetV2
   img_array = tf.keras.applications.mobilenet_v2.preprocess_input(img_array)
   
   predictions = model.predict(img_array)
   predicted_class_index = np.argmax(predictions[0])
   predicted_class_name = class_names[predicted_class_index]
   print(f"Predicted class: 100")
   ```

## Files to Upload to GitHub
To share this project, please upload the following files to your GitHub repository:
- `mobilenetv2_trained_model.keras` (your trained model weights)
- `performance_plot.png`
- `confusion_matrix.png`
- `single_prediction.png`
- `README.md` (this file)

