# Text Classification

The sol.ipynb implements a Naive Bayes text classifier that categorizes text documents into two classes: 'positive' and 'negative'. It offers flexible text preprocessing options, including removing stopwords, word binarization, and handling negation.

The ec.ipynb notebook uses the Opinion lexicon of Hu and Liu (2004) for text classifcation using the simple word count method

## Usage

1. **Prerequisites**: Python 3.x installed along with the required libraries.

   ```bash
   scikit-learn
   nltk
   ```
2. **Training and testing data**: The `training_data` variable must be set to the path of training data directory, organized into 'pos' and 'neg' files. Similary, the `testing_data` variable must be set to the path of testing data directory
3. **Opinion** **Lexicon**: Ensure that the `positive-words.txt `and `negative-words.txt` files are located in the same directory as ec.ipynb. These files contain the lexicon for sentiment analysis.
4. **Evaluation**: The code computes accuracy, precision, recall, and F1 score for each configuration and prints the results in the main method.
5. **Separate Classifiers**:

   The six classifier mentioned in the assignment are configured in the as follows

   ```
   configurations = [
   {'wo_stop': False, 'binarization': False, 'negation': False}, #Bag of words method using word frequencies
   {'wo_stop': False, 'binarization': True, 'negation': False}, # Bag of words method using word frequency as 1 (binarization)
   {'wo_stop': True, 'binarization': False, 'negation': False}, # Content word frequencies (ignoring function words)
   {'wo_stop': True, 'binarization': True, 'negation': False}, # Content word frequencies of 1 per word 
   {'wo_stop': False, 'binarization': False, 'negation': True}, # BoW method using word frequencies after applying the negation
   {'wo_stop': False, 'binarization': True, 'negation': True} # BoW method using word frequency as 1 after applying the negation 
   ] 
   #wo_stop stands for without stopwords, wo_stop implies Only content words are used for classfication
   ```

## Results

The code displays results, including the confusion matrix and evaluation metrics for each configuration in the Notebook itself
