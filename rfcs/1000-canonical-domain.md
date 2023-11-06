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

- `nixos.org` is confusing because it's not just about NixOS.
- Having both `nixos.org` and `nix.dev` is not great because it looks like both can't be official (but they are)

# Detailed design
[design]: #detailed-design

1. Move the current contents of `nix.dev` to the subdomain `docs.nix.dev`.
2. Move the current contents of `nixos.org` to `nix.dev`

# Examples and Interactions
[examples-and-interactions]: #examples-and-interactions

# Drawbacks
[drawbacks]: #drawbacks

The `.dev` TLD might invoke the feeling that Nix is only meant for developers, when really NixOS can also be used by non-developers.

# Alternatives
[alternatives]: #alternatives

- Try to get the registered but unused `nix.org`
  - (+) Shorter than `nixos.org`
  - (-) As a three-letter domain name it would likely be very expensive, probably in the order of $10'000 to $100'000 per year
- Use `nix-platform.org` or `nix-platform.com` (@infinisil squatted these for now in case we want to use one)
  - (+) Would also allow establishing the term _Nix Platform_ as the combination of all official Nix projects, mainly including Nix, NixOS and Nixpkgs.
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
