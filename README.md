# Natural_Language_Processing : Bag of words technique for text vectorization

Data set link : https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

The "Bag of Words" (BoW) is a basic and fundamental technique in Natural Language Processing (NLP) for representing text data as numerical features that can be used in machine learning models. Here's how it works:

1. **Tokenization**:
   - The first step is to tokenize the text, which means breaking it down into individual words or terms. This process divides the text into smaller units, typically words, but it could also be subwords or characters.

2. **Vocabulary Building**:
   - After tokenization, the unique words in the text are collected to form a vocabulary. Each unique word is known as a "token." This vocabulary becomes the set of all words that the BoW model is aware of.

3. **Vectorization**:
   - For each document (a piece of text), a vector is created. The length of the vector is the same as the size of the vocabulary, and each position in the vector corresponds to a word in the vocabulary. Initially, all values in the vector are set to 0.

4. **Counting Token Occurrences**:
   - To fill the vector for a document, you count how many times each word in the vocabulary occurs in that document. This count is placed in the corresponding position in the vector.
   - If a word is not present in the document, its count remains 0 in the vector.

5. **Sparse Vectors**:
   - BoW vectors are typically sparse because most words in the vocabulary won't appear in any given document. Only the words present in the document will have non-zero counts in the vector.

6. **Use in Machine Learning**:
   - These vectors, with word counts, can be used as features in various machine learning algorithms for tasks like text classification, sentiment analysis, topic modeling, and more.

BoW is simple and efficient, but it has limitations:

- **Loss of Order Information**: BoW disregards the order of words in the text, treating each document as an unordered collection of words. This can be a disadvantage for tasks that rely on word order, like language generation.

- **Vocabulary Size**: The size of the vocabulary can become very large, especially in large text corpora. This can lead to high-dimensional vectors, which can be computationally expensive and may require dimensionality reduction techniques.

- **Word Frequency**: BoW doesn't take into account the importance of words. Common words like "the," "and," or "in" may dominate the vectors, making it necessary to use techniques like TF-IDF (Term Frequency-Inverse Document Frequency) to weigh words based on their importance.

Despite these limitations, the Bag of Words model is a good starting point for text processing and can work well for many NLP tasks, especially when paired with appropriate feature engineering and machine learning algorithms.

