# Using Formulas
Combined with the Rosette API, formulas enable you to create complex function chains and highly customized output. Rosette API will recalculate your function whenever your linked cells are updated.  Be cautious here!  It is on the user to ensure that they are not overusing their Rosette API plan.  The dynamic nature of formulas makes them powerful tools, but you do not want to make thousands of calls with your Rosette API key unintentionally.
The Rosette API functions that are available as Excel formulas in the "Formulas" ribbon tab are:
* [Translate names](https://developer.rosette.com/features-and-functions#name-translation) 
* [Categorize](https://developer.rosette.com/features-and-functions#categorization)
* [Match Names](https://developer.rosette.com/features-and-functions#name-similarity)
* [Analyze Sentiment](https://developer.rosette.com/features-and-functions#sentiment-analysis)
# Using the Ribbon
The ribbon provides the capability for customization of the API result. The output is written to a new sheet and provides one-to-many cell support. The ribbon provides all the same functionality of the formulas and is configurable through ribbon buttons and the setting dialog. Endpoints can be enabled/disabled by clicking their icon. 
##Document Functions
###Sentiment
Rosette can analyze the sentiment (subjective attitude) of the input as positive, negative, or neutral. Given the input we return a sentiment label with a confidence score between 0 and 1.
###Entity Extraction
The Rosette entity extraction endpoint uses case-sensitive statistical models to identify entities in documents. An entity refers to an object of interest such as a person, organization, location, date, or email address. Identifying entities can help you classify data. You have the option to link entities in the input to a knowledge base of persons, locations, and organizations to help you establish the entity’s identity. It returns an entityId that links to a Wikipedia page with more information about the identity. 
###Categorization
Based on its analysis of the content of a string in English, the Rosette categorizer recognizes the Tier 1 contextual categories defined by the IAB Quality Assurance Guidelines Taxonomy.
###Tokenization
Rosette identifies and separates each word into one or more tokens through advanced statistical modeling. A token is an atomic element such as a word, number, possessive affix, or punctuation.
###Morphology
The Rosette morphology endpoint provides language-specific tools for returning parts-of-speech, lemmas, compound components, and Han-readings for each token in the input. For languages with compound words, Rosette divides the words into components. For Chinese tokens in Han script, Rosette returns pinyin transcriptions as the Han-reading. For Japanese tokens in Han script, Rosette returns Furigana transcriptions rendered in Hiragana as the Han-reading.
##Name Translation
The name translation endpoint can translate the name of an entity (Person, Location, or Organization) from English to another language, or to English from another language. When you are converting from English to another language, the endpoint is optimized to convert the English version of a person’s name back to the native language of that name. 
#Settings
Rosette for Excel settings are workbook-specific, enabling you to have multiple instances open for differing workflows.  Each workbook will open with the default settings the first time it is opened.  After that, the settings will be set to whatever was last configured for that workbook.  To change your default settings click the ‘Save as Defaults’ button in the ribbon or settings dialog. This behavior may be impacted by use with other Excel add-ins which have their own settings. The following images show what settings are available besides endpoint toggling in the ribbon. Extended descriptions of what the parameters mean can be found on the [developer portal](https://developer.rosette.com/features-and-functions#introduction).
#Questions?
If you’re wondering about what’s running behind the scenes, you can check the log files, located within the Application Data folder on your personal computer. An explanation of potential errors is located in our [documentation](https://developer.rosette.com/features-and-functions#errors). Otherwise, you’re welcome to contact us or browse support information [here](https://support.rosette.com/hc/en-us).
