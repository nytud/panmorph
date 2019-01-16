# panmorph
Tagsets and description of Hungarian morphological analysers. 


## Tagsets

### MSD (Morphosyntactic Description)

MSD provides harmonised lexical specifications for ten languages, including Hungarian. 

The description of version 3.0 is available [here](http://nl.ijs.si/ME/Vault/V3/msd/html/).

Morphological information is represented in attribute-value pairs, where attributes are marked by positions and values are represented by a single character. The non-applicability of a given attribute is marked by a hyphen. Position 0 encodes part-of-speech, other positions encode other morphological attributes, such as person, number, case. 

For example, `Vmis2s---y` is the code of a main verb in indicative mode, past tense, second person singular, definite conjugation (e.g. _adtad_).

This tagset was used in [Szeged Treebank](http://rgai.inf.u-szeged.hu/index.php?lang=en&page=SzegedTreebank) 1.0 and 2.0, and this was the output formalism of versions 1.0 and 2.0 of [magyarlanc](http://rgai.inf.u-szeged.hu/index.php?lang=en&page=magyarlanc), a toolkit for linguistic processing of Hungarian, as well. Later, a harmonized MSD-KR tagset has been developed, which is a slightly modified version of the original MSD. This tagset is used in Szeged Corpus and Treebank 2.5 and in magyarlanc 2.0. Here we refer to the latter version as MSD. 

The tagset is available in two formats:

* msd.tsv: possible tags of msd scheme. A wordlist was extracted from two sources:
1. the 100000 most frequent words of [Webcorpus](http://mokk.bme.hu/resources/webcorpus/)
1. tokens of Szeged Treebank
These words were morphologically analyzed with magyarlanc 2.0, the list contains only the tags.
* msd.pdf: documentation of the scheme with detailed description of possible values assigned to each POS-tags. The documentation includes co-occurrence matrices.

### CoNLL

This is not a tagset or an annotation scheme, just a format, actually the file format of the CoNLL-2009 shared task [Syntactic and Semantic Dependencies in Multiple Languages](http://aclweb.org/anthology/W09-1201). The original MSD codes are to be converted into a linearized format of attribute-value pairs. The code at position 0 is separated as the POS tag, while the other morphosyntactic attributes are in a linear order based on the MSD positions. Non-applicable attributes have 'none' value. For example, the code for the Hungarian verb form _adtad_ mentioned above is: `V SubPOS=m|Mood=i|Tense=s|Per=2|Num=s|Def=y`

The tagset is available in two formats:

* conll.tsv: sorted list of tags of Szeged Treebank
* conll.pdf: documentation of the scheme with detailed description of possible values assigned to each POS-tags.

### UD

This is an annotation scheme. 

The tagset is available in two formats:

* ud.tsv: possible tags of msd scheme. A wordlist was extracted from two sources:
1. the 100000 most frequent words of [Webcorpus](http://mokk.bme.hu/resources/webcorpus/)
1. tokens of Szeged Treebank
These words were morphologically analyzed with magyarlanc 2.0, the list contains only the tags.
* ud.pdf: documentation of the scheme with detailed description of possible values assigned to each POS-tags. The documentation includes co-occurrence matrices.

### emMorph

This is an annotation scheme. 

The tagset is available in one format:

* emmorph.tsv: possible tags of msd scheme. A wordlist was extracted from two sources:
1. the 100000 most frequent words of [Webcorpus](http://mokk.bme.hu/resources/webcorpus/)
1. tokens of Szeged Treebank

## Morphologically analyzed words of Hungarian

We analyzed the 100000 most frequent words of [Webcorpus](http://mokk.bme.hu/resources/webcorpus/) with emMorph and two versions of magyarlanc. Due to morphological ambiguity multiple analyses might be assigned to a word. The tsv file contains morphological tags of these tools assigned to each word of the wordlist. The .tsv file is made up of 4 columns:
1. token
1. emMorph tags by [emMorph](https://github.com/dlt-rilmta/emMorph)
1. UD tags by [magyarlanc 3.0](http://rgai.inf.u-szeged.hu/index.php?lang=en&page=magyarlanc)
1. MSD tags by magyarlanc 2.0

Possible tags of a token in each column are stored in JSON format. The order of the tags is irrelevant.

No manual corrections were carried out on the tags, therefore the list may contain errors. The analysis were done on november of 2018.

## Converters

* emmorph2msd is available [here](https://github.com/vadno/emmorph2msd). 
* emmorph2conll is available [here](https://github.com/vadno/emmorph2conll). 
* emmorph2ud is available [here](https://github.com/vadno/emmorph2ud). 
