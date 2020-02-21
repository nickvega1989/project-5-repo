### Initial Natural Language Processing

Once the data was organized we were able to conduct NLP. We used both the Count and Tfidf Vectorizers. After conducting more EDA on the vectorized data we then included our own unique stop words to the default list of stop words. We stuck with the default tokenization settings of the vectorizers. We did not lemmatize or stem. We did not experiment much in this domain of NLP for reasons we discuss later.

### Initial Modeling

We began with basic Logistic Regression & Support Vector Machine models. Due to the strength of these default algorithms & default vectorizers and Nick's organized data scraping & cleaning,  we achieved high accuracy scores of about 95%-96.4%. However, considering the context of emergency personnel and evacuation routes we wanted to improve this score since every percentage point could possibly impact lives being saved or lost. Instead of customizing these models and vectorizers we decided to explore other options. This is where advanced NLP and modeling comes in.


### Advanced NLP & Modeling with Google's BERT

To classify tweets as relevant or not to road closures we utilized Google's BERT.
BERT stands for Bidirectional Encoder Representations from Transformers. It analyzes a word based on the other words before and after it in the sentence/tweet. This provides context to language which other NLP techniques do not do. It is open sourced and already trained on a large text corpus (Wikipedia) but we can give it additional training that is specific to our task. We utilized Google's free Colab environment so we could access their GPU's since BERT is a computationally heavy. BERT provided an accuracy score of 99.8% and an MCC score of 99.6%.
---
