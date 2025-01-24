# PDF Extractor

PDF Extractor is a web application designed for extracting and processing data from PDF files. The app offers two primary features: extracting data using a conventional method and extracting data using the Gemini AI model for enhanced accuracy. The frontend is built with React and Bootstrap, while the backend utilizes Flask along with various Python libraries for PDF processing and natural language processing (NLP).

---

## Project Structure

- **`app.py`**: The main backend application file managing routes and API endpoints.
- **`gemini_process.py`**: Includes functions for processing PDFs with the Gemini AI model.
- **`process_pdfs.py`**: Contains functions for standard PDF processing.
- **`frontend/`**: Holds the React frontend application.
- **`pdf-parser/`**: Source code for the PDF parser frontend.
- **`build/`**: Build files for the frontend.
- **`uploads/`**: Directory for storing uploaded PDF files.
- **`env/`**: Environment-specific files and dependencies.
- **`requirements.txt`**: Lists Python dependencies for the project.
- **`render.yaml`**: Configuration file for deploying the app using Render.

---

## Key Functionalities

### PDF Upload and Data Extraction

1. **Standard Extraction**:
   - Users can upload PDF files via the frontend interface.
   - The backend processes the uploaded PDF to extract text and relevant details.
   - Extracted information includes fields like Name, Phone Number, and Address.

2. **Gemini AI Extraction**:
   - Users can choose to extract data using the Gemini AI model for greater precision.
   - The backend leverages the Gemini API to process the text and extract details.

---

## Backend Details

- **Framework**: Flask
- **Key Routes**:
  - `/upload`: Handles PDF uploads and extracts data using the standard method.
  - `/extract_with_gemini`: Extracts data using the Gemini AI model.

- **Core Functions**:
  - `extract_text_from_pdf`: Uses pdfplumber to extract text from PDF files.
  - `extract_details`: Employs spaCy's NER model to extract specific details from the text.
  - `extract_details_with_gemini`: Uses the Gemini API for extracting details from the text.

---

## Frontend Details

- **Framework**: React
- **Styling**: Bootstrap
- **Key Features**:
  - Upload PDF files through an interactive interface.
  - Display extracted data in a user-friendly format.
  - Reprocess data extraction using the Gemini AI model for improved results.
- **API Communication**: Axios is used to handle API requests to the backend.

---

## Deployment

- **Link**: [PDF Extractor](https://pdf-extraction-ml.onrender.com)
  - Note: Since this is hosted on a free instance, it may take a few moments to load.

---

## Dependencies

### Python Dependencies
- Flask
- Flask-CORS
- pdfplumber
- spaCy
- google-generativeai

### JavaScript Dependencies
- React
- Bootstrap

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/pdf-extractor.git
   cd pdf-extractor
   ```

2. Install backend dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Start the backend server:
   ```bash
   python app.py
   ```

4. Navigate to the `frontend/` directory and install frontend dependencies:
   ```bash
   cd frontend
   yarn
   yarn run dev
   ```

5. Open the application in your browser at `http://localhost`.

6. Upload a PDF file via the interface and view the extracted data. Optionally, retry extraction using the Gemini AI model for enhanced accuracy.

---

## Contributing

Contributions are welcome! Feel free to open a pull request or an issue for feature suggestions or bug reports.

---

## License

This project is licensed under the MIT License. Refer to the `LICENSE` file for more information.

---

## Acknowledgements

- **Flask** for backend development.
- **React** and **Bootstrap** for the frontend.
- **Gemini API** for advanced PDF data extraction.
- **spaCy** and **pdfplumber** for natural language processing and PDF parsing.

