we need now to device a method of separating incorrect sentences from correct ones, given that both are compoundd of correct english words.

IDEA 1: make database of possible word combinations. 
PROS: easy top program.
CONS: really hard.

IDEA 2:
count 100 most common words in the text. for each of them establish a database of possible correct following words - for each sentence calculate a score.

done, written them in common_words.txt