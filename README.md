# Tavle

If you have reached this page from the User-Agent of a request made to your service, thank you for
taking the time to look, and please accept our apology for any trouble it has caused you.

## What this is

Tavle is a small display layer for one household's own machines: it collects a few pieces of public
information (weather, bus departures, waste collection dates and the like) and shows them on a screen
in the hallway. It is not a product and it is not widely deployed. It runs on one or two machines in a
single home.

## How it was made

This code is guide-coded and LLM-assisted: it was written largely by AI coding assistants, working under
one person's direction and review. It has not been independently audited, and it surely contains
mistakes we have not found. Any fault in how it behaves towards your service is ours alone, never
yours.

## How we try to behave towards your service

We ask as little as we can, as rarely as we can:

- one requester per source on a machine, never several copies asking the same thing;
- your caching headers, expiry times and conditional requests are honoured, and a reply you mark
  unchanged is not asked for again;
- a minimum gap between requests, chosen well above what the data needs, and a longer one whenever
  you ask us to wait, slow down or stop;
- data that changes rarely (a timetable, a collection calendar) is fetched rarely, at most weekly;
  short-term data only when a person presses a button for it;
- an identifying User-Agent that leads here.

The requests go through decorum, a small fetcher whose whole purpose is to ask politely and to take no
for an answer.

## If we are a burden

Please tell us, and we will stop at once and change what you ask. You owe us no explanation, and you
need not wait for us: blocking us is entirely your right, and we would understand it. Open an issue
here: https://github.com/ghazz/tavle/issues. There is no contact by email.

## The rest

The goals are in `GOALS.md` and the fixed constraints in
`docs/core-requirements-fixed-constraints.md`. The working code is not published here. Licence: MIT
(`LICENSE`).
