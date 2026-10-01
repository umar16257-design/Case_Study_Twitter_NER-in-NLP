# Case_Study_Twitter_NER-in-NLP
Implementing NER for Tweet Analysis

# Problem Statement & Business Understanding

Twitter generates a large volume of short messages (tweets) containing valuable
information about people, locations, companies, products, events and other topics.

Relying only on hashtags is not sufficient because users may not use hashtags or
may use incorrect or misspelled hashtags.

The objective of this project is to build a Named Entity Recognition (NER) system
that can automatically identify and classify named entities present in tweets.

The dataset contains 10 fine-grained entity categories:
person, geo-location, company, facility, product, music artist, movie,
sports team, TV show and other.

### Business Objective

Build an automated NER system that can identify important entities in tweets
without depending on user-provided hashtags.

The system can help in:
- Trend and topic identification
- Brand and company monitoring
- Entity-based search and analysis
- Social media intelligence
- Automated information extraction

### Named Entity Recognition

NER is a Natural Language Processing task that identifies and classifies
named entities within text.

For this project, each token in a tweet is assigned a label using the BIO
(Beginning, Inside, Outside) tagging scheme.

Example:

Tweet:
"Harry Potter visited London"

Labels:
Harry      → B-person
Potter     → I-person
visited    → O
London     → B-geo-loc

### Modeling Approach

Two approaches will be explored:

1. BiLSTM + CRF using Word2Vec embeddings
2. BERT-based Transformer model using `bert-base-uncased`

The models will be trained and evaluated on the annotated Twitter NER dataset,
followed by predictions on custom sentences.

### Insight

This is a token-level classification problem where the goal is to correctly
identify the entity type of each token in a tweet. The project will compare
a recurrent neural network approach (BiLSTM + CRF) with an attention-based
Transformer approach (BERT).
