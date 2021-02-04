# My_NLP_Learning
Includes my learnings related to NLP
## Typical NLP pipeline:
![NLP Pipeline](https://user-images.githubusercontent.com/50025496/106348137-feffa180-62e9-11eb-8884-c75f7fcec88b.png)



#### Data Acquisition:
The first step in the process of developing any NLP system is to collect data relevant to the given task.Different possible sources of data is as follows.
* **Use a public dataset:** Take a look at Google’s specialized search engine for datasets
* **Scrape data :** We could find a source of relevant data on the internet.
* **Production intervention:** We can work with the product team to collect more and richer data by developing better instrumentation in the product. In the tech world, this is called product intervention.
* **Data augmentation :** We can use different data agumentation techniques like Synonym replacement,Back translation(Eg:English -> German -> English),Replacing entities,Bigram fliping etc.


#### Text Extarction and Cleanup:
Text extraction and cleanup refers to the process of extracting raw text from the input data by removing all the other non-textual information, such as markup, metadata, etc., and converting the text to the required encoding format

* **HTML Parsing and Cleanup.**
* **Unicode Normalization :** As we develop code for cleaning up HTML tags, we may also encounter various Unicode characters, including symbols, emojis, and other graphic characters. This means that the text we see should be converted into some form of binary representation to store in a computer. This process is known as text encoding.
* **Spelling Correction :** Could be beacuse of fast typing and fat-finger typing.
* Reading data from PDF using PYPDF or PDFMINER or extracting data from scanned documents using OCR(Pytessaract).

#### Pre processing :

All NLP software typically works at the sentence level and expects a separation of words at the minimum. So, we need some way to split a text into words and sentences before proceeding further in a processing pipeline. Sometimes, we need to remove special characters and digits, and sometimes, we don’t care whether a word is in upper or lowercase and want everything in lowercase. Many more decisions like this are made while processing text. Such decisions are addressed during the pre-processing step of the NLP pipeline.

* **Preliminaries:** Sentence segmentation and word tokenization.
* **Frequent steps**:Stop word removal, stemming and lemmatization, removing digits/punctuation, lowercasing, etc.
* **Other steps:** Normalization, language detection(`Polyglot`), code mixing, transliteration, etc.
* **Advanced processing:** POS tagging, parsing, coreference resolution, etc.

#### Feature Engineering:

* Feature engineering is an integral step in any ML pipeline. Feature engineering steps convert the raw data into a format that can be consumed by a machine.
* The main drawback of classical ML models is the feature engineering. Handcrafted feature engineering becomes a bottleneck for both model performance and the model development cycle.In the DL pipeline, the raw data (after pre-processing) is directly fed to a model. The model is capable of “learning” features from the data.

#### Modelling:

* Start with Simple Heuristics.(Stanford NLP’s TokensRegex and spaCy’s rule-based matching are two useful tools for advanced regular expressions).
* Building Your Model


## Text Representation 


#### Doc2Vec:
* Doc2vec is similar to Word2vec in terms of its general architecture, except that, in addition to the word vectors, it also learns a “paragraph vector” that learns a representation for the full text.By doing so it captures the contextual information which was not captured by word embedddinggs or character embeddings.
* Since it models some form of context and can encode texts of arbitrary length into a fixed, low-dimensional, dense vector, it has found application in a wide range of NLP applications, such as text classification, document tagging, text recommendation systems, and simple chatbots for FAQs.

#### Contextual word representations:
* It uses “language modeling,” which is the task of predicting the next likely word in a sequence of words.
* It make use of the word embeddings we discussed earlier but use complex architectures involving multiple passes through the text and multiple reads from left to right and 
 right to left to model the context of language use.
 
 #### Points to remember:
 * All text representations are inherently biased based on what they saw in training data.Need to be aware of those biases and its impact on our task.
 * Unlike the basic vectorization approaches, pre-trained embeddings are generally large-sized files (several gigabytes), which may pose problems in certain deployment scenarios.
 
 
## Text Classification/Topic Classificaton/Text Categorization/Document Categorization :
#### Types of classification:
 * Binary Classification,multiclass and multi label classification.
 
#### Typical Text classification Pipeline:
* Collect or create a labeled dataset suitable for the task.
* Split the dataset into two (training and test) or three parts: training, validation (i.e., development), and test sets, then decide on evaluation metric(s).
* Transform raw text into feature vectors.
* Train a classifier using the feature vectors and the corresponding labels from the training set.
* Using the evaluation metric(s) from Step 2, benchmark the model performance on the test set.
* Deploy the model to serve the real-world use case and monitor its performance.
 
 
