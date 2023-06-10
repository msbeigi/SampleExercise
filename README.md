## Requirements
To run the code for the Document Similarity scenario, you will need the following dependencies and resources:

* Python 3.7 or above
* NLTK (Natural Language Toolkit) library
* WordNet database (included in NLTK)
* sklearn library
* You can install the required Python packages using pip:

``` 
  pip install nltk 
  pip install sklearn

``` 
Before running the code, make sure to download the necessary NLTK resources. You can do this by running the following code in a Python interpreter:

``` 
  import nltk
  nltk.download('punkt')
  nltk.download('wordnet')
  nltk.download('averaged_perceptron_tagger')
  nltk.download('omw-1.4')
  nltk.download('stopwords')
```
## Code description

<div style="text-align: justify; text-indent: 20px;">
1.  <strong>docuemnt_similarity.py </strong> :This code implements a document similarity calculation using WordNet-based synsets and path similarity. It consists of two main functions, doc_to_synsets and similarity_score, and uses provided helper functions as well.

The doc_to_synsets function takes a document as input and processes it by tokenizing and performing part-of-speech tagging using NLTK. It then converts each token's tag using the convert_tag function and retrieves the corresponding synset from WordNet. The first synset match for each token is used, and if no match is found, the token is skipped. The function returns a list of synsets for the given document.

The similarity_score function calculates the normalized similarity score between two lists of synsets, then it stores the maximum similarity values for each synset in similarities_syn1 and then computes the average similarity score by summing all the maximum similarity values and dividing by the total number of synsets found.
</div> 
<div style="text-align: justify; text-indent: 20px;">  
2.  <strong>topic_selection.py  </strong>:This code performs topic modeling on the `newsgroup_data` using Gensim's LDA (Latent Dirichlet Allocation) model. It first preprocesses the data using `CountVectorizer` to extract three-letter tokens, remove stop words, and filter tokens based on their document frequency. Then, it trains an LDA model with 10 topics using the corpus and vocabulary mapping. The code includes functions to extract the 10 topics and their significant words, calculate the topic distribution for a new document, and assign topic names based on predefined categories.
</div>  
