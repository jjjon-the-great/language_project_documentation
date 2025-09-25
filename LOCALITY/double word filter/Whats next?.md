we need now to device a method of separating incorrect sentences from correct ones, given that both are compoundd of correct english words.

IDEA 1: make database of possible word combinations. 
PROS: easy top program.
CONS: really hard.

IDEA 2:
count 100 most common words in the text. for each of them establish a database of possible correct following words - for each sentence calculate a score.

done, written them in common_words.txt

99.6 percent of sentences contain at least a single word of the top frequent 100. splendid.

RESULTS:
worked AMAZINGLY. by calculating score for a sentence as recognised hits/unrecognised hits, and filtering it - managed to drive up separation way up - letting 88 percent of true sentences pass, while only letting 24 percent of false sentences pass.

another test - incresing amount of words from 100 to 300 yielded amazing results. trying 1000 next.

by trying 1000 words, managed to pass 18 percent false with 90 percent true.
2000 words yielded almost no improvement - 17 percent.
also possible to pass 12 percent false with 88 true. (0.7)
 also  10.6 percent false with 86 true (0.72)
 also10.7 false with 

EXPERIMENT: added prevs dictionary.

passed 14 false with 90 true. (0.72)
passed 8 with 85 true. (0.75)
passed  10.8 with 88.5 true. (0.74)

RESULT: definetly an improvement. try adding scaling factor? maybe improvement.

SCALE = 0.5 for behind.

passed 16 false with 92 true. (0.7)
passed 12.5 false with 90 true (0.72)
passed 10.1 false with 87.5 true (0.735)
passed 8 false with 84.5 true (0.75)

RESULT: negative scale - significant improvement at 90 true at 85 not much.

SCALE = 2 for behind.

passed 10.4 false with 86.6 true (0.75)
passed 7 false with 80 true (0.78)
passed 16 false with 91.4 true (0.72)

RESULT: bad.

will stick to SCALE=0.5 (0.72).

EXPERMINET: feed the entire bible, asimov's foundation, war and peace, and works of shakespeare into a giant text file - going to train the machine on it.

RESULT: reallu bad. worsened by a lot.

EXPERIMENT: increase amount of words to 10,000.

RESULT: 
passed 15.5 false with 92 true. (0.65)
passed 11 false with 88 true (0.68)
passed 14.5 false with 91.5 true (0.66)
passed 11.3 with 88.4 true (0.67)
passed 14.5 false with 91.4 true (0.665)

RESULT: stayed around the same.

20,000 entries?

passed 12:88 (0.665)

CONCLUSION: worse. try to reduce amount of keywords, might improve pervormance by reducing variance.

800 tokens:

17:91 (0.73)
15:90 (0.74)

1000 tokens:
14:90 (0.74)

2000 tokens:
12.5:90 (0.72)

5000 tokens:
9:87

