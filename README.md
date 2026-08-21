# Roman Urdu vs English Code-Switching NLP Classifier

An end-to-end Natural Language Processing (NLP) pipeline and fine-tuned transformer model for token-level and sequence-level identification of mixed Roman Urdu and English text.

---

### 📌 Why This Matters
In multilingual regions, everyday digital communication heavily features code-switching—blending Roman Urdu with English in casual messages and social media. Off-the-shelf NLP tools typically fail on mixed vocabulary and non-standardized phonetic spelling. This project structures, tokenizes, and accurately classifies code-switched text to enhance downstream NLP tasks like sentiment analysis and machine translation.

---

### 🌐 Live Model & Dataset Links
* **Hugging Face Model:** [https://huggingface.co/Ushna-Alam219/code-switching-codesaviours-si26-ushna](https://huggingface.co/Ushna-Alam219/code-switching-codesaviours-si26-ushna)
* **Hugging Face Dataset:** [https://huggingface.co/datasets/Ushna-Alam219/code-switching-codesaviours-si26-ushna](https://huggingface.co/datasets/Ushna-Alam219/code-switching-codesaviours-si26-ushna)
* **Loom Video Walkthrough:** [Add your Loom Video URL here]

---

### ⚙️ How It Works
1. **Dataset Curation & Preprocessing:** Collected and annotated bilingual Roman Urdu-English code-switched sentences with standardized label schemas.
2. **Tokenization:** Custom multilingual tokenization preserving intra-word morphological boundaries.
3. **Model Fine-Tuning:** Fine-tuned cross-lingual transformer architectures (such as XLM-RoBERTa) for accurate contextual disambiguation.
4. **Evaluation:** Validated on held-out test splits assessing precision, recall, and token classification accuracy.

---

### 📊 Results & Performance
* **Base Architecture:** Multilingual Transformer / XLM-RoBERTa
* **Task:** Token & Sentence Level Code-Switching Detection
* **Performance:** Demonstrates high precision and F1-scores across varied conversational Roman Urdu and English sentences.

---

### 🚀 How to Run Locally

```bash
# 1. Clone the repository
git clone [https://github.com/ushnamalik207-dotcom/code-switching-codesaviours-si26-ushna.git](https://github.com/ushnamalik207-dotcom/code-switching-codesaviours-si26-ushna.git)
cd code-switching-codesaviours-si26-ushna

# 2. Install required dependencies
pip install transformers torch datasets scikit-learn

# 3. Load model via Hugging Face Transformers
from transformers import AutoTokenizer, AutoModelForTokenClassification

tokenizer = AutoTokenizer.from_pretrained("Ushna-Alam219/code-switching-codesaviours-si26-ushna")
model = AutoModelForTokenClassification.from_pretrained("Ushna-Alam219/code-switching-codesaviours-si26-ushna")
