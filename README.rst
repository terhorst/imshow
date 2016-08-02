``imshow`` is a command-line utility for visualizing matrices. It is
essentially a wrapper for the ``matplotlib`` / MATLAB command of the
same name.

Usage
-----
.. code:: bash

    $ python -e 'import numpy; numpy.savetxt("array.txt", numpy.random.normal(size=(60, 60)))'
    $ imshow array.txt

produces a PNG image ``array.png`` of a random square matrix with 60 entries per side.

.. figure:: examples/array.png

    Example of default output.

The default output name ``array.png`` can be overridden by specifying a second argument.
The extension of the output file name controls the output format.

.. code:: bash

    $ python -e 'import numpy; numpy.savetxt("array.txt", numpy.random.normal(size=(60, 60)))'
    $ imshow array.txt array.jpg

.. figure:: examples/array.jpg

    The same array in JPEG format.

Several options, detailed in ``imshow -h``, control the appearance of the plot.

.. code:: bash

    $ imshow -g -b array.txt array.2.png

.. figure:: examples/array.2.png

    The same array, with a grid and colormap added.

Requirements
------------
Numpy and ``matplotlib``.

Author
------
Jonathan Terhorst <terhorst@gmail.com>