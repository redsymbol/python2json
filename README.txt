python2json - Convert python prettyprinted strings to formatted JSON

python2json accepts the string representation of a Python dictionary
that can be represented as a JSON object, and formats it as a JSON
object. By default, the result is pretty printed.

One use case: if your application logging (probably at a debug level)
includes dumping large Python dictionaries, and you need to inspect
one of them for troubleshooting. Once you isolate the log
line, you can copy the (potentially very large) string
representation of the dumped Python object, and paste/pipe it into
python2json to get a more easily inspected formatting.

(Normal JSON formatters, like the excellent json_pp [0], will not
quite work because Python's repr() of a nested dictionary is not
always compatible - especially if you are using a Python version that
prefixes its unicode strings with "u".)

python2json can be used in any situation where you want to transform a
Python object representation into a JSON-compatible representation.

[0] http://search.cpan.org/~makamaka/JSON-PP-2.27103/bin/json_pp

LICENSE

This code is in the public domain.

AUTHOR

Aaron Maxwell - amax AT redsymbol DOT net

