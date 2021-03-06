Wikimetrics - Article lists from category tree
==============================================

This module allows to fetch all the URLs of language-specific Wikipedia articles navigating the category tree specified.

The example configuration that we offer aims to get the list of English, Deutsch, French, Italian and Allemanish Wikipedia articles that have a category under https://www.wikidata.org/wiki/Q1456250 (max 3 hops).

Input
-----
```
node run.js
```

To configurate the action of the script, edit the file `config.json`, adjusting the following parameters according to your needs:

* `languages`: list of the language codes of interest (the language code must be the one used in the wikipedia local url, for example English: www.en.wikipedia.org->"en" or "EN")
* `filepath`: the path to the working folder
* `category`: the Wikidata entity corresponding to the category root of your desired tree
* `maxLevel`: the max level of recursion inside the category tree
* `databaseConfig`: the path to the file with the database settings

Output
------

The script will save a number of files in the filepath/1B directory, named `LANGUAGECODE.csv` containg one url per line of the articles of Wikipedia, in the language identified by LANGUAGECODE.
