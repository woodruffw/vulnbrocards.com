# VB005: No vulnerability from documented behavior

A vulnerability report can be safely dismissed if the behavior is documented to
occur, _particularly_ when the documentation explicitly describes the security
implications of the behavior or specific contexts in which the software is unsafe to use.

## Examples

- Python's [`http.server`](https://docs.python.org/3/library/http.server.html)
  is explicitly documented as not suitable for production use, as it only implements
  [basic security checks](https://docs.python.org/3/library/http.server.html#http-server-security).

- Python's [`pickle`](https://docs.python.org/3/library/pickle.html) is explicitly documented
  as not secure, full stop.

## Nuances

A downstream _usage_ that violates the documented guidelines for use may be considered vulnerable.

For example: a report against `pickle` itself (for e.g. enabling code execution) may be safely dismissed,
but a report against a downstream usage of `pickle` that ignores the documented warnings may be
considered valid.

## Credit

Suggested by [Hugo van Kemenade](https://github.com/hugovk).
