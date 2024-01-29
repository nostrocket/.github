## Nostrocket!

A Nostrocket client is a state machine that subscribes to a Nostrocket thread and parses events against the protocol, rebuilding the current state of the rocket. 

Different parts of the state machine can run in different places, e.g. much of the state can be rebuilt directly in the browser, but computationally heavy operations like indexing a large number of nostr events or validating the Bitcoin blockchain (some parts of the protocol also require knowledge of the current state of Bitcoin) are better done closer to the metal and can utilize DVMs etc.

[Oxygen](https://github.com/nostrocket/oxygen) is in active development. This builds a subjective view of Nostrocket state in the browser.   
[NIPs](https://github.com/nostrocket/NIPS).   
[Consensus and state transitions](https://github.com/nostrocket/NIPS/blob/main/state.md) to understand consensus and state transitions.
