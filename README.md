# BlackHoles.fyi plugins

[BlackHoles.fyi](https://blackholes.fyi) draws real black holes live in your browser, from
their measured numbers. This repository is its plugin marketplace for
[Claude Code](https://claude.com/claude-code).

## The `blackholes` plugin

It adds two things:

- **The BlackHoles.fyi MCP server** (`https://mcp.blackholes.fyi/mcp`). It gives your
  assistant a catalogue of eleven real black holes, each with its published
  measurements and the paper every number came from. Where the assistant
  can draw one, it puts a live image of the black hole in the chat.
- **A skill** that tells the assistant how to use the server: answer from
  the catalogue's numbers and give their sources, look up a black hole that
  is not in the catalogue in a set order, and say which numbers are its own.

The server is free, needs no account and only reads.

## Install

In Claude Code, run these two commands:

```text
/plugin marketplace add blackholes-fyi/plugins
/plugin install blackholes@blackholes-fyi
```

Then ask, for example, "Show me Cygnus X-1".

## Other assistants

Claude, ChatGPT and other assistants add the server by its address. The
steps, and the skill as a plain file, are on
[blackholes.fyi/agents](https://blackholes.fyi/agents).

## Licence

MIT, for what is in this repository: the skill, this page and the plugin's
manifests. The site's own code and images are not part of it.

## Changes

The files here are generated from the site's own source, so changes are
made there. To report a problem, write to
[hello@blackholes.fyi](mailto:hello@blackholes.fyi).
