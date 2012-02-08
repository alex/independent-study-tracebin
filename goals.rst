Goals
=====

This project has two goals:

1. To create a solid foundation for a long term performance analysis and
   profiling tool for PyPy.
2. To explore new ways of visualization profiling and performance information.

To make these a reality, the following goals must be met:

* The ``tracebin`` client must record useful information on the state of the
  program.
* The ``tracebin`` client must be able to serialize the data and send it to the
  server.
* The server must be able to store the data and display it (without any
  advanced visualization).
* The server must be able to render a page of Python code interpolated with
  resops and machine code.
* The server must be able to display a creative, novel, visualization of the
  data. What exactly this means is still up in the air. Some ideas for this are:

  * A density map of packages, modules, classes, and files based on JIT'd code.
  * An overlay of coverage data vs. trace data, showing what code is traced,
    but not covered by tests.
  *

These more or less need to be completed in the order described.

There is also a likelihood that new features will need to be added to the JIT
hooks, or new inspiration will be needed for the UI/UX/IA of the frontend.
Luckily there are two exceptionally talented friends assisting:

* Maciej Fijalkowski: PyPy core developer, and original developer of the JIT
  hooks.
* Idan Gazit: Brilliant designer, and inspiration for some of the current UI.
