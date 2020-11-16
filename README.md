### Important Note for Aganitha: I haven't made this library myself, I have borrowed it from https://github.com/HerambVD/spoken2written, I have done a good amount of coding but making a python library was new to me, also I have done machine learning but not deep learning, I tried to improve the library but I could barely manage to understand the natural language processing part. Most of my time went in researching about how to make a python library. This is all the I could manage. Thank You.

# Spoken English to Written English translator

There exits a difference between how we write and how we speak. e.g While speaking we say "I paid twenty thousand dollars to xyz organization". But, we don't write above example as it is, instead we write it as "I paid $20000 to xyz organization."
This is a python module is to translates such spoken english language to its written form.

e.g. It will translate: "I watched movie named triple H ." to "I watched movie named HHH"
                        "My weight is fifty five kilograms ." to "My weight is 55 kg"
                        "I paid twenty thousand dollars to xyz organization ." to "I paid $20000 to xyz organization ."
                        
<h1>Installation guide</h1>

Run this command in terminal:
```
pip install spoken2written
```
The dependencies spaCy,word2number will also be installed after installing the package.
It is better to have english language dependency requirement of spacy which is en_core_web_sm

To install this en_core_web_sm, run following command in terminal
```
python -m spacy download en_core_web_sm
```
<h1>Usage</h1>

First you have to import the module using the below code.
```
import spoken2written
```
If it shows error during importing then spacy english dependency package is not installed in your device. In this case,
install en_core_web_sm library using the command mentioned above.

After importing the package use TextTraslator method to translate spoken English to written form.

Example script:
```
>>>from spoken2written import TextTranslator
...test= "My life is triple B . European authorities fined Google a record sixty five thousand dollars on Wednesday for abusing its power in the mobile phone market and ordered the company to alter its practices . Furthermore , My T - Shirt size is double X in 2019 and it costs six dollars . My weight is fifty kilograms ."
...result=TextTranslator(test)
...print(result)
```
Output:
```
My life is BBB . European authorities fined Google a record $65000 on Wednesday for abusing its power in the mobile phone market and ordered the company to alter its practices . Furthermore , My T - Shirt size is XX in 2019 and it costs $6 . My weight is 50 kg .
```


