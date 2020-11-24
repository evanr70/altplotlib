==========
altplotlib
==========


altplotlib provides matplotlib-style object oriented bindings to altair.


Description
===========

Create high quality altair plots using more familiar calls.

.. code-block:: python
  
  import altplotlib
  import numpy as np

  rng = np.random.default_rng(seed=42)

  n_points, n_series = 100, 5
  multiple = rng.normal(size=(n_points, n_series)).cumsum(axis=0)
  x = np.linspace(0, 14, n_points)

  axis = altplotlib.AltairAxis()

  axis.plot(multiple[:, :3])
  axis.set_title("Hello, world!")
  axis.set_xlabel("This is my x-axis")
  axis.set_ylabel("This is my y-axis")
  axis.plot(multiple[:, 3], c="xkcd:rust")
  axis.plot(multiple[:, 4], c="tab:cyan")

.. image:: https://raw.githubusercontent.com/evanr70/altplotlib/master/gallery/simple_example.png
