Felix is an open-source broker for streams, caches and queues, written in Rust.
It stores every stream, cache and queue in one replicated log, and clients
reach it over QUIC. Subscribers resume from an offset, so they can tell exactly
which records they missed. One slow subscriber can't hold up the others.
Durable streams can require a majority of replicas to acknowledge each write.

This organization holds Felix and some of the projects built on it. Each one runs on
Felix alone, with no other datastore, and can be self-hosted.

## Projects

| Repository | What it is | Status |
|---|---|---|
| [felix](https://github.com/GetFelix/felix) | The broker, the control plane, client libraries for Rust, Python and TypeScript, and `felixctl` | 0.6.0-preview.2 |
| [felix-canvas](https://github.com/GetFelix/felix-canvas) | A multiplayer drawing canvas with live cursors, rich text, history you can scrub, and per-room sign-in | 0.2.0 |
| [felix-webhook-relay](https://github.com/GetFelix/felix-webhook-relay) | A webhook relay that stores each webhook durably, delivers it with retries, and replays any endpoint after an outage | 0.1.0 |
| [felix-arena](https://github.com/GetFelix/felix-arena) | A browser arena game in 3D, with a kill cam replayed from the match's log | Design stage |
| [felix-gateway](https://github.com/GetFelix/felix-gateway) | A WebSocket gateway between browsers and Felix, with each connection narrowed to one scope | 0.2.0 |

## Getting started

- The [Felix README](https://github.com/GetFelix/felix#readme) covers running a broker and the client libraries.
- Each project's README has a quick start, and its docs/ folder has the design.

## Contributing

Issues and pull requests are welcome in each repository. Each one's
CONTRIBUTING.md explains how its code and docs are organized.
