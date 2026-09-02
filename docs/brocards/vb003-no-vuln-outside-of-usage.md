# VB003: No vulnerability outside of usage

A vulnerability report can be safely dismissed if it describes a behavior that could occur, but does not in fact occur in actual usage of the software.

## Examples

- Vulnerabilities in private APIs, where all usages of that API are demonstrably
  not affected.

- Re-reports of vulnerabilities in dependencies, where all downstream usage of
  the dependency is demonstrably not affected by the upstream vulnerability.

## Nuances

- Sometimes functionality is *intended* to be unreachable (e.g. a private API),
  but is *in fact* reachable. When this occurs the *intent* behind the privateness
  or interiority of the functionality becomes irrelevant, since the behavior
  can in fact occur.
