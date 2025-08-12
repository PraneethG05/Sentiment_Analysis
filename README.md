
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">

</head>
<body>

  <h1>🚫 Hate Speech Detection in Tweets</h1>
  <p>
    In a rapidly evolving world there has been a significant change in the way our world communicates, and part of those changes includes a rise in inappropriate behaviors, such as the use of aggressive and hateful language online.Social media platforms have become hotspots for hate speech, sparking concerns about its harmful impact. To address this issue, recent studies have delved into various techniques to automatically detect and counteract hate speech using computer algorithms. Researchers have explored methods to extract meaningful features from hate speech messages, such as analyzing the words used, the tone, and the context in which they are expressed. By understanding these features, algorithms can learn to recognize patterns indicative of hate speech.To facilitate this learning process, different types of machine learning models have been employed. decision tree , Support vector machine(SVM), Term Frequency-Inverse Document Frequency, TF-IDF, Convolutional neural networks (CNNs), and transformer-based models have been among the most commonly used. These models are trained on large datasets of labeled hate speech examples, enabling them to identify similar patterns in new, unseen messages.However, the effectiveness of these approaches can vary depending on factors such as the dataset used and the specific characteristics of the social media platform. Some methods may perform well in one context but struggle in another due to differences in language usage, cultural nuances, or the types of hate speech prevalent on the platform.This paper aims to provide a comprehensive overview of these methodologies, highlighting their strengths, limitations, and potential applications. By synthesizing insights from various studies, it seeks to contribute to the development of more robust and adaptable solutions for combating hate speech online, ultimately fostering safer and more inclusive digital environments.
  </p>

  <h2>📚 Methodology</h2>

  <h3>1. Data Acquisition</h3>
  <ul>
    <li>Dataset: <strong>Sentiment140 Twitter Dataset</strong> from Kaggle (1.6 million labeled tweets)</li>
    <li>Labels: Positive and Negative sentiment (used as proxy for hate/non-hate)</li>
  </ul>

  <h3>2. Data Cleaning</h3>
  <ul>
    <li>Remove URLs, usernames, dates</li>
    <li>Convert to lowercase</li>
    <li>Remove duplicates and handle missing values</li>
  </ul>

  <h3>3. Text Preprocessing</h3>
  <ul>
    <li>Tokenization</li>
    <li>Stopword removal using NLTK</li>
    <li>Stemming using Porter Stemmer</li>
  </ul>

  <h3>4. Feature Extraction</h3>
  <ul>
    <li>TF-IDF Vectorization for Logistic Regression and Decision Tree</li>
    <li>Raw input embeddings for CNN</li>
  </ul>

  <h3>5. Model Training</h3>
  <ul>
    <li>Models used:
      <ul>
        <li>Logistic Regression (Scikit-learn)</li>
        <li>Decision Tree</li>
        <li>Convolutional Neural Network (Keras)</li>
      </ul>
    </li>
  </ul>

  <h3>6. Model Evaluation</h3>
  <ul>
    <li>Metrics: <code>Precision</code>, <code>Recall</code>, <code>F1-Score</code></li>
    <li>Visualization: ROC curves, confusion matrix, accuracy comparison</li>
  </ul>

  <h3>7. Model Deployment</h3>
  <ul>
    <li>Final trained model saved using <code>pickle</code></li>
    <li>Future deployment via API or web application</li>
  </ul>

  <h2>📊 Block Diagram</h2>
  <pre>
+------------------------------------+
|        Project Environment         |
| - Kaggle API Installation          |
| - Kaggle Dataset Setup             |
+----------------+-------------------+
                 |
                 v
    +----------------------------+
    |      Data Acquisition      |
    | - Downloading Dataset      |
    | - Extracting Data          |
    +------------+---------------+
                 |
                 v
  +------------------------------+
  |     Data Preprocessing       |
  | - Cleaning, Tokenization     |
  | - Stopwords, Stemming        |
  +------------+---------------+
                 |
                 v
+--------------------------------+
|        Model Training          |
| - TF-IDF / Embeddings          |
| - Logistic, Tree, CNN          |
+------------+---------------+
                 |
                 v
+--------------------------------+
|       Model Evaluation         |
| - Confusion Matrix             |
| - Accuracy & F1-Score          |
+------------+---------------+
                 |
                 v
+-----------------------------------------+
|  Visualization and Performance Analysis |
| - Word Cloud, Class Distribution        |
| - ROC, PR curves                        |
+-----------------+-----------------------+
                 |
                 v
+-------------------------------+
|         Conclusion            |
| - Insights & Future Work      |
+------------------------------+
  </pre>

  <h2>📈 Results</h2>
  <ul>
    <li><strong>Decision Tree</strong>
      <ul>
        <li>Precision: <code>0.88</code></li>
        <li>Recall: <code>0.89</code></li>
        <li>F1-Score: <code>0.89</code></li>
      </ul>
    </li>
    <li><strong>CNN</strong>
      <ul>
        <li>Precision: <code>0.85</code></li>
        <li>Recall: <code>0.84</code></li>
        <li>F1-Score: <code>0.85</code></li>
      </ul>
    </li>
    <li><strong>Logistic Regression</strong>
      <ul>
        <li>Precision: <code>0.81</code></li>
        <li>Recall: <code>0.79</code></li>
        <li>F1-Score: <code>0.81</code></li>
      </ul>
    </li>
  </ul>

  <h2>📌 Conclusion</h2>
  <p>
    As hate speech continues to grow across online platforms, the development of reliable detection systems is crucial. This project demonstrated a complete machine learning pipeline using TF-IDF and CNN-based methods. While Logistic Regression provides simplicity and interpretability, CNNs showed slightly better performance at the cost of more compute.
  </p>
  <p>
    However, machine learning alone cannot solve hate speech entirely. Social, educational, and policy-driven approaches must complement technical advancements to foster respectful online communication. Future work will involve:
  </p>
  <ul>
    <li>Multilingual hate speech detection</li>
    <li>Context-aware transformer models like BERT</li>
    <li>Deployment via web/mobile interface</li>
  </ul>

  <h2>📬 Contact</h2>
  <p>
    For questions, collaborations, or suggestions, feel free to reach out via
    <a href="mailto:ganjipraneeth300@gmail.com">email</a> or <a href="https://github.com/PraneethG05">GitHub</a>.
  </p>

</body>
</html>
