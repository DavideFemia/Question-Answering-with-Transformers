Assignment 2 review:



Paper:

- "and achieved the following results:" levare questa scritta, i risultati vengono presentati nell'apposita sezione
- Introduction: resuting f1 have to be in other section
- System description : "Our implementation is based on an encoder-only model" but actually it is not, it is just the first part of the structure.
- "In particular, we created new model classes for our BERTTiny-based / RoBERTa-based models. Each of these classes contains its own forward and generate methods. These functions in turn recall the forward / generate method of the underlying models. In addition, they include a part for generating the input of the encoder-decoder (Answer Generator). In this part we combine the (history and the) current question with the rationale predicted by the first encoder (Span Extractor)" --> what does "forward generate method" mean? implementation details like "classes" and "method" can be avoided, i didn't understand how many structures were built and how they're made (maybe, figures of the architectures may be useful)
- data section: non sono sicuro che sia necessaria per gli assignment. I passi di cleaning and preprocessing possono essere descritti nella sezione ...
- " For both the models we use a teacher forcing approach to ease the training of the Answer Generator in the early steps" --> what does "early steps" mean?
- "The teacher forcing probability decays linearly from 1.0 to 0.3" --> how is this decay rate set? manually?
- why did you choose AdamW? 
- Discussion: train-test split is not relevant here
- specify what happens when previous dialogues are over 512 tokens (what we cut and what we don't)...
- underline the fact that they're both distilled google models, but the original sizes and the original training is different because of dynamic masking in roberta 
(https://datascience.stackexchange.com/questions/97310/what-is-the-difference-between-bert-and-roberta)
- The smaller BERT models are intended for environments with restricted computational resources. They can be fine-tuned in the same manner as the original BERT models. However, they are most effective in the context of knowledge distillation, where the fine-tuning labels are produced by a larger and more accurate teacher.
 (https://huggingface.co/mrm8488/bert-tiny-finetuned-squadv2)
 in pratica vuol dire che per l'estrazione del rationale vanno bene... ma per l'estrazione di una label finale sono piu utili i large language models..
 - avoid to compare traing times with machine different from ours
 - avoid mentioning "fast.ai" - maybe i don't get the point but is a bit like saying Apple can do it better (of course it is the case...)
 - what would improve the sliding window techniwue? training speed? final score?
 - add error analysis
 - add llink to the final repository
 
 
 doubts:
 - is removing non-answerable questions right? "SQuAD2.0 combines the 100,000 questions in SQuAD1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering." isn't it the same for CoQa?
 - investigate what using M-FAC as optimizer would improve...
 
