# Assignment 2 - Image Captioning

This assignment is designed for the **Deep Network Development** course and focuses on creating, training, and evaluating a **custom image captioning model** while comparing its performance with an existing pre-trained model.

---

## Task Description

Your task is to develop a **custom image captioning model** using an **Encoder-Decoder architecture with Attention** and compare its performance with a pre-trained model.

### **Detailed Steps**

#### 1. **Dataset**
   - Use the **Flickr8k dataset**: [Flickr8k Dataset on Kaggle](https://www.kaggle.com/datasets/adityajn105/flickr8k).
   - Implement a **PyTorch Dataset class** to manage the data.
   - Incorporate **image** and **caption preprocessing**, including:
     - Tokenization of captions.
     - Appropriate padding for batch processing.
   - Split the dataset into **training**, **validation**, and **test** sets.

#### 2. **Model**
   - Create an **Encoder-Attention-Decoder** architecture:
     - **Encoder**:
       - Create a custom layer or use a **pre-trained backbone** (e.g., ResNet) for image feature extraction.
       - Fine-tune the encoder for better performance.
     - **Attention**:
       - Implement an attention mechanism to focus on specific parts of the image (context) during caption generation.
       - Use Linear layers or other techniques of your choice.
     - **Decoder**:
       - Use a sequence-based model (e.g., LSTM) to generate captions based on:
         - Encoder's image features.
         - Attention context.
   - **Extra Points**: Students implementing either of the following will earn extra credit:
     - Vision-based **Transformer** architecture.
     - Transformer-only decoder for the caption generation.

   - **Training**:
     - Define an optimizer, loss function, and the number of epochs.
     - Use **regularization techniques** to prevent overfitting.
     - Note: Points will be deducted for underfitted or overfitted models.
   - **Visualization**:
     - Plot loss and metric progression across epochs.
     - Visualize **attention weights** to demonstrate the learning process.
       - Failure to visualize attention weights will result in losing points.
   - **Evaluation**:
     - Use the **BLEU score** to measure the quality of generated captions.

#### 3. **Existing Model Comparison**
   - Choose a **pre-trained image captioning model**, ideally trained on the **Flickr8k dataset**.
   - Evaluate both your custom model and the pre-trained model on the **test set**.
   - Compare their performance:
     - **Visually**: Show predictions.
     - **Quantitatively**: Present evaluation metrics (e.g., BLEU scores).

---

## Guidelines

- Follow the provided sections in the notebook to guide your implementation, but adapt as needed.
- **Read all instructions carefully** to ensure all requirements are met.
- Avoid using external Python files. **All code must be contained within the notebook**.
- Include the following details at the beginning of your notebook:
  - **Name**
  - **Neptun ID**
- Add explanations throughout your code and results sections:
  - Explain your choices, observations, and any potential improvements.

---

## Defense Preparation

Prepare answers to the following example questions:

1. **Explain the concept of image captioning and its applications.**
2. **What are the components of an Encoder-Decoder architecture, and how do they function in image captioning?**
3. **How does the attention mechanism improve the performance of an image captioning model?**
4. **Discuss the importance of data preprocessing in the context of image captioning.**
5. **What are BLEU scores, and how do they evaluate the performance of an image captioning model?**
6. **Explain how you would address overfitting or underfitting in your model.**
7. **Discuss any potential improvements or alternative approaches you might consider for your model.**
8. **What are the advantages of using Transformer-based architectures for caption generation?**
