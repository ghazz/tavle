# Tavle: fixed constraints

Status: accepted 2026-10-04. The few requirements that every
other document, choice and tool must fit. Everything not listed here is
open to prior art: an established system or standard that does the job is
preferred over our own design, and over earlier decisions.

1. **Built and deployed with NixOS.** Everything known before runtime is
   computed at evaluation and build: configuration, validation, layouts,
   who reads what from whom. A deployed node is a static system.
2. **Pluggable modules.** A module is an independent unit that shapes data
   for presentation. Common needs (fetching, scheduling, publishing,
   validation) have standard default paths, so most modules are thin;
   a module brings its own machinery only where the defaults do not fit.
3. **Little to no resource cost.** For small always-on machines. Prefer
   nothing resident; where something must run, prefer the smallest
   established tool that does the job.
4. **Existing systems over our own implementation.** Our own code is
   limited to Nix glue and module data shaping. Anything else we would
   write needs a stated reason why no existing system fits.
5. **Producing and showing are separate.** Tavle creates and holds items
   and views; renderers are separate clients that fetch and show them.
   Tavle does not make pages or screens.
6. **Renderers of any weight.** Content must be usable by a minimal text
   client (a terminal, Markdown); graphical renderers are optional and
   never required by the content.
7. **Interaction, minimum set.** Buttons that run predefined tasks. Part
   of the generic interface, not a separate system.
8. **Local first.** No dependency on cloud services; data goes only to
   configured peers.

## Suggestions, not requirements

- **One address space.** A renderer requests items the same way whether
  they are on its own node or another; local is just our own address.
  Nodes are peers, with no central node; an unreachable node is normal.
