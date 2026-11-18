---
name: blackholes
description: Use when someone asks about a real black hole (its mass, spin, distance, how fast it is feeding, what it looks like) or wants to see or compare black holes. Shows them with the BlackHoles.fyi MCP server and answers from its published, cited measurements rather than from memory.
---

# Black holes from BlackHoles.fyi

BlackHoles.fyi draws real black holes live from their measured numbers. Its
MCP server gives you a catalogue of eleven black holes, each with its
published mass, spin, distance and accretion rate (how fast it is taking in
gas), and every number comes with the paper it was taken from. Where your
host can draw one, it also puts a live image of the black hole in the chat,
as a card.

Your job with this skill: answer from those numbers, cite them, and say
plainly when a number is yours and not the catalogue's.

## Before you start

You need the server's three tools: `list_black_holes`, `show_black_hole` and
`compare_black_holes`. If you do not have them, the server is not added.
Tell the person, and give them its address:

```text
https://mcp.blackholes.fyi/mcp
```

It is free and needs no account. In Claude Code the command is:

```text
claude mcp add --transport http blackholes https://mcp.blackholes.fyi/mcp
```

Other assistants add it as a custom connector by that address. Do not answer
from memory as if the numbers came from the catalogue while the tools are
missing.

## A black hole in the catalogue

The eleven are Sagittarius A\*, M87\*, Cygnus X-1, V404 Cygni, GRS 1915+105,
Gaia BH1, Gaia BH3, the GW150914 remnant, TON 618, 3C 273 and M31\*.

1. To show one, call `show_black_hole` with only its name. It takes the
   common name, the catalogue id or a SIMBAD, NED or GWOSC identifier. Pass
   no numbers: the catalogue's own are used.
2. To compare two to four, call `compare_black_holes` with their names.
3. To say what there is, call `list_black_holes`.
4. Answer from the text the tool returns. It carries numbered references:
   keep the numbers beside the figures you quote, and give the reference
   list when you quote a figure.
5. Quote a number with its uncertainty when the tool gives one. Where the
   tool says a value is not measured, or gives several published values
   that disagree, say that. Do not pick one silently.
6. The card is interactive. Tell the person they can drag to look round the
   black hole, and that the button at its top right opens other views and
   the sources. If your host shows no card, the text is the whole answer.

Each has a page on the site, with the same numbers and more images:

- `https://blackholes.fyi/gallery/sgr-a-star`
- `https://blackholes.fyi/gallery/m87-star`
- `https://blackholes.fyi/gallery/cygnus-x-1`
- `https://blackholes.fyi/gallery/v404-cygni`
- `https://blackholes.fyi/gallery/grs-1915-105`
- `https://blackholes.fyi/gallery/gaia-bh1`
- `https://blackholes.fyi/gallery/gaia-bh3`
- `https://blackholes.fyi/gallery/gw150914`
- `https://blackholes.fyi/gallery/ton-618`
- `https://blackholes.fyi/gallery/3c-273`
- `https://blackholes.fyi/gallery/m31-star`

## A black hole that is not in the catalogue

Say first that it is not in the catalogue. Never give figures for it as if
they came from BlackHoles.fyi.

You can still show it, from numbers you look up yourself:

1. Look up its published numbers in this order, because the earlier ones
   change the image most: mass, feed, spin, jet, companions, angle,
   distance. Use the papers, or a database that names its source (NASA ADS,
   arXiv, SIMBAD, NED, GWOSC). Only the mass is required.
2. Work out the feed if no paper gives it. It is the black hole's light
   output as a fraction of its Eddington limit, and the Eddington limit is
   1.26e38 erg/s for each solar mass. A black hole of 10 solar masses has a
   limit of 1.26e39 erg/s, so one shining at 1.26e37 erg/s has a feed of
   0.01.
3. Call `show_black_hole` with the name and each number you found, each with
   its source (the paper, with authors, year and journal).
4. For anything you looked for and did not find, pass `"unknown"` or leave
   it out. Do not guess, and do not fill a gap with a typical value.
5. Pass `"none"` only when observations say so: a feed of `"none"` draws a
   bare dark hole, and a jet of `"none"` says a jet was looked for and not
   seen.
6. Tell the person that these numbers are yours and unchecked. The card says
   so too.
7. Where a number was unknown, the card opens on one image and offers
   others. Call them possibilities, and say that no measurement picks
   between them. The tool's answer lists what is still unknown, so you can
   look again and call the tool a second time.

If the tool answers that the name is not in the catalogue even though you
passed numbers, your host is holding an old copy of the tool list. Tell the
person to refresh or re-add the connector.

## What the tools cannot do

- They do not show two black holes merging, or the site's explanatory
  diagrams. For how black holes work, point to
  `https://blackholes.fyi/explore`.
- They only read: no tool changes anything.
- They hold no black hole beyond the eleven. Everything else is your own
  research, labelled as yours.

## When you are done

Your answer is done when all of these hold:

- Every figure you quote has its reference number, or is marked as your own.
- You have said whether the black hole is in the catalogue.
- Anything unknown is named as unknown, not filled in.
- If a card was shown, you have told the person what they can do with it.
