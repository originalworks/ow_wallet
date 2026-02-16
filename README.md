# OW EVM Wallet Adapter

Rust adapter for an EVM wallet library with optional AWS KMS integration, developed by Original Works.

This crate provides a unified interface for signing EVM transactions either with a local private key or via AWS KMS.

## Configuration

The library expects the following environment variables (see .env.example):

### Required

- `RPC_URL` - RPC endpoint of the target EVM network.

### Optional

- `USE_KMS` - Enables KMS signing. Defaults to false if not defined.

### Conditional

- `SIGNER_KMS_ID` - Required when USE_KMS=true. Identifier of the AWS KMS key used for signing.

- `PRIVATE_KEY` - Required when USE_KMS is not true. Hex-encoded EVM private key.
