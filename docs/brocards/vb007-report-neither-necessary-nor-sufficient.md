# VB007: The report is neither necessary nor sufficient#

The presence of a vulnerability report (and a CVE or other identifier for that report) is neither necessary nor sufficient for a vulnerability to exist.

This is true in both directions:

- Many vulnerabilities are never formally reported.
- Many formal reports do not describe meaningful vulnerabilities.

Consequently, no _unvalidated_ assumption should ever be made about the relationship between
the presence of a report and the presence of a vulnerability.

## Examples

- A vulnerability report based on a CVE for an upstream component where the
  affected surfaces _are_ used, but the upstream CVE is not a meaningful
  vulnerability.
