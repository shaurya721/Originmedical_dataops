"README.txt " file content for Task 1:  

#   Task 1: Data Extraction, Anonymization, and Analysis    

   Overview    
This project involves extracting text from medical PDF reports, performing Optical Character Recognition (OCR), cleaning and anonymizing the data, extracting metadata, and converting the processed text back into anonymized PDF reports.  

   Tools & Libraries Used    
The following Python libraries were used in this task:  
-   pandas   – Data handling and analysis  
-   numpy   – Numerical computations  
-   matplotlib   – Data visualization  
-   PyPDF2   – PDF manipulation  
-   pdfplumber   – Extracting text from PDFs  
-   reportlab   – Generating PDFs  
-   fpdf   – PDF creation  
-   json   – Handling metadata storage  
-   sqlite3   – Database operations  
-   pdf2image   – Converting PDF pages to images  
-   pytesseract   – Optical Character Recognition (OCR)  
-   pillow   – Image processing  
-   re (regex)   – Extracting structured data from text  
-   Poppler (Required for PDF-to-image conversion)

   Steps Performed    

#   1. Environment Setup    
- Installed the required Python libraries using  "pip ".  
- Verified the installation of all dependencies.  
- Checked for the existence of dataset directories ( "RC1 " and  "RC2 ").  

#   2. PDF Extraction & OCR Processing    
- Identified all PDFs within the dataset.  
- Converted PDF pages into images using  "pdf2image ".  
- Performed OCR on extracted images using  "pytesseract ".  
- Stored the extracted text in  "extracted_text.txt ".  

#   3. Text Cleaning & Preprocessing    
- Applied regex patterns to clean extracted text.  
- Removed unnecessary whitespace and noise.  
- Saved the cleaned text as  "cleaned_text.txt ".  

#   4. Batch Processing of PDFs    
- Iterated through all PDFs in the dataset.  
- Converted them to images and extracted text.  
- Cleaned and stored text outputs for each report.  

#   5. Data Anonymization & Metadata Extraction    
- Generated unique anonymous IDs for each report.  
- Extracted key metadata fields such as:  
  - Gestational age  
  - Patient age  
  - BMI  
  - Examination findings  
- Stored extracted metadata in  "extracted_metadata.json ".  

#   6. Recreating Anonymized PDFs    
- Converted anonymized text files back to PDFs.  
- Ensured the correct use of Times New Roman font.  
- Saved anonymized PDF reports in the dataset.  

#   7. Metadata Analysis & Insights    
- Converted extracted metadata to a structured Pandas DataFrame.  
- Calculated key statistics:  
  -   Average Age    
  -   Average BMI    
  -   Most Common Examination Findings    
- Printed insights for further analysis.  

   Final Output Files    
-   extracted_text.txt   – Raw OCR-extracted text.  
-   cleaned_text.txt   – Processed and cleaned text.  
-   extracted_metadata.json   – Structured metadata from reports.  
-   Anonymized PDFs   – PDF reports with anonymized patient data.  
-   metadata.json   – Final structured metadata file.  
-   Exploratory Analysis Notebook   – Jupyter Notebook with statistical insights.  

   How to Run    
1. Ensure all required libraries are installed using  "pip install -r requirements.txt ".  
2. Update dataset paths if necessary.  
3. Run the Python scripts in sequence for extraction, anonymization, and analysis.  
