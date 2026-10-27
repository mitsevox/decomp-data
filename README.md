# decomp-data

Decompilation progress published by each project's CI and rendered by
[mitsevox.github.io](https://mitsevox.github.io/). Served at `https://mitsevox.github.io/decomp-data/`.

Do not edit measurement files by hand: every file under `data/` except cover art is written by the
publish action in `mitsevox/mitsevox.github.io/.github/actions/publish`, which validates it first.
The format is documented in that repository's `contract/README.md`. A bad publish is undone with
`git revert`.
