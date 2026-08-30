# VB001: No vulnerability report without a threat model

A vulnerability report can be safely dismissed if it lacks a threat model, or if the threat model presented is incoherent.

## Examples

- A report for a Python API that raises an exception in some undocumented or surprising cases, but doesn’t explain how an attacker could exploit that behavior to cause harm.

- A report for a hang or stall in a local developer tool. Hangs are undesirable behavior, but the opportunity for harm from one is negligible in a developer tooling context: the developer can always just kill the process.

## Resources

- [Alex Gaynor: Motion to Dismiss for Failure to State a Vulnerability](https://alexgaynor.net/2025/oct/20/motion-to-dismiss/)

## Nuances

Not all projects have a documented threat model, or one is that is easy to deduce.
