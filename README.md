# NLP resources for Serbian and Serbo-Croatian

Wikipedia and Wiktionary resources are distributed under the [CC BY-SA 3.0 license](https://creativecommons.org/licenses/by-sa/3.0/).

All dictionaries were parsed using Python 3.8.3. The regex library [re](https://docs.python.org/3/library/re.html) was used to match the structure of dictionary entries and extract the data. 

The XML structure is specified according to [TEI Lex0](https://dariah-eric.github.io/lexicalresources/pages/TEILex0/TEILex0.html), with a few additional tags. 

The Wiktionary synonyms and definitions were collected from the [Wiktionary dump](https://dumps.wikimedia.org/srwiktionary/) of September 2020. The \<entry>s contain an orthographic form (\<orth>) of a word and grammatical information group (\<gram>). Entries contain senses inside \<sense> tags, each with a list of \<xr type="synonymy"> cross-referencing synonyms. Since we extracted both synonyms and definitions from SH Wiktionary, there are two corresponding files. Definitions are either given as text or are derived from synonyms. In the definitions file, in addition to the orthographic form, we also recorded syllables (\<hyph>) and pronunciation information (\<pron>) tags. We kept all styling information, abbreviations and node descriptions inside \<innerlink> tags.

The [Systematic Dictionary of Serbo-Croatian](https://sr.wikisource.org/wiki/%D0%A1%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D1%81%D0%BA%D0%B8_%D1%80%D0%B5%D1%87%D0%BD%D0%B8%D0%BA_%D1%81%D1%80%D0%BF%D1%81%D0%BA%D0%BE%D1%85%D1%80%D0%B2%D0%B0%D1%82%D1%81%D0%BA%D0%BE%D0%B3_%D1%98%D0%B5%D0%B7%D0%B8%D0%BA%D0%B0_(1936)) contains words related to each other via systematic groups. We chose the first words from a group as a group name. Sets of words in a group are divided into subgroups and they were recorded as senses, with cross-referenced words in \<xr type=”related”> tags. Subgroups that were not synonymous to the group (antonyms, for example) were recorded under \<relations> tag, with \<relation> representing a related group that can contain its own senses and words.
