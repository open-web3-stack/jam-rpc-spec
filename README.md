# jam-rpc-spec

JSONRPC spec for JAM nodes. Powered by [open-rpc](https://open-rpc.org).

[Playground Link](https://playground.open-rpc.org/?schemaUrl=https://raw.githubusercontent.com/open-web3-stack/jam-rpc-spec/refs/heads/master/openrpc.json)

# Design Decisions

- Following Polkadot JSON RPC: https://polkadot.js.org/docs/substrate/rpc/
- Return raw encoded bytes instead of human readable JSON types
- Keep it simple and minimal so that it is not too much work for all the implementations to support it

Note: JAM node RPCs are strictly for development/testing/operational purposes only.

End users are not expected to use them. Most of the devs also shouldn't need to use them.

The expected users are: JAM chain node developers, JAM chain operators (validators and node operators), JAM chain indexers, JAM chain dashbaord and debugging telemetry.

Some of the non users are: end users, wallets, exchanges, smart contract developers, dApp developers.

# RPC categories

For network operators:

- system: Get information about the node.
- chain: Get heads details.
- state: Get onchain state.
- telemetry: Get telemetry info.

For development & testing:

Those methods are for development & internal testing only. They should not be exposed to the public.

- codec: Encode/decode bytes.
- testing: To perform confirmation tests.
- debug: Debugging related methods.