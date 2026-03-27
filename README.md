# Machine-Learning-Tutorial


  What is this project about?
This project is about building a simple **Autoencoder model** using deep learning.

An autoencoder is a neural network that learns how to:
 **compress data**
 **and then reconstruct it back**

Here, we use it on handwritten digit images to see how well the model can rebuild them.

---

  What I tried to learn
In this project, I focused on one main idea:

 How does the **bottleneck size** affect performance?

I tested different sizes:
- 16 (high compression)
- 32 (balanced)
- 64 (low compression)

---

 Dataset used
- MNIST dataset (handwritten digits 0–9)
- Each image is 28 × 28 pixels
- Converted into 784 values (flattened)

---

 What I did step by step

 1. Data Preparation
- Normalized pixel values (0–255 → 0–1)
- Flattened images
- Created a small CSV file (1000 samples)

---

 2. Model Building
I built a simple autoencoder using TensorFlow/Keras:

- Input → 784 neurons  
- Encoder → 128 → 64  
- Bottleneck → variable size  
- Decoder → 64 → 128 → 784  

---

 3. Training
- Optimizer: Adam  
- Loss function: Mean Squared Error (MSE)  
- Batch size: 256  

---

 4. Experiment
I trained the model with different bottleneck sizes:

| Bottleneck | Result |
|-----------|--------|
| 16 | High compression, more loss |
| 32 | Best balance |
| 64 | Better reconstruction |

---

  Results (What I observed)

- The model was able to reconstruct images quite well  
- Smaller bottleneck → loses some details  
- Larger bottleneck → better image quality  
- Best result came at **32**

---

 Output files

The code generates:
- `graph.png` → shows bottleneck vs loss  
- `reconstruction.png` → original vs reconstructed images  

---

 How to run the code

### Install required libraries:
```bash
pip install tensorflow numpy pandas matplotlib
