# python-importtime-graph
Display a treemap of the timings reported by `python -X importtime`

![A treemap sample](/importtime_demo.png?raw=true)

Try it: https://kmichel.github.io/python-importtime-graph/

## Usage

Run your python program with the `-X importtime` option, available
since [Python 3.7][doc].

The program will output timing statistics on stderr :

    import time: self [us] | cumulative | imported package
    import time:       137 |        137 | zipimport
    import time:       674 |        674 | _frozen_importlib_external
    import time:        84 |         84 |     _codecs
    import time:       705 |        789 |   codecs
    import time:       757 |        757 |   encodings.aliases
    import time:      1115 |       2659 | encodings
    import time:       461 |        461 | encodings.utf_8
    import time:       190 |        190 | _signal
    import time:       488 |        488 | encodings.latin_1
    import time:        72 |         72 |     _abc
    import time:       456 |        528 |   abc
    import time:       574 |       1101 | io
    import time:       102 |        102 |   _locale
    import time:       319 |        420 | _bootlocale
 
Copy these stats and then paste them using the button in the web page above.

You can also save the stats to a file and open the file in the web page.

    python -X importtime [YOUR_PROGRAM] 2> importtime.txt

Once rendered, you can download the output in SVG or PNG format.

[doc]: https://docs.python.org/3/using/cmdline.html#id5
