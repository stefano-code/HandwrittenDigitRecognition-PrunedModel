# HandwrittenDigitRecognition-PrunedModel
This project shows how to build, optimize, and deploy a neural network for handwritten digit recognition.

We start from a simple model trained on MNIST…  
and then we make it smaller and more efficient using:

👉 Pruning  
👉 Quantization  

At the end, we obtain a model ready to run on edge devices 📱

---

# 🧠 What This Project Does

- Loads the MNIST dataset (handwritten digits)
- Trains a simple neural network (MLP)
- Applies pruning to remove unnecessary weights
- Fine-tunes the model after pruning
- Converts the model to TensorFlow Lite
- Applies dynamic quantization
- Exports a lightweight `.tflite` model

---

# 📊 The Dataset

We use the **MNIST dataset**, one of the most famous datasets in machine learning.

It contains:

- 60,000 training images  
- 10,000 test images  
- Each image is 28 × 28 pixels  

👉 MNIST is often called the **“Hello World” of Deep Learning**

---

# 🧱 The Model

The model is a simple neural network:

- Input: 28 × 28 image → flattened to 784 values  
- Hidden layer: 512 neurons (ReLU)  
- Output layer: 10 classes (Softmax)  

Even if it is simple, it can reach:

👉 ~98% accuracy on test data

---

# ✂️ Pruning — Making the Model Smaller

After training, we apply **pruning**.

Pruning removes weights that are not important.

👉 Many connections in the network have very small values  
👉 These connections do not contribute much  

So we remove them.

The result:

- fewer parameters  
- smaller model  
- same (or similar) accuracy  

---

# 🔄 Fine-Tuning After Pruning

After pruning, the model needs to adjust.

We train it again for a few epochs.

👉 This step is very important  

It helps the model recover performance after removing connections.

---

# ⚡ Quantization — Making the Model Faster

After pruning, we apply **dynamic quantization**.

This reduces the precision of the weights:

👉 from float32 → to smaller representations

The result:

- smaller file size 📦  
- faster inference ⚡  
- better performance on mobile devices 📱  

---

# 📦 Final Output

At the end of the process, we generate:

👉 `digit_recognition_pruned_quant.tflite`

This model is:

- optimized  
- lightweight  
- ready for deployment on edge devices  

---

# 🚀 How to Run (Google Colab)

1. Open the notebook in Google Colab  
2. Run all cells step by step  
3. At the end, download the `.tflite` file  

---

# 🛠️ Technologies Used

- Python  
- TensorFlow / Keras  
- TensorFlow Model Optimization Toolkit  
- TensorFlow Lite  

---

# 🧪 Workflow Summary

1. Train model  
2. Apply pruning  
3. Fine-tune model  
4. Remove pruning wrappers  
5. Convert to TFLite  
6. Apply quantization  
7. Export model  

---

# 📱 Why This Matters (AI on Edge)

In this project:

- The model is trained on a computer 💻  
- Then optimized and compressed  
- Then prepared to run on a device 📱  

👉 This is the idea of **AI on Edge**

No cloud.  
No delay.  
Real-time intelligence on the device.

---

# 💡 Final Thought

At the beginning, the model learns everything.

Then we simplify it.  
We remove what is not needed.  
We make it lighter.

And in the end…

👉 we bring intelligence out of the lab  
👉 and into real devices 🚀
