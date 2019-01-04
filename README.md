# panmorph
Tagsets and description of Hungarian morphological analysers. 

test

## Tagsets

### MSD (Morphosyntactic Description)

MSD provides harmonised lexical specifications for ten languages, including Hungarian. 

The description of version 3.0 is available [here](http://nl.ijs.si/ME/Vault/V3/msd/html/).

Morphological information is represented in attribute-value pairs, where attributes are marked by positions and values are represented by a single character. The non-applicability of a given attribute is marked by a hyphen. Position 0 encodes part-of-speech, other positions encode other morphological attributes, such as person, number, case. 

For example, `Vmis2s---y` is the code of a main verb in indicative mode, past tense, second person singular, definite conjugation.

The tagset is available in two formats:

* tsv
* pdf

### CoNLL

This is an annotation scheme. 

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
