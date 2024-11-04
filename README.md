<H3>NAME:YOHESH KUMAR R.M</H3>
<H3>REGISTER NO: 212222240118</H3>
<H3>EX. NO.6</H3>
<H3>DATE:</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>

## Aim: 
	To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.
 
 
## Algorithm:
Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.

## Program:
```
!pip install nltk
import nltk
#import wordnet
nltk.download( 'punkt' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger' )
sentence=input()
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
# Print the parts of speech
for word, tag in pos_tags:
	print(word, tag)
 from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )

```

## Output
i.) Sample Input
![324403272-be801971-3ade-448b-9c7f-1241698c8d65](https://github.com/user-attachments/assets/4bf34e1c-f268-4805-a437-9f290ee0bfce)


ii.) Sample Output
	![324403665-f0c48bc8-6d2a-4614-949e-6c7e242b424f](https://github.com/user-attachments/assets/ef1cd386-81ce-4a39-9f34-629802cfda7c)

![324478457-096f3abf-59db-418d-ba13-f52af2f25471](https://github.com/user-attachments/assets/48ba9f6d-e9b2-4197-92be-e4caa794e4b1)




## Result:
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
