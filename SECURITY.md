# Security policy

## Supported versions

Security fixes go into the current release. Older releases are not patched — please update before reporting an issue you found on an outdated version.

## Reporting a vulnerability

**Please do not open a public issue for a security problem.**

Write to **support@ewitsolutions.com** with "dupEx security" in the subject. Useful in a first message:

  * what an attacker could achieve, and what access they would need for it
  * the dupEx version (Menu → Info shows it) and the package format
  * the distribution and desktop environment
  * a reproduction, if you have one

Reports are read and answered by a person — there is no ticket system behind this address and no automatic reply, so a day or two of silence means nothing beyond that. Please give us time to ship a fix before making details public.

## Why this matters here in particular

dupEx deletes files on request, and it is distributed as signed packages from this repository. Reports that concern either of those — a path that could delete something the user did not select, or anything touching the integrity of the downloads — are the ones we most want to hear about early.

## Verifying a download

Every artifact is signed. `dupex-release-key.asc` on the release page carries the public key, `SHA256SUMS` the digests:

```
gpg --import dupex-release-key.asc
gpg --verify dupex-1.0.0-rc1-x86_64.AppImage.asc dupex-1.0.0-rc1-x86_64.AppImage
sha256sum -c SHA256SUMS --ignore-missing
```
