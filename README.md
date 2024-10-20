# Smart-Vision-Technology
 CNN-based model for automated brand recognition from product images. It accurately classifies brands and uses OCR to extract product details like MRP and expiry dates.



 #Objectives:-
1. Brand Recognition: Accurately classify product images into corresponding brands.
2. Automation: Simplify the process of identifying product brands by eliminating the need for manual input.
3. Efficiency: Build a scalable solution that can handle large datasets and produce real-time predictions.
4. Preprocessing for OCR: Use Optical Character Recognition (OCR) as a supplementary technique to extract product details like MRP, manufacturing, and expiry dates.



 #Methodology:-

1. Data Collection and Preprocessing: 
   - We used datasets containing images of products categorized by brands.
   - Data augmentation techniques like rescaling, flipping, and zooming were applied using ImageDataGenerator to increase dataset variability and improve the model's generalization ability.

2. Model Architecture:
   - A custom CNN model was designed with multiple convolutional layers to extract key features from the images.
   - The model architecture includes three convolutional layers, each followed by max pooling to down-sample the image and reduce computational complexity.
   - The final layers include fully connected Dense layers with Dropout to prevent overfitting.
   - The output layer uses a softmax activation function to handle multi-class classification, with each class representing a different brand.

3. Training and Validation:
   - The dataset was split into training and validation sets, with an 80-20 split.
   - The model was trained for 10 epochs using Adam optimizer with categorical cross-entropy as the loss function.
   - The performance was tracked by validation accuracy and loss, with validation accuracy reaching high performance over the training iterations.

4. OCR Integration:
   - For additional product information extraction, Tesseract OCR was used to extract text from product labels.
   - The text extraction was enhanced by preprocessing images with techniques like grayscale conversion and thresholding.

5. Prediction:
   - The model was tested with new images that were uploaded, preprocessed, and then passed through the trained CNN model for brand recognition.
   - Predictions were made with high accuracy, and the system could correctly classify the product brand from the image.



 #Results:-
- Accuracy: The model achieved a high validation accuracy of over 90%, demonstrating its ability to distinguish between different product brands.
- Freshness Detection: An additional module was developed to detect product freshness using a heuristic based on image brightness, which provided insights into the visual state of fresh produce.
- Text Extraction: OCR successfully extracted key product details, including brand name, pack size, MRP, and expiry dates, with a reasonable accuracy after image preprocessing.




