# voting-anchor

Anchor program for a simple on-chain voting system: create polls, register candidates, and cast votes within a time window.

Built as part of the [Solana Foundation Bootcamp 2026](https://github.com/solana-foundation/solana-bootcamp-2026) voting exercise. The companion Rails dApp that interacts with this program lives at [solrengine/voting](https://github.com/solrengine/voting).

## Program

- Program ID: `2F1Z4eTmFqbjAnNWaDXXScoBYLMFn1gTasVy2mfPTeJx`
- Anchor: `1.0.0`
- Cluster: `localnet` (see `Anchor.toml`)

### Instructions

- `initialize_poll(poll_id, start_time, end_time, name, description)` — create a poll PDA keyed by `poll_id`.
- `initialize_candidate(poll_id, candidate)` — register a candidate PDA under the poll.
- `vote(poll_id, candidate)` — increment a candidate's vote count, gated by the poll's start/end times.

## Getting started

```bash
yarn install
anchor build
anchor test
```

Integration tests run against [LiteSVM](https://github.com/LiteSVM/litesvm) via `cargo test`.

## References

- Original bootcamp material: https://github.com/solana-foundation/solana-bootcamp-2026
- Rails dApp client: https://github.com/solrengine/voting
