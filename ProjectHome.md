hyphenator is a pure Python module to hyphenate text using existing hyphenation dictionaries, like those used by OpenOffice.org.

Usage:

```
>>> from hyphenator import Hyphenator
>>> h = Hyphenator("/usr/share/myspell/hyph_nl_NL.dic")
>>> h.inserted('lettergrepen')
u'let-ter-gre-pen'
>>> h.wrap('autobandventieldopje', 11)
('autoband-', 'ventieldopje')
>>> for pair in h.iterate('Amsterdam'):
...     print pair
...
('Amster', 'dam')
('Am', 'sterdam')
>>>
```

Features:

  * 100% pure Python (2.x, conversion to Python 3 is planned)
  * caches dict files and hyphenated words
  * supports nonstandard hyphenation patterns