# spellchecker-tools
## About
This Repository contains a few modified swiss german tools for hunspell based translations tool. Use it on your risk!
If you want to make any additions, feel free to create a pull request.
Please note, that the extension for [open office](https://extensions.openoffice.org/en/project/german-de-ch-frami-dictionaries), [libre office](https://extensions.libreoffice.org/en/extensions/show/german-de-ch-frami-dictionaries) and thunderbird is neither developed nor maintained by backslash. This means, changes in this repository will not have any influence on the original projects.
## Files & Structure

### de-ch
This directory contains the extension which in general can be downloaded in scope of libre office extension. We will enhance especially the dictionary file located under:
/de_CH_frami/de_CH_frami.dic

### additional
The directory additional contains a text file with new words which are not part of the extension yet. We use it in our own spellchecker solution provided by wproofreader to improve the base quality of the dictionary included in the extension. Terms which are listed here should become part of the extension sooner or later, but this takes time… So new terms will be added to the additiona-file first of all and will be mooved to the extension later on.

### Usage on Mac OSX
The dictionary can be used systemwide on OSX. To do so, follow these steps:
1. Open a terminal window
2. Execute this command - it will download and copy the files to correct directory. Please note, that curl is required: 
```
curl -o $HOME/Library/Spelling/de_CH.aff https://raw.githubusercontent.com/backslashag/spellchecker-tools/main/de-ch/dict-de-ch-frami/de_CH_frami/de_CH_frami.aff

curl -o $HOME/Library/Spelling/de_CH.dic https://raw.githubusercontent.com/backslashag/spellchecker-tools/main/de-ch/dict-de-ch-frami/de_CH_frami/de_CH_frami.dic
```

3. Restart the AppleSpell Service. You could kill the process in the activity monitor tool.
4. Reopen the application where you want to use the spellchecker. You should see the new language as 'Deutsch (Schweiz) (Library)'

If you're worried about execution scripts in the terminal, download both files and copy them manuall to the spelling-folder under /Library .

As the dictionary is updated frequently, you can perform the script above regulary. The dictionaries will be overwritten. Please make sure that you restart the AppleSpell service.