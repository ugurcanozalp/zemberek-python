# Zemberek Python Api

> This library allows one to use Zemberek software which is written in Java, using Java Virtual Machine (JVM) in python.

Zemberek is a Java-based natural language processing (NLP) tool created for the Turkish language. 

## Requirements

1.  Python 3.6+
2.  JPype1 0.7.0

## Install required libraries

    Go to folder and run the following command.

    ```console
    pip install .
    ```

## Usage of API (pyzemberek library)
    
1.  Import library and create Zemberek object.

    ```python
    import pyzemberek as pyzmbrk
    zmbrk = pyzmbrk.Zemberek()
    ```

2.  Use the object and library. Some examples.

    ```python
    import turkishnlptool as pyzmbrk
    zmbrk = pyzmbrk.Zemberek()
    zmbrk.addVerb(['tweetlemek','tweetle','tivitle'])
    zmbrk.analyze('tweetleyeyazdım')
    stems, lemmas = zmbrk.stemLemma('kutucuğumuz')
    print('stems: {stems}, lemmas: {lemmas}')
    zmbrk.analyze('kutucuğumuz')
    zmbrk.informalWordAnalysis('okuycam diyo')
    stems, lemmas = zmbrk.sentenceDisambugation('Bol baharatlı bir yemek yaptıralım.')
    print('stems: {stems}, lemmas: {lemmas}')
    sents = zmbrk.sentenceBoundary('Prof. Dr. Veli Davul açıklama yaptı. Kimse %6.5 lik enflasyon oranını beğenmemiş! Oysa maçta ikinci olmuştuk... Değil mi?')
    print(sents)
    res = zmbrk.sentenceTokenization('İstanbul\'a, merhaba! Ankara\'dan sonra yeni bir şehre gelmek bana iyi geldi :)')
    print(res)
    stems,lemmas= zmbrk.sentenceDisambugation('İstanbul\'a, merhaba! Ankara\'dan sonra yeni bir şehre gelmek bana iyi geldi :)')
    print('stems: {stems}, lemmas: {lemmas}')
    zmbrk.sentenceTokenization('Nbr knk ? yrn n zmn gelcen?')
    zmbrk.correctDocument('Nbr knk ? yrn n zmn gelcen?')
    res = zmbrk.correctDocument('böle olmasını istemiyom ya')
    print(res)
    res = zmbrk.normalizeDocument('Nbr knk ? yrn n zmn gelcen?')
    print(res)
    poses = zmbrk.findPOS('Keşke yarın hava güzel olsa')
    print(poses)
    ```
