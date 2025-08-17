# 🛡️ Spam Email Detection System

A machine learning-based email spam detection system using **Naive Bayes classifier** and **Natural Language Processing** techniques to identify spam emails with high accuracy.

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [How It Works](#how-it-works)
- [Project Structure](#project-structure)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project implements a **spam email detection system** using machine learning techniques. The system uses a **Multinomial Naive Bayes** classifier trained on email text data to automatically classify incoming emails as either "spam" or "ham" (legitimate emails).

## ✨ Features

- **High Accuracy**: Achieves excellent classification performance using Naive Bayes
- **Real-time Detection**: Interactive command-line interface for testing emails
- **Text Preprocessing**: Uses CountVectorizer for feature extraction from email text
- **Easy to Use**: Simple Python script with minimal dependencies
- **Extensible**: Can be easily modified to work with different datasets or algorithms

## 📊 Dataset

The project uses the **SMS Spam Collection Dataset** (`spam.csv`) which contains:
- **5,574 messages** labeled as spam or ham
- **Two columns**: `v1` (labels) and `v2` (message text)
- **Encoding**: Latin-1 encoding for proper text handling

### Dataset Structure:
```
v1    | v2
------|------------------------------------------
ham   | "Go until jurong point, crazy.. Available only ..."
spam  | "Free entry in 2 a wkly comp to win FA Cup final ..."
ham   | "U dun say so early hor... U c already then say..."
```

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Step 1: Clone the Repository
```bash
git clone https://github.com/abhishekk1004/spam_email.git
cd spam_email
```

### Step 2: Install Dependencies
```bash
pip install pandas scikit-learn
```

### Step 3: Download Dataset
Place the `spam.csv` file in the project root directory.

## 💻 Usage

### Running the Spam Detector
```bash
python email.py
```

### Example Interaction
```
Model Accuracy: 0.9865
```

```
Enter an email message (or type 'exit' to quit): Congratulations! You've won $1000! Click here to claim now!
🚨 This email looks like SPAM!

Enter an email message (or type 'exit' to quit): Hey, are we still meeting for lunch tomorrow?
✅ This email looks SAFE.

Enter an email message (or type 'exit' to quit): exit
```

## 📈 Model Performance

The system typically achieves:
- **Accuracy**: ~98.5%
- **Training Time**: < 1 second
- **Prediction Time**: Near-instantaneous

### Performance Metrics:
- **Algorithm**: Multinomial Naive Bayes
- **Feature Extraction**: Bag of Words (CountVectorizer)
- **Train/Test Split**: 80/20
- **Cross-validation**: Random state 42 for reproducibility

## 🔧 How It Works

1. **Data Loading**: Reads the spam dataset and prepares labels
2. **Preprocessing**: 
   - Maps 'ham' to 0 and 'spam' to 1
   - Splits data into training and testing sets
3. **Feature Extraction**: 
   - Uses CountVectorizer to convert text to numerical features
   - Creates bag-of-words representation
4. **Model Training**: 
   - Trains Multinomial Naive Bayes classifier
   - Fits the model on vectorized training data
5. **Evaluation**: Tests model accuracy on unseen data
6. **Prediction**: Provides real-time spam detection for new emails

## 📁 Project Structure

```
spam_email/
│
├── email.py          # Main Python script
├── spam.csv                  # Dataset file
├── README.md                 # Project documentation
└── requirements.txt          # Dependencies (optional)
```

## 📸 Screenshots

### Model Training Output
```
Model Accuracy: 0.9865071243
```

### Interactive Testing
![Spam Detection Demo](https://via.placeholder.com/600x300/ff6b6b/ffffff?text=Interactive+Spam+Detection+Demo)

### Feature Importance Visualization
![Feature Importance](https://via.placeholder.com/600x400/4ecdc4/ffffff?text=Top+Spam+Indicator+Words)

## 🛠️ Future Enhancements

- [ ] Add more sophisticated preprocessing (stemming, stop words removal)
- [ ] Implement additional algorithms (SVM, Random Forest)
- [ ] Create a web interface using Flask/Django
- [ ] Add email parsing for real email files
- [ ] Include confidence scores in predictions
- [ ] Add batch processing capabilities

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### How to Contribute:
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)

## 🙏 Acknowledgments

- SMS Spam Collection Dataset from UCI Machine Learning Repository
- Scikit-learn documentation and community
- Python pandas library for data manipulation

---

⭐ **Star this repository if you find it helpful!** ⭐