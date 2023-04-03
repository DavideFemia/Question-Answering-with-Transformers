# Question-Answering-with-Transformers :crystal_ball: :green_book:
©Riccardo Paolini @Davide Femia @Alessandro D’Amico ©Sfarzo El Husseini

In this work we address the problem of Conversational Question Answering, with reference to the CoQA dataset introduced by Stanford University in (Reddy et al., 2018). One of the major challenges of this tasks is the management of the conversation history to answer the current question. 
We propose a solution based on Transformers such as BERTTiny and DistilRoBERTa.
In particular, our architectures consist of two networks, the first deals with the rationale (the sentence which contains the answer) extraction, while the latter identifies the correct answer and reformulates it (see figure below).

![](https://www.mdpi.com/electronics/electronics-12-00209/article_deploy/html/images/electronics-12-00209-g001.png)


## Models
- BERTTiny (``prajjwal1/bert-tiny``)
- DistilRoBERTa (```distilroberta-base```)

## Tested configurations
Two main configurations were experimented

- *Not* Considering the history of the conversation    
- Considering the history of the conversation (4 previous dialogues)

These models were tested both on the test set and validation set, obtaining the following results
