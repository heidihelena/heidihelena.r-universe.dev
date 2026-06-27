# heidihelena.r-universe.dev

The [R-universe](https://r-universe.dev) registry for **Heidi Helena Andersén**'s
R packages, https://orcid.org/0000-0001-5923-5865. This repository is just an *index* — a single `packages.json` that
points R-universe at the source repositories. The package code lives in those
repos; nothing is duplicated here.

R-universe rebuilds the packages on every push to their sources and serves them
at **<https://heidihelena.r-universe.dev>**.

## Install

```r
install.packages(
  c("vahtian", "vahtian.epinet"),
  repos = c("https://heidihelena.r-universe.dev", "https://cloud.r-project.org")
)
```

(The CRAN mirror is included so dependencies resolve.)

## Packages

| Package | What it does | Source |
|---|---|---|
| [![vahtian](https://heidihelena.r-universe.dev/badges/vahtian)](https://heidihelena.r-universe.dev/vahtian) **vahtian** | Reproducible, provenance-first evidence tooling — freeze a record set into a content-hashed, provenance-stamped corpus, verify it (tamper-evident), and keep a hash-chained audit trail. Byte-identical with the Python package [`vahtian`](https://pypi.org/project/vahtian/). | [heidihelena/vahtian](https://github.com/heidihelena/vahtian) · `packages/vahtian-r` |
| [![vahtian.epinet](https://heidihelena.r-universe.dev/badges/vahtian.epinet)](https://heidihelena.r-universe.dev/vahtian.epinet) **vahtian.epinet** | Epistemic network analysis. | [heidihelena/epinet](https://github.com/heidihelena/epinet) · `r/vahtian.epinet` |

## Adding a package

Append an entry to [`packages.json`](packages.json):

```json
{ "package": "<name>", "url": "https://github.com/heidihelena/<repo>", "subdir": "<path>" }
```

`package` must match the `Package:` field in that package's `DESCRIPTION`; omit
`subdir` if the package is at the repo root.

---

Part of [Vahtian](https://vahtian.com) — human-first, auditable research tooling.
Apache-2.0 where applicable.
```
