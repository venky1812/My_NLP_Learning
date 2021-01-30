# My_NLP_Learning
Includes my learnings related to NLP
## Typical NLP pipeline:
![NLP Pipeline](https://user-images.githubusercontent.com/50025496/106348137-feffa180-62e9-11eb-8884-c75f7fcec88b.png)



#### Data Acquisition:
The first step in the process of developing any NLP system is to collect data relevant to the given task.Different possible sources of data is as follows.
* Use a public dataset: Take a look at Google’s specialized search engine for datasets
* Scrape data : We could find a source of relevant data on the internet.
* Production intervention: We can work with the product team to collect more and richer data by developing better instrumentation in the product. In the tech world, this is called product intervention.
* Data augmentation : We can use different data agumentation techniques like Synonym replacement,Back translation(Eg:English -> German -> English),Replacing entities,Bigram fliping etc.


#### Text Extarction and Cleanup:
Text extraction and cleanup refers to the process of extracting raw text from the input data by removing all the other non-textual information, such as markup, metadata, etc., and converting the text to the required encoding format

* HTML Parsing and Cleanup.
* Unicode Normalization :As we develop code for cleaning up HTML tags, we may also encounter various Unicode characters, including symbols, emojis, and other graphic characters. This means that the text we see should be converted into some form of binary representation to store in a computer. This process is known as text encoding.
* Spelling Correction : Could be beacuse of fast typing and fat-finger typing.
* Reading data from PDF using PYPDF or PDFMINER or extracting data from scanned documents using OCR(Pytessaract).
