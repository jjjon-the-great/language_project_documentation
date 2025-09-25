RATIONALE: i have noticed that many of the false sentences contain gibberish. ill try to make a database of known/ unknown words - and cut off sentences that have over x% of unknown words.

Task 1: establish a word database using half of the sentences in the train database.

I have to think of a way to organise data in a way for it to be easily searchable - probably binary search tree.

Task 1.1 - find longest word in english sentences
task 1.1 result: the category of long words contains chemistry terms OR url's.

Task 1.2: try to find url's in incorrect sentences!
task 1.2 result: only 704 words in false sentences contain the sequence "http". this might be useful!

experiment: construct dictionary of half the legal sentences, see how many sentences contain how many non legal words.
results: interesting!

task 1.3: downloaded a bunch of english words. trying to analyse using them as database.

in order to simulate aproaching the database with unknown 
RESULTS OF WORD CUTOFF EXPERIMENT:
best cutoff at 40 percent and larger - remove.

we get rid of approximately 55 percent of False sentences, and 0.2 percent of true sentences as false negatives.

GREAT SUCCESS