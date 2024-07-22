# gio-pyio

Python like IO for gio.

[![Documentation Status](https://readthedocs.org/projects/gio-pyio/badge/?version=latest)](https://gio-pyio.readthedocs.io/en/latest/?badge=latest)

This library provides python like IO for Gio. It is intended to bridge the gap
between Gtk apps using GFile for file handling and python libraries that
expect files in the form of 
[file objects](https://docs.python.org/3/glossary.html#term-file-object).

## Usage
See the example below:
```python
file = Gio.File.new_for_path('/path/to/json/file.json')
with gio_pyio.open(file, 'rb') as file_like:
    data = json.load(file_like)
    print(data)
```

For advanced usage see [the reference](https://gio-pyio.readthedocs.io/)
