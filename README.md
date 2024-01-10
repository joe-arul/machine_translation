# Machine Translation (with Attention mechanism)

In this assignment I explore different strategies used in building and training a Language Translator. I use Seq2Seq learning to convert sequences from English to Hebrew. I also include techniques such as **bi-directional** learning and **Attention** mechanism which serve as the building blocks of advanced transformer-based NLP models such as GPT, Llama etc. . 

### **Language Choice and Details**

I initially wanted to build a model to translate English to **Tamil** which happens to be my Native Language so that I could work with the translations easily. But due to less number of available sentence pairs (207) on the https://www.manythings.org/anki/ website for this language, I picked **Hebrew**.

Though Hebrew has been a language of fascination for me for a while now due to its Biblical association, there are a few other important reasons I picked Hebrew for learning machine translation.

- Hebrew is **written from right to left**, it will be interesting to see if Bi-LSTM and Attention produces better results.

- English and Hebrew are from completely different language-families and roots. (https://webspace.ship.edu/cgboer/languagefamilies.html)
They are from completely different regions and time-periods and have isolated places of origins.
  - English -> **Region:** West Germany, **Language family:** Indo-European, **Root:** Germanic
  - Hebrew -> **Region:** Israel, **Language family:** Afro-Asiatic, **Root:** Semitic

- They share almost a near-zero lexical similarity (https://en.wikipedia.org/wiki/Lexical_similarity) and less genetic relationship and linguistic interference. (https://en.wikipedia.org/wiki/Genetic_relationship_(linguistics))

- English-Hebrew also has a good number of sentence pairs available on the https://www.manythings.org/anki/ website(127856)


![LexicalDistance](<img/lexical_distance_eng_heb.png>)
Image Source: https://alternativetransport.wordpress.com/2015/05/05/34/

### Strategies Used: 

- Used Hebrew Tokenizer (github.com/YontiLevin/Hebrew-Tokenizer) to parse and clean Hebrew text (Canonical normalization used for English does not work)
- Converted text to sequences (reversed sequence list for Hebrew)
- Models : Seq2Seq, Bi-directional Seq2Seq (Bi-LSTM), Seq2Seq with Attention layer
- Tuning: Latent dimensions, training epochs, dropout, activation functions
- Sampling:  Greedy and Multinomial (with different temperatures)



Link to [Notebook](notebooks/machinetranslation.ipynb)
