# Image Classification Model

This project implements an image classification model using Convolutional Neural Networks (CNNs). The model is trained to classify images into categories based on labeled datasets. A Streamlit app is also included to upload and classify new images in real time.

---

## Features

- Trains a CNN using TensorFlow and Keras
- Handles custom dataset with multiple classes
- Predicts uploaded images via a web app
- Streamlit app with live image upload
- Google Colab support for training and inference

---

## Project Structure

```
image_classification/
├── app.py                    # Streamlit prediction interface
├── image_model.py           # Model training script
├── model.h5                 # Saved Keras model
├── dataset/                 # Image dataset (organized by folder/class)
│   ├── train/
│   └── test/
├── sample_image.jpg         # Optional test image
└── README.md                # Project documentation
```

---

## Technologies Used

- Python 3
- TensorFlow / Keras
- NumPy
- PIL
- Streamlit

---

## How to Run

### Local Machine

1. Clone the repository:
   ```
   git clone https://github.com/your-username/image-classification-model.git
   cd image-classification-model
   ```

2. Install required packages:
   ```
   pip install -r requirements.txt
   ```

3. Train the model:
   ```
   python image_model.py
   ```

4. Start the Streamlit app:
   ```
   streamlit run app.py
   ```

---

### Google Colab

1. Upload the required files (`model.h5`, `app.py`, etc.)
2. Install packages:
   ```python
   !pip install streamlit pyngrok tensorflow
   ```

3. Run app:
   ```python
   from pyngrok import ngrok
   get_ipython().system_raw('streamlit run app.py &')
   print(ngrok.connect(8501))
   ```

---

## Dataset Format

The dataset must be structured like this:

```
dataset/
├── train/
│   ├── class1/
│   └── class2/
├── test/
│   ├── class1/
│   └── class2/
```

Each class folder should contain `.jpg` or `.png` images of that class.

---

## Output

For each uploaded image, the app displays:

- Uploaded image preview
- Predicted class label

---

## License

This project is intended for academic and educational purposes only.

---

## Author

Submitted as part of a Machine Learning Internship Project.
