# tuw-nlp

NLP utilities developed at TUW informatics

## Install and Quick Start
Install the tuw-nlp repository (Windows shell: run as Administrator):

```
pip install .
```

Then you can parse a sentence as simple as:

```python
from tuw_nlp.grammar.text_to_4lang import TextTo4lang

tfl = TextTo4lang("en", "en_nlp_cache")

fl_graphs = list(tfl("brown dog", depth=1, substitute=False))

# Then the fl_graphs will directly contain a networkx graph object
fl_graphs[0].nodes(data=True)

```
For more examples you can check the jupyter notebook under *notebooks/experiment*


## Modules

### text 

General text processing utilities, contains:
- segmentation: stanza-based processors for word and sentence level segmentation
- patterns: various patterns for text processing tasks 

### graph
Tools for working with graphs, contains:
- utils: misc utilities for working with graphs

### grammar
Tools for generating and using grammars, contains:
- alto: tools for interfacing with the [alto](https://github.com/coli-saar/alto) tool
- irtg: class for representing Interpreted Regular Tree Grammars
- lexicon: Rule lexica for building lexicalized grammars
- ud_fl: grammar-based mapping of [Universal Dependencies](https://universaldependencies.org/) to [4lang]() semantic graphs.
- utils: misc utilities for working with grammars

## Contributing

We welcome all contributions! Please fork this repository and create a branch for your modifications. We suggest getting in touch with us first, by opening an issue or by writing an email to Gabor Recski or Adam Kovacs at firstname.lastname@tuwien.ac.at

## Citing

## License 

MIT license
