# decomp-data

Decompilation progress published by each project's CI and rendered by
[mitsevox.github.io](https://mitsevox.github.io/). Served at `https://mitsevox.github.io/decomp-data/`.

Every file under `data/` except cover art is written by the publish action in
`mitsevox/mitsevox.github.io/.github/actions/publish`, which validates it first. The format is
documented in that repository's `contract/README.md`. A bad publish is undone with `git revert`.

Edit a measurement file by hand only to correct published data, and only by the procedure in the
wiki's [Publishing](https://mitsevox.github.io/wiki/publishing/) chapter, "Correcting published
data": edit, run `publish.py reseal` so `latest.json` names the corrected file's new digest, then
check the tree with both readers (`tools/check_data_tree.py` in the site repository) before the
pull request merges.
