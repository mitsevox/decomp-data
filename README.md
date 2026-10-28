# decomp-data

Decompilation progress published by each project's CI and rendered by
[mitsevox.github.io](https://mitsevox.github.io/). Served at `https://mitsevox.github.io/decomp-data/`.

Every file under `data/` except cover art is written by the publish action in
`mitsevox/mitsevox.github.io/.github/actions/publish`, which validates it first. The format is
documented in that repository's `contract/README.md`. A bad publish is undone with `git revert`.

Edit a measurement file by hand only to correct published data, and only by the procedure in the
wiki's [Publishing](https://mitsevox.github.io/wiki/publishing/) chapter, "Correcting published
data". In short: edit; run `publish.py reseal`, which rewrites the digests in `latest.json` and
runs the publisher's check; run `tools/check_data_tree.py` from the site repository, the page's
own validator; open a pull request that states the reason and merge it only when both readers
accept; then run `tools/check_data_tree.py` again on a fresh clone of the merged branch, since this
repository has no CI of its own.
