# Named Entity Recognition (NER) Fine-Tuning

## 📋 Project Overview
This project focuses on fine-tuning BERT model for Named Entity Recognition (NER) using a custom dataset. The goal is to improve entity recognition accuracy in IT domain by leveraging transfer learning on a pre-trained transformer model.

## Dataset
For this project, two datasets from Hugging Face are used:

- **Conll2003 :** This dataset contains English texts annotated with four types of entities: persons, locations, organizations, and miscellaneous entities. It includes approximately 20,000 lines divided into three sets (training, test, validation). Each line represents a word annotated with its grammatical tag (POS), syntactic tag (chunk), and NER tag (e.g., B-PER for a person, I-LOC for a location). It follows a tagging scheme where entities are marked as being inside (I) or at the beginning (B) of an entity.

- **Annotated_NER_PDF_Resumes :** This dataset consists of 5,029 resume (CV) samples, each annotated with IT-related skills. The skills are manually labeled and extracted from PDF files, with the data provided in JSON format.

## 🛠️ Libraries Used
- **Transformers (Hugging Face):** Pre-trained model fine-tuning
- **dataset (Hugging Face):** Loading and pre-processing datasets
- **NLTK:** NLP utilities and tokenization
- **NumPy:** Data handling and manipulation
- **evaluate & seqeval:** Evaluating model performance using diffrent metrics
- **Matplotlib** Visualization of training performance

## 📦 Installation
```bash
# Clone the repository
git clone https://github.com/YacineAitKaci/NER-Fine-tuning.git

# Navigate to the project directory
cd NER-Fine-Tuning

# Install required libraries
pip install transformers[sentencepiece] datasets nltk numpy seqeval evaluate matplotlib 
```

## 🏃 How to Use
1. **Prepare the dataset:** Ensure the path to your 'ResumeJsonAnnotated' dataset is set correctly in the code 
2. **Run the training notebook:**
```bash
jupyter notebook NER_Fine_Tuning.ipynb
```
3. **Evaluate the model:** Inspect precision, recall, and F1-score to assess performance.
4. **Run inference:** Use the fine-tuned model for named entity recognition on new text data.

## 📊 Results & Analysis
- **Fine-tuned Transformer Model:** Improved entity recognition for domain-specific data.
- **Performance Metrics:** Evaluation of model predictions using standard NLP metrics.
- **Visualization:** Loss curves and accuracy trends over training epochs.

## ⚡ Challenges Faced
- Data imbalance and noise in certain entity categories.
- Model overfitting on small datasets.
- Handling token misalignment in transformer-based tokenization.

## 💡 Future Improvements
- Experiment with different pre-trained models (e.g., RoBERTa, DistilBERT).
- Augment training data for better generalization.
- Deploy the trained model as an API for real-time inference.

---

Made with ❤️ for NLP & Machine Learning enthusiasts!

