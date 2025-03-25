# 📄 PDF Resume Text Extraction & Analysis Framework  

## 📌 Project Overview  
This project implements and compares multiple PDF text extraction methods to build a robust **resume analysis pipeline**. It evaluates **extraction accuracy, performance, and quality assessment** while analyzing **resume characteristics, industry trends, and text composition patterns**.  

---

## 🎯 Objectives  
- **Compare multiple PDF extraction methods:** PyMuPDF, PyPDF2, pdfplumber, OCR (Tesseract).  
- **Assess extraction quality:** Text accuracy, layout preservation, and handling of tables/images.  
- **Analyze resume characteristics:** Text length, word count, and distribution across industries.  
- **Benchmark performance:** Speed and accuracy trade-offs for different extraction techniques.  
- **Automate processing:** Develop a **smart extraction pipeline** with quality validation and error handling.  

---

## 🗂 Dataset  
- **Size:** 2,484 resumes  
- **Categories:** 20+ job roles (e.g., IT, Healthcare, Finance)  
- **Content:** Extracted text with metadata (method used, industry, etc.)  
- **Structure:** Mixed formatting quality (scanned & text-based PDFs)  

---

## 🏗 Extraction Pipeline  
1. **Multi-method parallel extraction:** Run multiple extraction methods simultaneously.  
2. **Quality validation checks:** Filter out empty/corrupted extracts.  
3. **Optimal method selection:** Prefer the best-performing extraction method for each document.  
4. **Metadata recording:** Store method details and extraction success rates.  
5. **Progress tracking:** Monitor batch processing efficiency.  

---

# 📈 Extraction Method Performance
| Method       | Speed (ms/page) | Accuracy      | Layout Support | Tables | Images |
|--------------|-----------------|---------------|----------------|--------|--------|
| PyMuPDF      | 50              | ⭐⭐⭐⭐⭐ (99%+)  | ⭐⭐⭐☆☆          | ❌     | ❌     |
| PyPDF2       | 200             | ⭐⭐⭐☆☆         | ⭐☆☆☆☆          | ❌     | ❌     |
| pdfplumber   | 300             | ⭐⭐⭐⭐☆         | ⭐⭐⭐⭐⭐          | ✅     | ❌     |
| OCR (Tesseract) | 2000          | ⭐⭐☆☆☆         | ⭐☆☆☆☆          | ❌     | ✅     |

## 📌 Best Use Cases:
- ✔ **PyMuPDF**: Best for text-based resumes (fastest processing).
- ✔ **PyPDF2**: Good for simple formatted documents but slower.
- ✔ **pdfplumber**: Ideal for resumes with tables/columns.
- ✔ **OCR**: Required for scanned documents but slow.

---

## 🔍 Key Findings:
- ✅ **PyPDF2** dominated (99.96% usage) – Most resumes had simple text formatting.
- ✅ **IT & Healthcare sectors** were the most represented.
- ✅ **Optimal resume length**: 5,600 characters (760 words).
- ✅ **Text skewness detected** – Some resumes were excessively long (33,000+ characters).
- ✅ **No placeholder text found** – Indicates high data quality.

---

## 📊 Resume Analysis Results:
### Resume Length Distribution
- Mean: ~6,000 characters | Median: 5,600 characters
- Skewness: Right-skewed (indicating long-tail distributions)
- Max Length: 33,000 characters

### Word Count Statistics
- Mean: ~810 words | Median: 760 words
- Character-to-word ratio: ~7.4 (higher than the standard 5-6)

### Industry Distribution
- **IT sector dominant** (120 resumes)
- **Healthcare & BPO well-represented**
- **Agriculture & Aviation underrepresented**

---

## 📊 Visualizations:
- **Resume text word cloud** – Identifies most frequently used skills.
- **Category-wise distribution heatmap** – Displays industry representation.
- **Resume length histogram** – Analyzes variation in resume sizes.

---

## 📌 Practical Applications:
- ✔ **Recruitment Optimization** – Identify high-demand skills & industry trends.
- ✔ **Resume Writing Guidelines** – Define ideal length & text composition.
- ✔ **Data Science & NLP** – Build models using structured resume data.
- ✔ **Automated Screening** – Improve applicant filtering through text analytics.

---

## 📜 Conclusion:
This project successfully developed an end-to-end **resume text extraction & analysis framework**. It benchmarked multiple PDF extraction methods, validated data quality, and provided insightful analytics on resume characteristics and industry trends. The methodology serves as a foundation for future HR automation, NLP-based resume parsing, and AI-driven recruitment solutions.

---

## 🏆 Project Success Metrics:
- ✅ **100% extraction coverage**
- ✅ **0% placeholder content**
- ✅ **20+ job categories analyzed**
- ✅ **4 extraction methods evaluated**

---

## 🔗 Future Enhancements:
- Integrate **Named Entity Recognition (NER)** for skill & experience extraction.
- Apply **Machine Learning** for resume classification & ranking.
- Expand dataset to include more diverse resume formats.

---

## 🛠 Installation & Requirements  
Install the required Python libraries:  
```bash
pip install PyMuPDF PyPDF2 pdfplumber pdfminer.six pytesseract pdf2image camelot-py[cv] pandas openpyxl
