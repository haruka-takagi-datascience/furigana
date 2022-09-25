# Building a Special Furigana Machine

In the Japanese language, there are three different forms of written language. Hiragana, Katakana and Kanji. The Kanji characters are a derivation of traditional Chinese characters, and over time they have become a writing system of their own. In Japanese writing, the three forms Hiragana, Katakana and Kanji all mix to express information in newspapers, books and posters. When studying Japanese, it is an initial hurdle for learners to be able to read these Kanji characters, as they have different readings depending on what other characters surround them. To help learners, furigana was invented, as a form to show the reading of the Kanji characters in Hiragana. An example is shown in the image below. 

<img src="images/img_1.png">

In this example the furigana/reading of 今日 is きょう:kyou. And the furigana/reading of 天気 is てんき:tennki.
Already in the Japanese Morphological Analysis space, there are many packages that have the ability to convert sentences with Kanji characters into their readings. Some of these packages are MeCab, Jumanji, Pykakashi, and etc. 

However, when it comes to analyzing Japanese text in computational linguistis ways, we run into a problem. In the example above and in all of the furigana packages available so far, there is no way to tell which reading attributes to which character. 

For example, using the example above, 今日 = きょう:kyou, a native Japanese speaker will recognize that...
1. 今:きょ:kyo + 日:う:u
2. 天:てん:ten + 気:き:ki

However, there is no way to tell this with the furigana machines. And on top of this the character 天 has more than one possible reading when alone, the possible readings for 天 are てん, あめ, あま, そら = ten, ame, ama, sora. This is the case for most Kanji characters, most of them have more than one readings and many have up to 4 possible readings. 

In this project I will be creating a special furigana machine that will be able to put these readings on any combination of characters individually. 
For example, using this machine the program will be able to determine that 今日 is 今:きょ:kyo + 日:う:u. This will be useful to implement in Japanese learning textbooks or a new program that will help learners read any text. It will also be useful in data conversion & expansion involving dialogue transcripts, such as the "Corpus of Spontaneous Japanese" known as CSJ in the NLP space. The CSJ is a database containing a large collection of Japanese spoken language data and information for use in linguistic research. I believe most of the Automatic Speech Recognition technology using Japanese, such as Amazon Alexa of Google Home for Japanese use, is trainined off the CSJ and datasets similar to the CSJ. 

