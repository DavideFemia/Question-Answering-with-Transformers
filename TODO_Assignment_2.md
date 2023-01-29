## review notebook assignment 2

# Task 2
- some more barplots or graphs to inspect the length of questions and answers should be added
-> Totally agree! We'll add them.

# Task 5
- same of the task 6 review (below)

# Task 6
- i think that some subsessions are maybe missing (should be 6 subsections: one for each model and seed):
- where are the results on val and test with the other seeds (apart from 42)?
-> Answer: the seeds are aggregated (averaged) for each model. So we only have 4 models, bert/roberta history/no-history.
- where is the training process display?
-> TO DO! We have to re-run the models!
- how did you cut the sentences? did you cut them? how much do they "fill" the 512 tokens? they frequently fill em or is just a few cases? in the last case maybe a quantile-cut is to be considered
-> TO DO!

# Task 7
- error analysis: where are the comments on the reasons of the errors? (read the paper https://arxiv.org/pdf/1808.07042.pdf to gain them and relate our displayed errors)
-> TO DO!
- what is the purpose of the histogram of the lengths of the conversations?
-> REALLY NICE QUESTION ahahah. Maybe I will remove it because, given that we use a fixed length for the history, the length of the conversation becomes irrelevant...
- the 5 errors for the 2 models for each of the 5 sources should be displayed (for a total of 2x5x5 = 50), of course some comments can group multiple Q-A pairs.
-> In total we have 4 models for 5 conversations for 5 errors each. However we can consider to only use the best model (history or without history) so that we shorten a little bit the final print!

# doubts
- why is the "test" split still used in the train-val-split split (if it is namely not available)? probably this is something i didn't personally get
-> Yeah, it's something we can remove from the split function.
- what is the 'length of conversation'? in the error analysis there are histograms of the distribution of lengths but are <<512 
-> Answer: number of QA pairs. WE HAVE TO PLACE THE DISTRIBUTION OF TOKENS HERE AS I'VE DONE IN TASK 2.
