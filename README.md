# **Herb Purity Checker**

The **Herb Purity Checker** is a machine learning-powered real-time system designed to classify the medicinal herb *Marsdenia tenacissima* (Murva) into three categories—**Pure**, **Adulterated**, and **Impure**. This project uses a fine-tuned **VGG-16 model** for classification and OpenCV for real-time camera integration. It includes a dashboard for visualizing predictions and confidence levels.

---

## **Table of Contents**

1. [Features](#features)  
2. [Dependencies](#dependencies)  
3. [Dataset Structure](#dataset-structure)  
4. [Setup and Installation](#setup-and-installation)  
5. [Usage](#usage)  
6. [Workflow](#workflow)  
7. [Visualization](#visualization)  
8. [Future Scope](#future-scope)  
9. [Acknowledgments](#acknowledgments)

---

## **Features**

- **Real-Time Analysis**: Capture images via a live camera feed and classify their purity in real-time.  
- **Deep Learning Integration**: Fine-tuned VGG-16 model for robust classification.  
- **Visualization Dashboard**: Provides detailed analysis, including bar charts, pie charts, and confidence levels.  
- **Ease of Use**: Simple interface for training, testing, and prediction.  

---

## **Dependencies**

Install the following Python libraries:

```bash
pip install tensorflow opencv-python matplotlib pillow numpy
```

Additional tools:  
- Python 3.10+  
- A compatible camera module or USB camera.  
- GPU support (optional but recommended for training).  

---

## **Dataset Structure**

Organize the dataset as follows:

```
dataset/
├── train/
│   ├── Pure/
│   ├── Adulterated/
│   ├── Impure/
├── validation/
│   ├── Pure/
│   ├── Adulterated/
│   ├── Impure/
└── test/
    ├── Pure/
    ├── Adulterated/
    ├── Impure/
```

Ensure each folder contains images of the respective class for training, validation, and testing.

---

## **Setup and Installation**

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/herb-purity-checker.git
   cd herb-purity-checker
   ```

2. Install the dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3. Prepare your dataset by organizing it in the specified structure.

4. (Optional) Ensure your system has a camera module connected and accessible by OpenCV.

---

## **Usage**

### **Training the Model**
To train the VGG-16 model on your dataset:
1. Run the following command:
   ```bash
   python main.py
   ```
2. Choose option `1` (Train the Model) in the menu.
3. Specify the batch size and number of epochs when prompted (default: 32 and 10).  
4. The trained model will be saved as `murva_purity_model.h5`.

---

### **Testing the Model**
To evaluate the model's accuracy on the test dataset:
1. Run the script:
   ```bash
   python main.py
   ```
2. Choose option `2` (Test the Model).

---

### **Real-Time Prediction**
To classify herbs in real-time using a camera:
1. Run the real-time checker:
   ```bash
   python main.py
   ```
2. The system will display predictions on the video feed.  
3. Press `v` to visualize predictions in a dashboard.  
4. Press `q` to exit.

---

## **Workflow**

1. **Capture Herb Image**: The system captures images from a live camera feed or uses test images.  
2. **Preprocess Image**: Resize and normalize images for VGG-16 input requirements.  
3. **Predict Using Model**: The trained model predicts the purity category with confidence percentages.  
4. **Display Results**: Results are shown on the video feed and through a detailed visualization dashboard.

---

## **Visualization**

The project includes a detailed dashboard that provides:  
- **Purity Distribution**: A bar chart showing confidence percentages for each category.  
- **Overall Purity**: A pie chart displaying the ratio of `Pure` vs. other categories.  
- **Sample Image Display**: The processed herb image used for analysis.

---

## **Future Scope**

1. Expand the system to classify more medicinal herbs.  
2. Integrate IoT for remote quality control.  
3. Optimize the model for edge devices like Raspberry Pi.  
4. Add real-time alerts for impurity detection.  
5. Incorporate blockchain for herb traceability in supply chains.

---

## **Acknowledgments**

We would like to acknowledge the use of the following tools and frameworks:  
- TensorFlow/Keras for building and training the model.  
- OpenCV for real-time camera integration.  
- Matplotlib and PIL for visualization and image handling.  
- VGG-16 model pre-trained on ImageNet.  

Feel free to contribute to this project by submitting a pull request or opening an issue. Let us know if you have any questions or suggestions!
