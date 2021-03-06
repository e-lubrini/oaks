# swagger-client
FRED is a tool for automatically producing RDF/OWL ontologies and linked data from natural language sentences. The method is based on Combinatory Categorial Grammar, Discourse Representation Theory, Linguistic Frames, and Ontology Design Patterns. Results are enriched with NER and WSD. 

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com//.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com//.git`)

Then import the package:
```python
import swagger_client 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import swagger_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
authorization = 'authorization_example' # str | The authorization bearear. Type \"Bearer xxx-yyy-zzz\", where is your secret token.
text = 'text_example' # str | The input natural language text.
prefix = 'prefix_example' # str | The prefix used for the namespace of terms introduced by FRED in the output. If not specified fred: is used as default. (optional)
namespace = 'namespace_example' # str | The namespace used for the terms introduced by FRED in the output. If not specified http://www.ontologydesignpatterns.org/ont/fred/domain.owl# is used as default. (optional)
wsd = true # bool | Perform Word Sense Disambiguation on input terms. By default it is set to false. (optional)
wfd = true # bool | Perform Word Frame Disambiguation on input terms in order to provide alignments to WordNet synsets, WordNet Super-senses and Dolce classes. By default it is set to false. (optional)
wfd_profile = 'b' # str | The profile associated with the Word Frame Disambiguation (optional) (default to b)
tense = true # bool | Include temporal relations between events according to their grammatical tense. By default it is set to false. (optional)
roles = true # bool | Use FrameNet roles into the resulting ontology. By default it is set to false. (optional)
textannotation = 'earmark' # str | The vocabulary used for annotating the text in RDF. Two possible alternatives are available, i.e. EARMARK and NIF. (optional) (default to earmark)
semantic_subgraph = true # bool | Generate a RDF which only expresses the semantics of a sentence without additional RDF triples, such as those containing text spans, part-of-speeches, etc. By default it is set to false. (optional)

try:
    api_instance.stlab_tools_fred_get(authorization, text, prefix=prefix, namespace=namespace, wsd=wsd, wfd=wfd, wfd_profile=wfd_profile, tense=tense, roles=roles, textannotation=textannotation, semantic_subgraph=semantic_subgraph)
except ApiException as e:
    print("Exception when calling DefaultApi->stlab_tools_fred_get: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**stlab_tools_fred_get**](docs/DefaultApi.md#stlab_tools_fred_get) | **GET** /stlab-tools/fred | 


## Documentation For Models



## Documentation For Authorization

 All endpoints do not require authorization.


## Author



