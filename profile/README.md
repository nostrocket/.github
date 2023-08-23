## Nostrocket!

A Nostrocket client is a state machine that subscribes to a Nostrocket thread and parses events against the protocol, rebuilding the current state of the rocket. 

Different parts of the state machine can run in different places, e.g. much of the state can be rebuilt directly in the browser, but computationally heavy operations like indexing a large number of nostr events are better done closer to the metal. Some parts of the protocol also require knowledge of the current state of Bitcoin, and so a full validator needs access to a Bitcoin node that it trusts.

Everything is currently implemented in Golang. This validates/rebuilds state from a Nostrocket thread, and publishes the result. A frontend client can use these events optimistically while performing full validation in the background. Right now, the spaceman implementation simply trusts the results published by the Golang implementation and does not perform any validation.
