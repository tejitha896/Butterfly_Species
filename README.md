# butterfly_speciesProject Title: Enchanted Wings - Marvels of Butterfly Species

📌 Project Summary
------------------------------------------------------------
"Enchanted Wings" is a butterfly image classification system that leverages deep learning and computer vision to identify butterfly species from images. This application uses a pre-trained VGG16 model (fine-tuned with custom data of 50+ butterfly classes) and is deployed through a user-friendly Flask web interface.

The goal is to support biodiversity research, ecological education, and citizen science efforts through AI-powered species recognition.

------------------------------------------------------------
📁 Folder Structure
------------------------------------------------------------
Butterfly_app_Details/
├── app.py                 → Flask backend for classification
├── train_model.ipynb      → Jupyter notebook used to train the model
├── vgg16_model.h5         → Trained Keras model
├── class_dict.csv         → Mapping of class IDs to butterfly names
├── requirements.txt       → Python dependencies
├── templates/
│   ├── index.html         → Image upload form
│   └── result.html        → Result display after prediction
└── static/
    └── uploads/           → Temporary image storage for uploaded files

------------------------------------------------------------
🛠️ Setup & Running Instructions
------------------------------------------------------------
1. Open your terminal or CMD
2. Navigate to the app folder:

   cd path\to\Butterfly_app_Details

3. (Optional) Create and activate a virtual environment:
   python -m venv venv
   venv\Scripts\activate  # Windows

4. Install all required dependencies:
   pip install -r requirements.txt

5. Run the Flask server:
   python app.py

6. Open your browser and go to:
   http://127.0.0.1:5000

------------------------------------------------------------
🧪 Usage Description
------------------------------------------------------------
✅ Step 1: On the homepage, upload a butterfly image (JPG/PNG).  
✅ Step 2: Click the "Classify Butterfly" button.  
✅ Step 3: The system will display:
   - The predicted butterfly species
   - The confidence level of prediction
   - A preview of the uploaded image

✅ Step 4: Option to "Upload Another Image" for testing more samples.

⚠️ Image will be resized to 224x224 before classification (as required by the model).

------------------------------------------------------------
📊 Model Details
------------------------------------------------------------
- Base Model: VGG16 (ImageNet weights)
- Input Image Size: 224x224 pixels
- Fine-Tuned on: 50 butterfly species (6,499 total images)
- Optimizer: Adam
- Accuracy: 97.59%
- Format: Saved as .h5 using Keras

------------------------------------------------------------
🌍 Application Scenarios
------------------------------------------------------------
- 🦋 **Biodiversity Monitoring**: Track and record butterfly populations in a region.
- 📚 **Educational Tools**: Help students and enthusiasts learn about butterfly species.
- 🌱 **Citizen Science Projects**: Enable the public to participate in species documentation.

------------------------------------------------------------
🧠 Technologies Used
------------------------------------------------------------
- Python
- TensorFlow & Keras
- Flask
- HTML/CSS (Frontend)
- Pandas & NumPy
- OpenCV / PIL (image preprocessing)


------------------------------------------------------------
✅ Final Notes
------------------------------------------------------------
- Make sure class_dict.csv and vgg16_model.h5 are present in the same directory as app.py
- Upload only valid butterfly images
- Do not rename files unless you update the code accordingly

Thank you for reviewing this project!
