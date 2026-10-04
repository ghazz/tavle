# Tavle goals

## Finished when

Tavle is an ambient dashboard in daily use: information understood at a
glance, plus a small set of bounded actions (fixed actions, refresh,
acknowledgement, small structured choices). It is the common frontend that
other projects integrate with themselves, without moving their domain logic
into Tavle. A set of useful everyday modules exercises its distinct
capabilities.

Not a goal: general input, text entry or editing, or replacing a full
computer interface.

## Restrictions, set before implementation

Full text: `docs/core-requirements-fixed-constraints.md`.

- Built and deployed with NixOS; everything known before runtime is
  computed at build.
- Modules are thin, pluggable units with standard default paths.
- Little to no resource cost: near-zero idle cost, nothing resident where
  avoidable; scheduled or event-triggered work producing flat snapshots,
  not a resident runtime per module.
- Existing systems over our own code; ours is Nix glue and module data
  shaping.
- Producing and holding items is separate from showing them.
- Content works in a minimal text client; graphical clients are optional.
- Buttons that run predefined tasks are the minimum interaction.
- Local first; data goes only to configured peers. Small state transfers
  between nodes are preferred over duplicated polling.
