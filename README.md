# Timestamps of unpublished work — Reinaldo M. Silva-Filho

This repository holds only cryptographic timestamps, no content. Each entry proves that a given set of files existed, unchanged, at a given date. The files themselves stay private until they are published.

## What is here
- `carimbos/manifesto_<date>.sha256`: the SHA-256 hash of a manifest. A manifest is a private text file that lists the SHA-256 of every file of the work in progress.
- `carimbos/manifesto_<date>.txt.ots`: an [OpenTimestamps](https://opentimestamps.org) proof that the manifest with that hash existed at that date. The proof is anchored in the Bitcoin blockchain.

The manifests and the files are not published here. A manifest lists file paths, and those reveal the topics.

## How priority is proved later
When a piece of work is published, the corresponding manifest and files can be shown:
1. recompute the SHA-256 of each published file and compare it with its line in the manifest;
2. recompute the SHA-256 of the manifest and compare it with `manifesto_<date>.sha256` here;
3. verify the date with `ots verify manifesto_<date>.txt.ots` (the OpenTimestamps client), or at opentimestamps.org.

The commit history of this repository gives an extra public date for each entry.
