# VB004: No vulnerability from standard behavior

A vulnerability report can be safely dismissed if the behavior described is a direct
consequence of the software’s correct adherence to a standard or specification.

In these instances the vulnerability (if one exists) is present within the standard itself,
and not the implementation.

## Examples

- Many standards (inadvisedly) require implementors to accept invalid inputs
  under the so-called [robustness principle](https://en.wikipedia.org/wiki/Robustness_principle).
  Behavior that adheres to these requirements is not vulnerable _per se_.

- Behavior stemming from cryptographic requirements that are insecure in isolation but secure by construction.
  For example, MD5 is considered an insecure digest but is not insecure when used in an HMAC-MD5
  construction.

## Nuances

An implementation that _chooses_ to be more strict than the standard requires _should_ be
considered vulnerable if the intended strictness is violated.
