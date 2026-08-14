# Chinese Web Novel Corpus Metadata (BG / BL)

Novel-level metadata for the corpus used in *[PAPER TITLE]* ([AUTHORS], [YEAR]).

The corpus is 198 completed Chinese web novels published on
[JJWXC (晋江文学城)](https://www.jjwxc.net), split evenly between two romance
genres:

| Genre | Label | Novels | Description |
|---|---|---|---|
| BG (言情) | `bg` | 99 | Male/female romance |
| BL (纯爱) | `bl` | 99 | Male/male romance ("boys' love") |

Publication dates span 2010–2025.

## Files

- `data/bg_metadata.csv` — 99 BG novels
- `data/bl_metadata.csv` — 99 BL novels

## Columns

Both files share eight columns scraped from each novel's JJWXC page:

| Column | Description |
|---|---|
| `title` | Novel title as it appears on JJWXC |
| `novelid` | JJWXC novel ID; the page is `https://www.jjwxc.net/onebook.php?novelid=<novelid>` |
| `author` | Author's pen name |
| `publish_date` | Timestamp of the first chapter's publication |
| `category` | JJWXC's own tag string, e.g. `原创-纯爱-架空历史-爱情-主受` |
| `word_count` | Total character count reported by JJWXC (字数) |
| `score` | JJWXC's aggregate popularity score (积分) |
| `progress` | Serialization status; all novels here are `完结` (completed) |

The final two columns name the two romantic leads, and differ by genre:

| File | Columns |
|---|---|
| `bg_metadata.csv` | `male_lead_name`, `female_lead_name` |
| `bl_metadata.csv` | `gong_name` (攻), `shou_name` (受) |

### Lead-pair labels

Lead names are derived from the JJWXC listing and manually verified. They are
**blank for 8 novels** (4 per genre) that have no single central romantic pair —
ensemble casts, multi-couple structures, or works where the site's own tagging
does not resolve to one pair. A blank is a positive annotation meaning "no single
lead pair," not missing data.

## What is not included

The novel texts themselves are under copyright and are **not** redistributed
here. This repository contains only factual bibliographic metadata. The
`novelid` column lets you locate each work on JJWXC directly.

## Citation

<!-- Replace with the paper's BibTeX entry once available. -->

```bibtex
@inproceedings{TODO,
  title     = {TODO},
  author    = {TODO},
  year      = {TODO}
}
```

## License

The metadata in this repository is licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE).

This covers the compiled metadata and annotations only. The novels themselves
remain the copyright of their respective authors.
