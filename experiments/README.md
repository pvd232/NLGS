# Project experiments

## Next comparison from the November 13 office hours

Peter wants to find recurring kinds of harm in Casanare testimony, including distinctions absent from existing categories. Zach suggested starting with the hearing text and the English summaries Peter already had. [Meeting discussion](../notes/2026-11-13-horvitz/transcript.md#a07)

| Input to the encoder | Question |
| --- | --- |
| Original hearing passage | Which passages group together when the encoder sees all of the testimony? |
| Generic summary | Which of those relationships survive summarization? |
| Harm-focused summary | Does asking specifically about harm surface similarities across passages about different events? |
| Harm-focused summary with a restorative-justice prompt | How much does an explicit framework change what the model preserves? This was an optional extension. |

For a matched comparison, preserve the mapping from each summary to its source span, use the same passages, encoder and clustering settings across arms, and record the language of each input. Existing summaries may cover an entire hearing. Compare those at the hearing level, or generate passage-level summaries for a passage-level comparison. English summaries paired with Spanish passages introduce a language difference. A same-language summary arm would help distinguish its effect from summarization. These are implementation notes for the proposed experiment.

Inspect the passages behind each apparent cluster before assigning it a name. For the separate retrieval evaluation, the [benchmarking proposal](../proposals/2026-11-13-benchmarking/proposal.pdf) fixes a held-out transcript and candidate pool and compares rankings against human relevance judgments. It specifies Recall@1/5/10 and MRR@10. Expert judgments can evaluate discoveries made without a predefined taxonomy.

## Earlier work

| Record | Where to start |
| --- | --- |
| C-STS color control | [Results and figures](https://github.com/pvd232/JEP/blob/9efa1d385fcc67f4daabc7f606f83263e8cdba0a/training_outputs/color_clustering_20261104/report.md) |
| Frozen-encoder pilot and learned similarity heads | [Experiment report](https://github.com/pvd232/JEP/blob/935dbf363f7a91ea91d8553578d4ce03df7b0ded/training_outputs/moral_geometry_20261110/REPORT.md) |
| Response retrieval and remaining evaluations | [November 10 handoff](https://github.com/pvd232/JEP/blob/935dbf363f7a91ea91d8553578d4ce03df7b0ded/research/followup_20261110/PROJECT_BRIEFING_20261110.md) |
| C-STS revision used in earlier experiments | [Dataset and documentation](https://github.com/pvd232/JEP/tree/9ae8379b2ad134561c1d52e61c34f74bc3304dc1/datasets/csts-jep-revision-v1-1) |

Place new experiment code and run reports in this directory. In each report, record the corpus revision, passage unit, split, model revision, prompt, and evaluation judgments so that another researcher can reproduce the comparison.
