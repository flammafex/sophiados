# SophiaDOS

**Sophia Distributed Operating System**

A kernel for P2P applications. Three primitives—state, authorization, time—no central authority.

## The Problem

Every networked application answers three questions:

1. **What is the current state?**
2. **Who is allowed to do what?**
3. **In what order did things happen?**

Traditional systems answer these with servers: databases, auth providers, synchronized clocks. But servers are single points of failure, censorship, and surveillance.

SophiaDOS answers these questions without servers.

## The Stack

```
┌─────────────────────────────────────────────────────┐
│                   Applications                      │
│     Scarcity · Clout · Prestige · Rendezvous        │
├─────────────────────────────────────────────────────┤
│                    SophiaDOS                        │
│       Hypertoken  ·  Freebird  ·  Witness           │
│         (state)       (auth)       (time)           │
├─────────────────────────────────────────────────────┤
│                Network (P2P/WebRTC)                 │
└─────────────────────────────────────────────────────┘
```

### 🧩 Hypertoken — State

Distributed state synchronization using CRDTs. No consensus required, no leader election, no servers. State converges eventually across all peers.

[hypertoken.ai](https://hypertoken.ai)
[github.com/flammafex/hypertoken](https://github.com/flammafex/hypertoken)

### 🕊️ Freebird — Authorization

Anonymous authorization using Verifiable Oblivious PRFs (VOPRF). Prove you're allowed without revealing who you are. No identity provider, no tracking, no linkability.

[freebird.bot](https://freebird.bot)
[github.com/flammafex/freebird](https://github.com/flammafex/freebird)

### 🙌 Witness — Time

Threshold-signed timestamping with Ed25519/BLS. Prove something existed at a specific time without trusting any single authority. Optional blockchain anchoring for public verifiability.

[witnesses.now](https://witnesses.now)
[github.com/flammafex/witness](https://github.com/flammafex/witness)

## Applications

Software built on SophiaDOS:

| Application | Description |
|-------------|-------------|
| [**🩸 Scarcity**](https://scarbucks) | Digital cash with demurrage. Gossip-based double-spend prevention. |
| [**🌑 Clout**](https://cloutsocial.net/about) | Censorship-resistant social network. Web of Trust filtering. |
| [**🗳️ Prestige**](https://prestige.vote) | Anonymous verifiable voting. Secret ballot, public proof. |
| [**🤝 Rendezvous**](https://rendezvous.icu) | Private mutual matching. Diffie-Hellman reveals only mutual selections. |

## Design Principles

**No servers.** Applications run entirely on user devices, communicating peer-to-peer.

**No accounts.** Authorization without identity. Prove what you can do, not who you are.

**No trust.** Cryptographic verification replaces institutional trust. Don't trust the network; verify the math.

**Offline-first.** State synchronizes when connectivity exists. Applications work without it.

## Getting Started

See individual repositories for detailed documentation.

## License

Apache 2.0. See [LICENSE](LICENSE) for details.

---

*Wisdom, distributed.*
