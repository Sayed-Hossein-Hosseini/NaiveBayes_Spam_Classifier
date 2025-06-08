# 📧 Spam Detector - Naive Bayes from Scratch

A simple but powerful **Spam Email Classifier** implemented **from scratch** in Python — without using `sklearn`'s built-in models.

This project demonstrates how to build a text classifier using the **Naive Bayes algorithm**, a probabilistic model that works especially well for **text classification** tasks like spam detection.

---

## 🚀 Project Features

✅ Implements **Multinomial Naive Bayes** from scratch  
✅ Uses **Laplace Smoothing** to handle unseen words  
✅ Preprocesses email texts (lowercasing, punctuation removal)  
✅ Calculates **prior** and **conditional** probabilities manually  
✅ Evaluates performance with **accuracy** and **confusion matrix**  
✅ Visualizes the confusion matrix with a **heatmap**  
✅ Saves predictions in a clean **CSV** file ready for analysis  

---

## 🗂️ Dataset

The dataset used is `spam_ham_dataset.csv`, which contains:

- `label` → 'spam' or 'ham' (manually labeled)  
- `text` → the actual email content  
- `label_num` → numerical label (1 = spam, 0 = ham)

---

## ⚙️ How It Works

1. **Preprocessing**:  
   - Convert text to lowercase  
   - Remove punctuation  
   - Tokenize into words  

2. **Training**:  
   - Build a vocabulary  
   - Count word frequencies in spam and ham emails  
   - Calculate prior probabilities P(spam) and P(ham)  
   - Calculate conditional probabilities P(word | spam) and P(word | ham) with Laplace smoothing  

3. **Prediction**:  
   - For each test email, compute:  
     `log(P(spam | email))` and `log(P(ham | email))`  
   - Classify as **spam** or **ham** based on higher log-probability  

4. **Evaluation**:  
   - Calculate **accuracy**  
   - Build and display a **Confusion Matrix**  
   - Visualize it with a **heatmap** using seaborn  

5. **Export**:  
   - Save predictions to a CSV file with a column `"Spam"` containing the predicted labels.

---

## 📊 Example Results

- Accuracy: ~ **98.26%** (depends on random train/test split)
- Example Confusion Matrix:

|               | Predicted Spam | Predicted Ham |
|---------------|----------------|---------------|
| **Actual Spam** | 308            |  6            |
| **Actual Ham**  | 12             | 709           |

---

## 📦 Dependencies

- Python >= 3.7
- pandas
- numpy
- matplotlib
- seaborn

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
````

---

## 📝 Running the Code

1. Clone this repository:

```bash
git clone https://github.com/yourusername/spam-detector-naive-bayes.git
cd spam-detector-naive-bayes
```

2. Run the main Python script (example: `spam_detector.py`):

```bash
python spam_detector.py
```

3. Outputs:

* Accuracy printed in console
* Confusion matrix displayed
* Heatmap shown
* CSV saved as `spam_predictions_from_scratch.csv`

---

## 📚 Learning Purpose

This project was developed as part of a **machine learning exercise** to deeply understand:

* How Naive Bayes works
* How to implement probabilistic models from scratch
* How to evaluate classification models
* How text classification pipelines work

---

## ❤️ Acknowledgements

Dataset inspired by classic **spam detection** tasks.

Project built for the course:

* **Machine Learning Fundamentals**
* Student: **Sayyed Hossein Hosseini DolatAbadi**

---

## 📜 License

This project is released under the [MIT License](LICENSE).

---

✨ **Enjoy this simple yet powerful spam detector!**
Feel free to fork it, improve it, and explore more advanced NLP techniques 🚀.
