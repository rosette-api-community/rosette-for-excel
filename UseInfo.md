# Rosette for Excel
Rosette for Excel brings the power and functionality of Basis Technology’s [Rosette API](https://developer.rosette.com) into Microsoft Excel. The plugin allows you to analyze text held in Excel sheets via both formulas and ribbon functions.

# Using Formulas
Together with the Rosette API, Excel formulas enable you to create complex function chains and highly customized output. Every time you update a linked cell, the Rosette API will recalculate your function results accordingly.*

The Rosette API functions available as in Excel's "Formulas" tab are (click through for our interactive documentation and complete language coverage or scroll down for more information):
* [Sentiment](https://developer.rosette.com/features-and-functions#sentiment-analysis)
* [Categorization](https://developer.rosette.com/features-and-functions#categorization)
* [Name Translation](https://developer.rosette.com/features-and-functions#name-translation) 
* [Name Similarity](https://developer.rosette.com/features-and-functions#name-similarity)

*N.B. Every cell update counts as an API call. It is the user’s responsibility to make sure they are not exceeding their Rosette API plan limits. You can track your usage on your Rosette API dashboard, and if you need more calls, just let us know! If you start seeing 403 error responses, you’ve exceeded your call limit for the month and will need to upgrade your plan. 

# Using the Ribbon
The Rosette ribbon functions allow you to customize your API results by combining functions together. Enable the functions you’d like to use by clicking on their icons. The output is written to a new sheet and provides one-to-many cell support. The ribbon provides additional linguistic analysis functionality not available with formulas and can be further configured through through the Settings dialog.

The Rosette API functions available in the Excel ribbon are:
* [Sentiment](https://developer.rosette.com/features-and-functions#sentiment-analysis)
* [Categorization](https://developer.rosette.com/features-and-functions#categorization)
* [Entity Extraction](https://developer.rosette.com/features-and-functions#entity-extraction)
* [Morphological Analysis](https://developer.rosette.com/features-and-functions#morphological-analysis)
* [Tokenization](https://developer.rosette.com/features-and-functions#tokenization)
* [Name Translation](https://developer.rosette.com/features-and-functions#name-translation)

# Function Glossary
## [Sentiment](https://developer.rosette.com/features-and-functions#sentiment-analysis)
Rosette can analyze the sentiment (subjective attitude) of an input text as positive, negative, or neutral. Calls to the sentiment endpoint return a sentiment label with a confidence score between 0 and 1. You can choose to evaluate either entity (sometimes called aspect) or document-level sentiment. Rosette for Excel can also automatically color code the results. Both options can be set using the Documents/Prose tab of the Settings dialog in the ribbon. 
## [Categorization](https://developer.rosette.com/features-and-functions#categorization)
Based on its analysis of a string of English text, the Rosette categorizer returns a category label. These labels are drawn from the Tier 1 contextual categories defined by the IAB Quality Assurance Guidelines Taxonomy.
## [Entity Extraction](https://developer.rosette.com/features-and-functions#entity-extraction)
The Rosette entity extraction endpoint uses case-sensitive statistical models to identify entities in unstructured text. An entity refers to an object of interest such as a person, organization, location, date, or email address. Extracting the entities in a text can help you classify it. Rosette can be optimized to extract entities from short-form social media text by selecting the "SOCIAL MEDIA" option in the  Documents/Prose tab of the Settings dialog. It can also automatically link entities found in the input text to Wikipedia. To enable this feature, check the “Hyperlink Entity QIDs to Wikipedia” box, also in the Documents/Prose tab. 
## [Morphological Analysis](https://developer.rosette.com/features-and-functions#morphological-analysis)
The Rosette morphology endpoint performs several base linguistic functions that prepare your text for indexing and further analysis. 
* Lemmatization: Returns the dictionary or base form of a word based on context and usage.
* Part-of-Speech Tagging: Labels and identifies the grammatical role of every word in an input text.
* Decompounding: For languages with compound words, returns the individual component parts.
* Han Readings: Provides pinyin/Hiragana transcriptions of Chinese and Japanese words written in Han script. 

You can select the functions you'd like to use through the “Morphology Options” dropdown in the Documents/Prose tab of the Settings dialog. 

## [Tokenization](https://developer.rosette.com/features-and-functions#tokenization)
Rosette's tokenization function identifies and separates each word in an input text into one or more tokens through advanced statistical modeling. A token is an atomic element such as a word, number, possessive affix, or punctuation mark. Like morphological analysis, tokenization helps prepare your text for indexing and further analysis.
## [Name Translation](https://developer.rosette.com/features-and-functions#name-translation)
Use Rosette's name translation to translate the name of an entity (person, location, or organization) from English to another language, or to English from another language. When converting from English, Rosette is optimized to convert the English version of a  name back to its native language. You can optimize the translation process by using the parameters found in the Translate Names tab of the Settings dialog. Specifying the input entity type, source language of use, source script, source language of origin, target script, and/or target scheme (an advanced feature used for transliteration) may improve both speed and performance, but is not required. 
## [Name Similarity](https://developer.rosette.com/features-and-functions#name-similarity)
The name similarity function allows you to evaluate the relative similarity of a pair of entity names (person, location, organization). Rosette returns a similarity score between 0 and 1. 
# Settings
Rosette for Excel settings are workbook-specific, which allows you to define different settings for different workflows. New workbooks open with the default settings enabled, but once you’ve configured your own, they’ll be saved along with your data. To change your default settings click the “Save as Defaults” button in the ribbon or Settings dialog. In addition to the function specific settings discussed above you also have several general sheet-level options. The Layout tab allows you to add hyperlinks and a copy of the input text to the results sheet.The Documents/Prose tab allows you to specify the language of your input text. For more information about settings (also referred to as parameters) and language support, check out the Rosette [developer portal](https://developer.rosette.com/features-and-functions#introduction).
# More Information
If you’d like to know more about what’s going on behind the scenes, you can check out the log files, which are held in the “Application Data” folder on your personal computer. An explanation of potential error codes can be found in our [documentation](https://developer.rosette.com/features-and-functions#errors). If you need more help, [contact us](mailto:support@rosette.com) or browse our [support information](https://support.rosette.com/hc/en-us).
