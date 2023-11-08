---
feature: canonical-domain
start-date: 2023-11-06
author: Silvan Mosberger
co-authors: (find a buddy later to help out with the RFC)
shepherd-team: (names, to be nominated and accepted by RFC steering committee)
shepherd-leader: (name to be appointed by RFC steering committee)
related-issues: (will contain links to implementation PRs)
---

# Summary
[summary]: #summary

Use `nix.dev` as the canonical domain for all official Nix projects.

# Motivation
[motivation]: #motivation

- `nixos.org` is incongruent since it's not just about NixOS.
- Having both `nixos.org` and `nix.dev` is not great because it looks like both can't be official (but they are)
- `nixos.com` is an adult escort website, it would be better to distance ourselves a bit from it :)

# Detailed design
[design]: #detailed-design

1. Move the current contents of `nix.dev` to the subdomain `docs.nix.dev`.
2. Move the current contents of `nixos.org` to `nix.dev`, keeping `nixos.org` registered

# Examples and Interactions
[examples-and-interactions]: #examples-and-interactions

## Redirects
Generally all subdomains and links should continue working using appropriate redirects.

Some problems might occur for destinations that are valid for both `nixos.org` and `nix.dev` (e.g. both having `nixos.org/install`/`nix.dev/install`)

Some problems may also occur for `cache.nixos.org` and `tarballs.nixos.org`.
In such a case, these domains could be temporarily mirrored until the problem can be resolved.

## Ownership
Both nix.dev and nixos.org are already controlled by the NixOS foundation, so there's no change in ownership.

## Sources
The sources for all pages will stay the same for now:
- The new `docs.nix.dev` will use the same source as the current `nix.dev`: https://github.com/NixOS/nix.dev
- The new `nix.dev` will use the same source as the current `nixos.org`: https://github.com/NixOS/nixos-homepage

# Drawbacks
[drawbacks]: #drawbacks

The `.dev` TLD might invoke the feeling that Nix is only meant for developers, when really NixOS can also be used by non-developers.

# Alternatives
[alternatives]: #alternatives

- Try to get the registered but unused `nix.org`
  - (+) Shorter than `nixos.org`
  - (-) As a three-letter domain name it would likely be very expensive, probably in the order of $10'000 to $100'000 to buy
- Use `nix-platform.org` or `nix-platform.com` (@infinisil squatted these for now in case we want to use one)
  - (+) Would also allow establishing the term _Nix Platform_ as the combination of all official Nix projects, mainly including Nix, NixOS and Nixpkgs.
  - (-) _Nix Platform_ is [not a widely agreed-upon term](https://github.com/NixOS/nix.dev/pull/575#pullrequestreview-1455203487). It would require an independent discussion to establish it, and thus unduly grow the scope of this proposal.
  - (-) Those domain names are rather long.
- Moving the current contents of `nix.dev` under `docs.nixos.org`
  - (+) Allows keeping `nixos.org` as the canonical domain
  - (-) Doesn't avoid the confusion regarding NixOS
- Trivial alternative of not doing anything and keeping both `nix.dev` and `nixos.org` as official websites.
  - (+) Doesn't require any effort
  - (-) Doesn't avoid the confusions about officiality of `nix.dev` and non-NixOS uses

# Prior art
[prior-art]: #prior-art

- https://github.com/NixOS/foundation/issues/34
- https://github.com/NixOS/nix.dev/issues/290
- https://github.com/NixOS/nixos-homepage/issues/633
- https://discourse.nixos.org/t/nix-related-domains-that-i-control/10034
- https://github.com/NixOS/nix.dev/issues/285
- https://github.com/NixOS/nixos-homepage/pull/882
- https://github.com/NixOS/nixos-homepage/issues/828

# Unresolved questions
[unresolved]: #unresolved-questions

# Future work
[future]: #future-work

- Figure out whether the sources (and/or the styles) of the two websites should be unified.
