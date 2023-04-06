# data inspection:
- the turn number seems not "truly ordered"
- first letter was cut in the rationale (?)

# typo "theacher" --> "teacher"

# distilroberta:
- what are the start_idx/end_idx predicted by the Span Extractor? Written in model description. They are used to retrieve the rationale from the passage.
- what is P (in the span extractor)? the passage. I just added it to the description!

# berttiny
- what is P (in the span extractor)? As above.

validation/test
- missing results for distilroberta (all the other seeds other than 42, with and w/o history).  Maybe old version??


# All conclusions are missing for error analysis   Maybe old version?? Or you mean something else is to be done?
- (if you "get unexpected answers" you can read the paper https://arxiv.org/pdf/1808.07042.pdf to gain them and relate our displayed errors)
but i checked some of them and i think that some of the errors can be explained just by "googling"

