# MNIST Digit Classifier

Handwritten digit recognition on the MNIST dataset using a Multilayer Perceptron (MLP) built with TensorFlow/Keras.

## Project Structure
mnist-digit-classifier/

├── notebook/mnist_classifier.ipynb

├── requirements.txt

└── .gitignore
## Pipeline

| Step | Description |
|------|-------------|
| Data Loading | 60,000 train / 10,000 test images via `tf.keras.datasets` |
| EDA | Class distribution analysis, sample visualisation |
| Preprocessing | Flatten 28×28 → 784, normalise to [0, 1] |
| Model | MLP — Dense(128, ReLU) → Dropout(0.2) → Dense(64, ReLU) → Dense(10, Softmax) |
| Evaluation | Accuracy, Loss, Classification Report, Confusion Matrix |

## Model Architecture

| Layer   | Units | Activation | Parameters |
|---------|-------|------------|------------|
| Dense   | 128   | ReLU       | 100,480    |
| Dropout | —     | p = 0.2    | 0          |
| Dense   | 64    | ReLU       | 8,256      |
| Dense   | 10    | Softmax    | 650        |
| **Total** | | | **109,386** |

## Results

| Metric        | Score   |
|---------------|---------|
| Test Accuracy | ~98.2%  |
| Test Loss     | ~0.065  |

## Quick Start

```bash
git clone https://github.com/Leonardo-M-AI/mnist-digit-classifier--updated-.git
pip install -r requirements.txt
jupyter notebook notebook/mnist_classifier.ipynb
```

## Tech Stack
`Python` `TensorFlow/Keras` `scikit-learn` `NumPy` `Matplotlib`

## License
MIT

## Business Impact

A model achieving ~98.2% accuracy on handwritten digit recognition
can automate data entry in banking (cheque processing), postal services
(address sorting), and healthcare (form digitisation), reducing manual
review costs by an estimated 35-60% on digit-heavy workflows.

## What I Would Do Next

- Replace the MLP with a CNN to push accuracy above 99%
- Test on real-world noisy data (not just clean MNIST)
- Deploy the model as a REST API using FastAPI
- Compare MLP vs CNN vs SVM performance in a single notebook
