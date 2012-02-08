Visualization Design
====================

One of the major goals of this project is to develop a new visualization to
better express profiling data. My goal is to take `this`_ visualization [#]_ and
extend and improve it. One of the major advantage of this visualization is it
gives not only good information about how long calls took, but provides context
about the call graph and the timeline of the program. Some of the key goals
are:

* See individual functions taking a large portion of the execution time.
* See smaller functions which are called repeatedly and in aggregate take a
  large portion of the execution time.
* Have a sense of the timeline of the program, preferably overlaid with other
  key timeline events, such as:

  * VM data (JIT compilation, GC minor, GC major).
  * User application metadata.

Some of the interaction mechanisms envisioned (which will need to be mapped to
user input somehow):

* Zooming in on a single call, and it's sub calls.
* Graying out data:

  * All non-child calls.
  * All calls not to the same function.
  * All calls in different classes, modules, packages, etc.
* Coloring by other considerations (default coloring is "same call, same
  color"):

  * By call frequency (more saturated, more frequently called?)

* Reorganization of the visualization based on other events (timeline view is
  the default):

  * Based on total call time (one function per-line).


Some input mechanisms available:

* Hover (including a delayed hover)
* Click
* Double click
* A filter box


.. [#] `Originally developed by Neelakanth Nadgir`_

.. _`this`: http://blogs.oracle.com/realneel/resource/open_table_hash_walk.svg
.. _`Originally developed by Neelakanth Nadgir`: http://blogs.oracle.com/realneel/entry/visualizing_callstacks_via_dtrace_and