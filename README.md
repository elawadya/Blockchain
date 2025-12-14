# Blockchain

## Description
This Quantlet implements a minimal blockchain data structure in Python. It creates a **genesis block** and appends new blocks whose hashes are computed via **SHA-256** and linked through the `prev_hash` field, illustrating the core idea of hash-linked blockchains.

## Files
- `Blockchain.py` – Python implementation of a toy blockchain
- `Metainfo.txt` – Quantlet metadata (used to generate the README automatically in the QuantLet workflow)

## How it works
- Each `Block` stores:
  - `data` (string payload)
  - `prev_hash` (hash of the previous block)
  - `hash` (SHA-256 hash over `prev_hash + data`)
- The `Blockchain` starts with a genesis block and provides `add_block()` to append new blocks.

## Requirements
- Python 3.x (standard library only)

## Usage
Run:
```bash
python Blockchain.py
```

## Expected output
The script prints the chain to the console, block by block:
- Data
- Previous hash
- Hash

Example (abbreviated):
```
Blockchain:
Data: Genesis Block
Previous hash: 0
Hash: ...

Data: First block
Previous hash: ...
Hash: ...
```
