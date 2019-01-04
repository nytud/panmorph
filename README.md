# panmorph
Tagsets and description of Hungarian morphological analysers. 


## Tagsets

### MSD (Morphosyntactic Description)

MSD provides harmonised lexical specifications for ten languages, including Hungarian. 

The description of version 3.0 is available [here](http://nl.ijs.si/ME/Vault/V3/msd/html/).

Morphological information is represented in attribute-value pairs, where attributes are marked by positions and values are represented by a single character. The non-applicability of a given attribute is marked by a hyphen. Position 0 encodes part-of-speech, other positions encode other morphological attributes, such as person, number, case. 

For example, `Vmis2s---y` is the code of a main verb in indicative mode, past tense, second person singular, definite conjugation (e.g. _adtad_).

This tagset was used in Szeged Corpus and Treebank 1.0 and 2.0, and this was the output formalism of magyarlanc 1.0 and 2.0, as well. Later, a harmonized MSD-KR tagset has been developed, which is a slightly modified version of the original MSD. This tagset is used in Szeged Corpus and Treebank 2.5 and in magyarlanc 2.0. Here we refer to the latter version as MSD. 

The tagset is available in two formats:

* tsv
* pdf

### CoNLL

This is not a tagset or an annotation scheme, just a format, actually the file format of the CoNLL-2009 shared task _Syntactic and Semantic Dependencies in Multiple Languages_. The original MSD codes are to be converted into a linearized format of attribute-value pairs. The code at position 0 is separated as the POS tag, while the other morphosyntactic attributes are in a linear order based on the MSD positions. For example, the code for the Hungarian verb form _adtad_ mentioned above is: `V SubPOS=m|Mood=i|Tense=s|Per=2|Num=s|Def=y`

The tagset is available in two formats:

* tsv
* pdf

### UD

This is an annotation scheme. 

The tagset is available in two formats:

* tsv
* pdf

### emMorph

This is an annotation scheme. 

The tagset is available in two formats:

* tsv
* pdf


## Converters

### emmorph2msd

The converter is available [in another repo](https://github.com/vadno/emmorph2msd). 

### emmorph2conll

The converter is available [in another repo](https://github.com/vadno/emmorph2conll). 

### emmorph2ud

The converter is available [in another repo](https://github.com/vadno/emmorph2ud). 
