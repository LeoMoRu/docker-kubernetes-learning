
=== Respuesta si errores ===
{'apiVersion': 'v1', 'kind': 'Pod', 'metadata': {'name': 'mi-primer-pod', 'labels': {'app': 'nginx'}}, 'spec': {'containers': [{'name': 'web', 'image': 'nginx:alpine', 'ports': [{'containerPort': 80}]}]}}


=== Se quita un espacio de identacion en image ===
  File "<string>", line 1, in <module>
    import yaml; print(yaml.safe_load(open('pod-example.yaml')))
                       ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/__init__.py", line 125, in safe_load
    return load(stream, SafeLoader)
  File "/usr/lib/python3.14/site-packages/yaml/__init__.py", line 81, in load
    return loader.get_single_data()
           ~~~~~~~~~~~~~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/constructor.py", line 49, in get_single_data
    node = self.get_single_node()
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 36, in get_single_node
    document = self.compose_document()
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 55, in compose_document
    node = self.compose_node(None, None)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 84, in compose_node
    node = self.compose_mapping_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 133, in compose_mapping_node
    item_value = self.compose_node(node, item_key)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 84, in compose_node
    node = self.compose_mapping_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 133, in compose_mapping_node
    item_value = self.compose_node(node, item_key)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 82, in compose_node
    node = self.compose_sequence_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 111, in compose_sequence_node
    node.value.append(self.compose_node(node, index))
                      ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 84, in compose_node
    node = self.compose_mapping_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 127, in compose_mapping_node
    while not self.check_event(MappingEndEvent):
              ~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/parser.py", line 98, in check_event
    self.current_event = self.state()
                         ~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/parser.py", line 428, in parse_block_mapping_key
    if self.check_token(KeyToken):
       ~~~~~~~~~~~~~~~~^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/scanner.py", line 115, in check_token
    while self.need_more_tokens():
          ~~~~~~~~~~~~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/scanner.py", line 152, in need_more_tokens
    self.stale_possible_simple_keys()
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/scanner.py", line 291, in stale_possible_simple_keys
    raise ScannerError("while scanning a simple key", key.mark,
            "could not find expected ':'", self.get_mark())
yaml.scanner.ScannerError: while scanning a simple key
  in "pod-example.yaml", line 10, column 5
could not find expected ':'
  in "pod-example.yaml", line 11, column 5

=== Se usa tabulacion en vez de espacio ===

Traceback (most recent call last):
  File "<string>", line 1, in <module>
    import yaml; print(yaml.safe_load(open('pod-example.yaml')))
                       ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/__init__.py", line 125, in safe_load
    return load(stream, SafeLoader)
  File "/usr/lib/python3.14/site-packages/yaml/__init__.py", line 81, in load
    return loader.get_single_data()
           ~~~~~~~~~~~~~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/constructor.py", line 49, in get_single_data
    node = self.get_single_node()
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 36, in get_single_node
    document = self.compose_document()
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 55, in compose_document
    node = self.compose_node(None, None)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 84, in compose_node
    node = self.compose_mapping_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 133, in compose_mapping_node
    item_value = self.compose_node(node, item_key)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 84, in compose_node
    node = self.compose_mapping_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 133, in compose_mapping_node
    item_value = self.compose_node(node, item_key)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 82, in compose_node
    node = self.compose_sequence_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 111, in compose_sequence_node
    node.value.append(self.compose_node(node, index))
                      ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 84, in compose_node
    node = self.compose_mapping_node(anchor)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 133, in compose_mapping_node
    item_value = self.compose_node(node, item_key)
  File "/usr/lib/python3.14/site-packages/yaml/composer.py", line 64, in compose_node
    if self.check_event(AliasEvent):
       ~~~~~~~~~~~~~~~~^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/parser.py", line 98, in check_event
    self.current_event = self.state()
                         ~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/parser.py", line 449, in parse_block_mapping_value
    if not self.check_token(KeyToken, ValueToken, BlockEndToken):
           ~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.14/site-packages/yaml/scanner.py", line 116, in check_token
    self.fetch_more_tokens()
    ~~~~~~~~~~~~~~~~~~~~~~^^
  File "/usr/lib/python3.14/site-packages/yaml/scanner.py", line 258, in fetch_more_tokens
    raise ScannerError("while scanning for the next token", None,
            "found character %r that cannot start any token" % ch,
            self.get_mark())
yaml.scanner.ScannerError: while scanning for the next token
found character '\t' that cannot start any token
  in "pod-example.yaml", line 10, column 11

=== No se ponen los dos puntos en containerPort ===

{'apiVersion': 'v1', 'kind': 'Pod', 'metadata': {'name': 'mi-primer-pod', 'labels': {'app': 'nginx'}}, 'spec': {'containers': [{'name': 'web', 'image': 'nginx:alpine', 'ports': ['containerPort 80']}]}}
