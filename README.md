# Brain Tumor Classifier

NeuroScan AI is a deep learning-based web application that detects and classifies brain tumors from MRI images. This project uses image preprocessing and a trained classification model based on VGG16 to help identify tumor types and support early medical diagnosis.

## Features

- Real-time brain tumor classification using a pre-trained deep learning model  
- Simple and responsive web interface built with Flask  
- Drag-and-drop image upload support  
- Displays model prediction and confidence score  
- Generates PDF report for predictions  

## Tech Stack

- **Backend**: Python, Flask  
- **Deep Learning**: TensorFlow, Keras (VGG16)  
- **UI**: HTML (Jinja2 Template), CSS, JavaScript  
- **Image Files**: `.jpg` MRI scans  
- **Model File**: `model.h5`  

## Project Structure

```
brain-tumor-detector/
├── app.py                                # Main Flask application
├── brain-tumor-detection-using-deep-learning.ipynb  # Jupyter Notebook (training)
├── model.h5                              # Trained deep learning model
├── requirements.txt                      # Python dependencies
├── templates/
│   └── index.html                        # HTML template for the frontend
├── uploads/                              # Uploaded MRI images
│   ├── Te-gl_0010.jpg                    # Glioma example
│   ├── Te-me_0010.jpg                    # Meningioma example
│   ├── Te-no_0010.jpg                    # No Tumor example
│   └── Te-pi_0010.jpg                    # Pituitary example
```

## How to Run

1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the Flask application:
   ```bash
   python app.py
   ```

3. Open your browser and go to:
   ```
   http://localhost:5000/
   ```

## Usage

- Upload a brain MRI image using the input field.
- Click on the "Predict" button.
- The model will output the tumor class (e.g., **Glioma**, **Meningioma**, **No Tumor**, **Pituitary**) along with the prediction confidence.
- Optionally, download the result as a PDF report.

## Notes

- `model.h5` is a VGG16-based model trained on brain MRI images.
- Images are preprocessed (resized, normalized) before being passed to the model.
- The uploaded images are stored temporarily in the `uploads` directory for processing.

## Future Improvements

- Add support for DICOM and 3D MRI scans  
- Enable batch predictions for hospitals and clinics  
- Deploy on cloud with secure API endpoints  
- Add multilingual support and accessibility improvements  

## License

This project is for educational purposes and is open-source under the MIT License.
