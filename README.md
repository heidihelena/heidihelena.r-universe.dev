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
  c("vahtian", "vahtian.epinet", "recoverlite"),
  repos = c("https://heidihelena.r-universe.dev", "https://cloud.r-project.org")
)
```

(The CRAN mirror is included so dependencies resolve.)

## Packages

| Package | What it does | Source |
|---|---|---|
| [![vahtian](https://heidihelena.r-universe.dev/badges/vahtian)](https://heidihelena.r-universe.dev/vahtian) **vahtian** | Reproducible, provenance-first evidence tooling — freeze a record set into a content-hashed, provenance-stamped corpus, verify it (tamper-evident), and keep a hash-chained audit trail. Byte-identical with the Python package [`vahtian`](https://pypi.org/project/vahtian/). | [heidihelena/vahtian](https://github.com/heidihelena/vahtian) · `packages/vahtian-r` |
| [![vahtian.epinet](https://heidihelena.r-universe.dev/badges/vahtian.epinet)](https://heidihelena.r-universe.dev/vahtian.epinet) **vahtian.epinet** | R interface to EpiNet — honestly evaluated outcome models on tabular and graph-shaped data: calibration, permutation nulls, model cards, closed-form contestability. Research demonstrator, not clinical decision support. | [heidihelena/epinet](https://github.com/heidihelena/epinet) · `r/vahtian.epinet` |
| [![recoverlite](https://heidihelena.r-universe.dev/badges/recoverlite)](https://heidihelena.r-universe.dev/recoverlite) **recoverlite** | Pre-data recovery tests for planned study designs — simulate a declared design–analysis pair over a crossed scenario grid (null/target effects × declared/pessimistic nuisance assumptions) and get a PASS/RISK/FAIL verdict with Monte-Carlo-aware diagnosands: power, bias split into estimator bias and estimand drift, coverage, Type S/M, model failure. Companion to the recovery-test methods paper. | [heidihelena/recoverlite](https://github.com/heidihelena/recoverlite) |

## Adding a package

Append an entry to [`packages.json`](packages.json):

```json
{ "package": "<name>", "url": "https://github.com/heidihelena/<repo>", "subdir": "<path>" }
```

`package` must match the `Package:` field in that package's `DESCRIPTION`; omit
`subdir` if the package is at the repo root.

---

Maintained by [Heidi Helena Andersén](https://orcid.org/0000-0001-5923-5865).
`vahtian` and `vahtian.epinet` are part of [Vahtian](https://vahtian.com) —
human-first, auditable research tooling; `recoverlite` accompanies the
recovery-test methods paper. Apache-2.0 where applicable.
