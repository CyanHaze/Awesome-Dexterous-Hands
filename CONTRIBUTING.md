# Contributing

Thanks for helping improve this list of dexterous-hand resources. Contributions are welcome through pull requests or issues.

## Ways to Contribute

- Add new papers, datasets, simulators, hardware platforms, tutorials, or repositories.
- Fix broken links, typos, missing code links, or incorrect metadata.
- Suggest new categories only when the current taxonomy cannot place the resource cleanly.
- Improve the category definitions when a boundary is ambiguous.

## Category Selection Rules

Choose the most specific section first:

- If the work maps human hand motion, hand-object demonstrations, or human intent to a robot hand, use **Human-to-Robot Hand Retargeting**.
- If the work provides a control interface or data-collection system, use **Dexterous Teleoperation and Data Collection**.
- If the work reconstructs hand-object geometry, contact, object state, or interaction motion from images or video, use **HOI Reconstruction for Dexterous Manipulation**.
- If the work uses tactile sensing on robot hands or for dexterous manipulation, use **Tactile Dexterous Hands**.
- If the work is mainly about a manipulation task, use **Dexterous Manipulation Tasks**.
- If the work introduces a hand design or platform, use **Robot Hands and Hardware Platforms**.
- If the work is mainly a dataset, simulator, benchmark, or evaluation protocol, use **Datasets, Benchmarks, and Simulators**.

Cross-listing is allowed when useful, but keep it limited. A paper should usually appear in one primary section and at most one secondary section.

## Add a Paper

1. Find the best category in `README.md`.
2. Insert the entry in reverse chronological order within that category.
3. Keep the formatting consistent with nearby entries.
4. Add official code or project links when available.
5. Prefer official project/code links over third-party mirrors.

### Format with shields.io Badges

Basic format:

```md
- **ShortName**, "Full Paper Title". [![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX)
```

With project page:

```md
- **ShortName**, "Full Paper Title". [![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX) [![Project](https://img.shields.io/badge/Project-Page-green)](https://project-page-url)
```

With code:

```md
- **ShortName**, "Full Paper Title". [![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/org/repo)
```

If a paper is a recommended starting point, prefix it with `[STAR]`:

```md
- [STAR] **ShortName**, "Full Paper Title". [![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX)
```

## Add a Dataset, Benchmark, Simulator, or Hardware Platform

Use the same style as paper entries, but make the resource type clear in the short name or note.

```md
- **DatasetName**, from "Paper Title". [![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX) [![Project](https://img.shields.io/badge/Project-Page-green)](https://project-page-url)
```

## PR Checklist

- One topic per PR.
- No duplicate entries.
- Links open correctly.
- Entry is in the most specific category.
- Entries are sorted reverse chronologically when possible.
- Formatting matches the surrounding section.
- The resource has a clear connection to dexterous robot hands.

## License

By contributing, you agree that your contributions will be licensed under the repository's MIT License.

