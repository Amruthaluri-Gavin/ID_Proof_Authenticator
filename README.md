# ID Proof & Face Verification System

A web application built with Streamlit that verifies a user's identity by comparing a live photo from their webcam against their ID card. This app uses facial recognition for matching and OCR to extract text from supported ID cards.

![Demo Gif (Coming Soon)]() ## Features

* **Interactive Web UI:** Built with Streamlit for a simple and easy-to-use interface.
* **Live Webcam Capture:** Uses `st.camera_input` to capture a live selfie for verification.
* **Dual Verification Mode:**
    * **College ID:** Performs both facial verification and OCR text extraction (specifically configured for SRM AP college IDs in the current code).
    * **Other ID Proof:** Performs facial verification only.
* **Facial Recognition:** Employs the `deepface` library to detect faces in both images and calculate a similarity score.
* **Text Extraction (OCR):** Uses `pytesseract` to scan the ID card and extract textual information like Name, Roll Number, and Branch.
* **Instant Results:** Displays the similarity score and a clear **"✅ MATCH CONFIRMED"** or **"❌ MISMATCH DETECTED"** status based on the match threshold.

## Tech Stack

* **Language:** Python
* **Web Framework:** Streamlit
* **Facial Recognition:** `deepface`
* **Text Extraction (OCR):** `pytesseract`
* **Image Processing:** `opencv-python`, `Pillow`, `scipy`
* **Face Detection:** `mediapipe`, `opencv-python`

## How to Run

### Prerequisites

1.  **Python 3.8+**
2.  **Tesseract OCR Engine:** You must have Tesseract installed on your system.
    * [Windows Installation Guide](https://github.com/tesseract-ocr/tessdoc/blob/main/Installation.md)
    * On macOS: `brew install tesseract`
    * On Linux: `sudo apt-get install tesseract-ocr`
3.  **Update Tesseract Path (If Needed):**
    * After installing, find the `tesseract.exe` path (e.g., `r'C:\Program Files\Tesseract-OCR\tesseract.exe'` on Windows).
    * Update the `TESSERACT_PATH` variable at the top of `app.py` with this path.

### Local Setup

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Create a virtual environment:**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    ```sh
    pip install -r requirements.txt
    ```

4.  **Run the Streamlit app:**
    ```sh
    streamlit run app.py
    ```

5.  Open your browser and go to `http://localhost:8501`.
