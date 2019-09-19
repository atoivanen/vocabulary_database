# Vocabulary Database

> This repository includes seed data for the Vocabulary app. The source code of the app can be found in separate repositories in https://github.com/atoivanen/vocabulary_backend and https://github.com/atoivanen/vocabulary-frontend.

## vocabulary_word.csv

The vocabulary_word.csv file includes French-Finnish, French-English, and Italian-Finnish dictionaries that have been extracted from dictionaries of [the FreeDict project](https://freedict.org/). Some of the word entries have been modified and new entries have been added.

This file can be imported to the Vocabulary database with the command

```
copy vocabulary_word(lemma,translation,pos,gender,source_lang,target_lang,created_date,modified_date,pronunciation) from 'vocabulary_word.csv' delimiter ';' csv header;
```

To be able to edit imported words in the UI you must include a created_by_id field with your user ID.