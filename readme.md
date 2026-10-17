# Residual Attention Network! Fault Diagnosis Model Based on CWT+Residual-Attention

Preface: To address the issues of non-stationary fault vibration signals, complex local frequency band characteristics, and difficulties in effectively highlighting key discriminative regions with conventional convolutional neural networks (CNNs), this issue proposes a fault diagnosis framework based on Continuous Wavelet Transform (CWT) and Residual Attention Network (RAN). The method first converts the raw one-dimensional fault signal into a two-dimensional time-frequency image to preserve the temporal-frequency joint features during the fault evolution. Subsequently, it employs Residual Attention-56 for feature extraction and classification. By introducing attention modules at different levels, the model enhances its response to critical fault time-frequency regions while suppressing irrelevant background interference. Additionally, we provide comparative experiments between VGG and ResNet to facilitate comparison learning.
● Dataset: CWRU West Reserve University Bearing Dataset
1. Model Introduction
\t1.1 \tResidual Attention Introduction\tThe problem addressed in the paper is not "How to simply add an attention module after a classification network," but rather: How to systematically integrate the attention mechanism into deep feedforward convolutional networks, enabling end-to-end training and continuous performance improvement as the network depth increases. The core model proposed in the paper is Residual Attention Network (RAN), which fundamentally involves repeatedly stacking multiple Attention Modules (ALM) along the main branch of the convolution feature extraction path, allowing different layers to learn attention at different scales and semantic levels.
The Residual Attention Network is composed of multiple Attention Modules stacked together. Each Attention Module consists of two branches: (1) Trunk Branch, which is responsible for conventional feature extraction; (2) Mask Branch, which utilizes a bottom-up top-down (bottom-up to top-down) encoder-decoder structure to generate a soft mask, recalibrating the features from the trunk branch.
1.2 Innovation
1. Innovation Point 1: Proposes a CWT-Residual Attention classification method for non-stationary fault signal diagnosis, which enhances the model's ability to model time-frequency local anomalies by integrating continuous wavelet transform with deep residual attention mechanisms.
2. Innovation Point 2: Addressing the characteristic of key discriminative information in fault time-frequency images often being concentrated in specific frequency bands, transient energy, and texture edges, uses multi-layer soft attention mechanisms in Residual Attention for reweighting time-frequency features, thereby strengthening the response capability to sensitive areas of faults. The attention module in the original Residual Attention network can learn different types of attention at different layers and achieve better performance through mixed attention.
3. Innovation Point 3: By comparing with typical image classification models such as VGG and ResNet, and combining confusion matrices and model evaluation, the system evaluates the performance advantages and applicability boundaries of Residual Attention in fault diagnosis scenarios, providing experimental basis for subsequent fault diagnosis network design.
4. Innovation Model Code Structure
2. Data Loading and Preprocessing
2.1 Import Data
Referencing previous articles, preprocess the fault 10 classification data, using the KSU bearing data 10 classification dataset:
train_set, val_set, test_set are divided into training set, validation set, and testing set according to a ratio of 7:2:1, and finally save the data.
2.2 Convert Fault Signals to Continuous Wavelet Transform Time-Frequency Images
3. Based on CWT+Residual-Attention Fault Diagnosis Model
3.1 Define the network model, set parameters, and train the model
50 epochs, accuracy 100%, significantly improved classification results with CWT+Residual-Attention network. It effectively extracts critical features from fault signal characteristics for model recognition, achieving significant results!
3.2 Model Evaluation
(1) Accuracy, Precision, Recall, F1 Score
(2) Failure Classification Confusion Matrix:
(3) Classification Label Visualization
(4) Original Data t-SNE Feature Visualization
(5) t-SNE feature visualization after model training:
3.3 Model Comparison
(1) Training visualization comparison
\t  
(2) Model Accuracy Comparison
\t  
The chart presents the classification results of VGG, ResNet, and Residual Attention models on the Western Reserve University bearing dataset. It is evident that the Residual Attention model outperforms its comparative counterparts in terms of Accuracy, Macro-F1, and Recall metrics, indicating that introducing an explicit attention mechanism in fault time-frequency image classification tasks enhances feature discrimination capabilities. Compared to VGG, Residual Attention not only possesses stronger hierarchical feature extraction abilities but also can adaptively enhance critical fault areas through the mask branch; compared to ResNet, its advantages are primarily reflected in selective modeling of local time-frequency textures and key frequency bands.
Click to download: Complete original data, Python code
2. Friends who enjoy the content can follow, give the article a "like", share on social media or discuss in groups.
Previously Featured Content:
Rapid Document | Parallel Fault Diagnosis Model Based on 2D-SWinTransformer+1D-CNN-SENet
Significant update on bearing life prediction! New ensemble of CNN-BiGRU-Attention models + enriched visualization charts.
Multimodal - Fault Diagnosis | Big Kernel Convolutions Open a New Era in Visualization!
Superior! Direct writing in Area One! Fault diagnosis model based on SSA+Informer-SENet.
Multi-source Information Fusion: Data layer fusion + feature layer fusion fault diagnosis models!

## Images

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
