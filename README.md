# pixStem

## Webpage: http://pixstem.org

Webpage (development version): https://gitlab.com/pixstem/pixstem/builds/artifacts/master/file/pages_development/index.html?job=pages_development_branch

Python library for analysing pixelated scanning transmission electron microscopy (STEM) datasets.
Pixelated STEM is using a 2D detector to image the convergent beam electron pattern generated by the electron beam after passing through a material.

The library has implemented several common functions used with these types of datasets, like radial integration and center of mass.
These are implemented as HyperSpy-type signals, where these new signals both inherit the old methods and add many new ones.


Installing
----------

The easiest way is installing using with pip:

```bash
pip3 install pixstem
```

Using
-----

```python
import numpy as np
import pixstem.api as ps
s = ps.PixelatedSTEM(np.random.random(size=(5, 5, 10, 10)))
s_r = s.radial_integration()
```
