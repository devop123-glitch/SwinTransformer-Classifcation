# SwinTransformer-Classifcation
📌 Project Overview

This project presents a custom implementation of a Swin Transformer–based deep learning framework for multi-class medical image classification, focusing on renal and liver datasets. The model is designed to efficiently capture both local spatial features and global contextual relationships using shifted window self-attention, making it well-suited for high-resolution medical imaging tasks.

###🧠 Model Architecture

The architecture follows a hierarchical transformer design, consisting of:

Patch Embedding Layer: Converts input images into non-overlapping patches using convolution, reducing spatial dimensions while increasing feature richness.
Swin Transformer Blocks: Utilize window-based multi-head self-attention (W-MSA) and shifted window attention (SW-MSA) to model intra-window and cross-window dependencies efficiently.
Patch Merging Layers: Gradually reduce spatial resolution while increasing channel depth, enabling hierarchical feature learning similar to CNNs.
MLP Layers & Layer Normalization: Applied within each block to enhance feature transformation and stability.
Final Classification Head: Aggregates global features and maps them to output classes.

This design significantly reduces computational cost compared to standard Vision Transformers while maintaining strong representational power.

###⚙️ Training Pipeline

The project includes a fully modular PyTorch training pipeline with:

Data Augmentation: Random rotations, flips, and resizing to improve generalization.
Efficient Data Loading: Using PyTorch DataLoader with batching and parallel workers.
Class Imbalance Handling: Weighted cross-entropy loss based on dataset distribution.
Optimization Strategy: Adam optimizer with weight decay for stable convergence.
Learning Rate Scheduling: Adaptive reduction using ReduceLROnPlateau.
Early Stopping Mechanism: Prevents overfitting by monitoring validation loss.
###📊 Evaluation & Metrics

Model performance is evaluated using a comprehensive set of metrics:

Accuracy, Precision, Recall, F1-score
Sensitivity (True Positive Rate)
Specificity (True Negative Rate)
ROC-AUC Curves
Confusion Matrix Visualization

Additionally, the project includes visualization of incorrect predictions, helping to analyze model weaknesses and improve interpretability.

###🚀 Key Features
Custom implementation of Swin Transformer from scratch
Efficient window-based attention mechanism
Robust handling of class imbalance
End-to-end training, validation, and testing pipeline
Advanced evaluation and visualization tools
Scalable and modular design for experimentation

### Classification
Train
Loss: 0.4392
Acc: 0.8230
Prec: 0.8234
Recall: 0.8230
F1: 0.8226
specificity: 0.9409
sensitivity: 0.8247


Val 
Loss: 0.5974
Acc: 0.7911
Prec: 0.7946
Recall: 0.7911
F1: 0.7920
specificity: 0.9304
sensitivity: 0.7911

Test 
Loss: 0.5763
Acc: 0.7832
Prec: 0.7843
Recall: 0.7832
F1: 0.7830

### results
<img width="960" height="429" alt="AdobeExpressPhotos_9ad2f666c1d547ef842276980ab09548_CopyEdited" src="https://github.com/user-attachments/assets/6015553b-91b2-4a4d-aca7-17069ac6d2a9" />

<img width="624" height="563" alt="AdobeExpressPhotos_65bd6096a6c746399516b735d2e8a880_CopyEdited" src="https://github.com/user-attachments/assets/766964ef-0337-4249-91c7-5fc5644fd51c" />

<img width="507" height="291" alt="AdobeExpressPhotos_5d02b3e877904239b198cde7ada0be11_CopyEdited" src="https://github.com/user-attachments/assets/1dddb81f-201d-4ace-bf5b-32052d3180f7" />

<img width="925" height="394" alt="AdobeExpressPhotos_143e83ce75054aabb0e93c8a9d90965b_CopyEdited" src="https://github.com/user-attachments/assets/1a7bb2bc-c800-4dcf-b5ea-35366d121639" />

<img width="921" height="381" alt="AdobeExpressPhotos_cdc8ae1ce44e499f95655d71ef4d1798_CopyEdited" src="https://github.com/user-attachments/assets/c4b45eee-5468-4146-a725-4c10d637771a" />



🎯 Conclusion

This project demonstrates how transformer-based architectures like Swin Transformer can be effectively adapted for medical image classification tasks, providing a balance between computational efficiency and high predictive performance. It serves as a strong foundation for further research in medical AI, computer vision, and deep learning optimization.
