# Working on Tavle (for agents)

Read first, in this order:
- `README.md` -- what Tavle is and its current status.
- `GOALS.md` -- what "finished" means and the agreed restrictions.
- `docs/core-requirements-fixed-constraints.md` -- the fixed constraints every
  design, document and tool choice must fit. Everything not listed there is
  open to prior art: prefer an established system or standard over new design.

Ground rules:
- This repository is public, history included. Do not commit private material:
  personal or household details, credentials, local hostnames or paths,
  session notes, handoffs or task lists. Keep those in your own workspace.
- Prefer existing systems; our own code is limited to Nix glue and module data
  shaping. A proposal to write anything else states why no existing system fits.
- Keep changes small and explain them in the commit message.
