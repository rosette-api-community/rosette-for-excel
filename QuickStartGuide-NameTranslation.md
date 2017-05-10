# Getting Started with Rosette for Excel: Name Translation
## About Rosette for Excel (Beta)
Rosette for Excel is a plugin developed by [Basis Technology Corp.](https://www.rosette.com/about-us/) to make the multilingual text analytics, natural language processing, and name handling features of the [Rosette API](https://developer.rosette.com/) available to Excel users code-free. With functions and formulas for name translation, name matching, sentiment analysis, entity extraction, categorization, tokenization, and morphological analysis, the Rosette for Excel plugin makes doing textual analysis in Excel easy. Got a spreadsheet with a column of names in Korean? Use the Rosette for Excel `=TranslateName` formula to translate them into English, the same way you would use the `=SUM` formula. Inundated with customer reviews in Spanish? Use the Sentiment Analysis function to quickly group the reviews as positive, negative, or neutral. 
## Installation
Rosette for Excel is currently available for Windows OS only. The present beta release has been tested in Office 2010, 2013, and 2016 on Windows 7 and 10, with broader support on its way for the upcoming GA release. To install:
* Head to the Rosette for Excel [release page](https://github.com/rosette-api-community/rosette-for-excel/releases) on the Rosette API Community GitHub
* Click on the link to the most recent release 

Under **Downloads** click **RosetteForExcel.msi** 

! Image 1

Once the .msi file downloads onto your machine, double-click to install. The installation is "per user” so no elevated permissions should be required.

Open Excel. You should see a new tab called **ROSETTE**, as well as a Rosette icon and menu in the **Formulas** tab:

! Image 2

## Getting Started
Before you can actually start using the plug-in, you’ll need an active Rosette API key. If you already have a Rosette developer account, you can enter your information using the dialog found in the **ROSETTE** tab.

! Image 3

If you don’t already have a Rosette account, click the **Sign Up** button or head to developer.rosette.com to get your free Rosette API key (no credit card required). 

! Image 4

Once you’ve completed the signup and activation process, enter your key in the **API Key** dialog in the **ROSETTE** tab. Click the **Check Key** button to make sure your connection is working. If a green check appears, you’re good to go! 

! Image 5

## Translating Names
The Rosette for Excel plugin supports a wide range of features using formulas and ribbon functions. In this guide we’ll look at both applied to a quick name translation use-case.
### Technique 1: Formulas
Say I have a list of Japanese names written in Kana and Kanji characters that I would like to translate into English. In this case they happen to be Japanese baseball players. Perhaps I work in baseball recruiting and I’ve found a list of the top-mentioned Japanese baseball players on social media. I’d like to know the players’ names in English. In my Excel sheet I’ve made two new columns to hold the English translations of the players’ first and last names (though Rosette also supports combined first/last name translations as well as locations and organizations).

! Image 6

In the first cell where I’d like to have a translation, I select **Translate Names** from the Rosette drop down menu in the **Formulas** tab. A dialog box appears with several options, or parameters.

! Image 7

A few important things to know about the parameters: 
1. `Name`: The cell that contains the name you’re trying to translate. If your name is part of a larger string of words, you’ll need to use the entity extraction ribbon function to pull out the names individually first, or your results won’t be accurate (see the second half of this guide).
2. `TargetLanguage`: The language you’d like to translate the name to. Use the three-letter ISO code, which can be found in our [features and functions guide](https://developer.rosette.com/features-and-functions)).
3. `EntityType`: If you know the type of name (`PERSON`, `LOCATION`, or `ORGANIZATION`) you’re translating, specify it here. If you’re not sure, Rosette will make its best guess. Note, this parameter only accepts `PERSON`, `LOCATION`, or `ORGANIZATION` as input.
4. `SourceLanguageOfUse`: If you know the language the name is written in (in this case Japanese), specify it here using the three-letter ISO code. Again, if you’re not sure, Rosette will run its own identification algorithm. 
5. `SourceScript`: If known, the script the name to be translated is written in. I left this one blank, because I could see that two different scripts were present in the list (Kana and Kanji). Check out the [features and functions guide](https://developer.rosette.com/features-and-functions) for the appropriate script abbreviations.
6. SourceLanguageOfOrigin: The three-letter ISO code for the language a name originated in. This is especially helpful for names that have already been transliterated from their original language/script. If the name to be translated was “Vladimir Nabokov” you could input `rus` for “Russian”. 
7. TargetScript: The script you’d like the translation written in (again using the four-letter script abbreviation). For example, when translating from English to Korean, you can specify whether you’d like the script written in Hangul (hang) or Hanja (hani). 
8. TargetScheme: If you’re transliterating names, set your target scheme here using the transliteration scheme abbreviation (for most users this should be left blank).

Note: Parameters can also be set using cell data. If you regularly process lists of names in different languages, it would be easy to create a template with all the necessary parameter information built in!

Once you’ve set the appropriate parameters, click **OK**, and the translated name will appear in the selected cell. If you get a `#VALUE!` error, check your language codes and script abbreviations. 

! Image 8

If you’d like to apply the same settings to a whole list of names, select the cell with the formula and drag down, just as you would with a mathematical Excel formula. The translated names will appear in the cells as you go.

! Image 9

### Technique 2: Ribbon Functions
Say instead of having a list of names, I have an Excel sheet populated with sentences (think newspaper headlines or short biographies) about Japanese baseball players. I want to know which players are being discussed, but in order to translate their names I first need to extract them. 

In my sheet, I select the cells that contain the relevant text. In the **ROSETTE** tab I click the **Extract Entities** icon in the ribbon and hit the **Go** button. A status bar will appear on the right hand side to show Rosette’s progress. When it finishes, you’ll see an option to open your results, which will appear in a new sheet. 

! Image 10

In the results sheet I can see the extracted entities and their type. In this case let’s say I’m interested in the locations and organizations mentioned in the text in addition to the names. 

First, I’ll  sort the sheet by “Entity Type.” 

! Image 11

Then, I’ll feed the `PERSON`, `LOCATION`, and `ORGANIZATION` entities into the **Translate Names** function. 

! Image 12

Again, I’ll see my results in a new sheet.

! Image 13

If I wanted, I could copy and paste the column of translated names back over to my extracted entities sheet, which would also link me back to my original sentences. I could also use a formula instead of a ribbon function to produce the same effect. Below, I’ve added a column to my extracted entities sheet, and run the **Translate Names** formula on the extracted entities.

! Image 14

Baseball players aren’t the only names you might want to translate. If your business operates in multiple countries, with sales representatives using different languages and scripts to track leads and opportunities, imagine running this process on your SalesForce records. You could also use Rosette to analyze reviews or comments submitted by visitors to your website from around the world. 
## Next Steps
In addition to name translation and entity extraction, the Rosette for Excel plugin also includes sentiment analysis, categorization, tokenization, name matching, and morphological analysis functionality. For more information, check out the GitHub [use info document](/UseInfo.md) and refer to our [features and functions guide](https://developer.rosette.com/features-and-functions) for full language support and error code listings. 

Are you working on a cool project with Rosette for Excel that you’d like us to showcase on our blog? [Get in touch](mailto:community@rosette.com)! You can also reach our support team by emailing support@rosette.com. 
