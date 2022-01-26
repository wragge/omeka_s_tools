# Omeka S Tools
> Tools for working with data in an instance of Omeka S


## Install

`pip install omeka-s-tools`

## How to use

[See the documentation](https://wragge.github.io/omeka_s_tools/api.html) for full details of the Omeka API Client.

```python
from omeka_s_tools.api import OmekaAPIClient

omeka = OmekaAPIClient('http://timsherratt.org/collections/api')
```

```python
items = omeka.get_resources('items')
items['total_results']
```




    49



```python
items['results'][0]
```




    {'@context': 'http://timsherratt.org/collections/api-context',
     '@id': 'http://timsherratt.org/collections/api/items/671',
     '@type': ['o:Item', 'schema:Newspaper'],
     'o:id': 671,
     'o:is_public': True,
     'o:owner': {'@id': 'http://timsherratt.org/collections/api/users/1',
      'o:id': 1},
     'o:resource_class': {'@id': 'http://timsherratt.org/collections/api/resource_classes/161',
      'o:id': 161},
     'o:resource_template': {'@id': 'http://timsherratt.org/collections/api/resource_templates/5',
      'o:id': 5},
     'o:thumbnail': None,
     'o:title': "Newcastle Morning Herald and Miners' Advocate (NSW : 1876 - 1954)",
     'thumbnail_display_urls': {'large': None, 'medium': None, 'square': None},
     'o:created': {'@value': '2022-01-20T06:36:11+00:00',
      '@type': 'http://www.w3.org/2001/XMLSchema#dateTime'},
     'o:modified': {'@value': '2022-01-20T06:36:11+00:00',
      '@type': 'http://www.w3.org/2001/XMLSchema#dateTime'},
     'o:media': [],
     'o:item_set': [],
     'o:site': [],
     'schema:name': [{'type': 'literal',
       'property_id': 1116,
       'property_label': 'name',
       'is_public': True,
       '@value': "Newcastle Morning Herald and Miners' Advocate (NSW : 1876 - 1954)"}],
     'schema:url': [{'type': 'uri',
       'property_id': 393,
       'property_label': 'url',
       'is_public': True,
       '@id': 'http://nla.gov.au/nla.news-title356'}],
     'schema:identifier': [{'type': 'literal',
       'property_id': 190,
       'property_label': 'identifier',
       'is_public': True,
       '@value': '356'}]}



See [the documentation](https://wragge.github.io/omeka_s_tools/api.html) for more examples.

----
Created by [Tim Sherratt](https://timsherratt.org) ([@wragge](https://twitter.com/wragge)) for the [GLAM Workbench](https://glam-workbench.net/).
