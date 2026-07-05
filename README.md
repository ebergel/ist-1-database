# IST-1 Database — Frozen Public Mirror

A verbatim, hash-pinned mirror of the **International Stroke Trial (IST-1)
database, version 2**, redistributed under the Open Data Commons
Attribution License (ODC-By). This repository exists so that a specific,
immutable snapshot of the dataset remains reachable and verifiable
independent of any upstream availability.

**This is a mirror, not a source.** The authoritative, canonical release
is the University of Edinburgh deposit below. If you want the dataset for
your own work, prefer the original source; use this mirror only when you
need the exact bytes this snapshot pins.

---

## Canonical source (cite this, not the mirror)

- **Dataset:** International Stroke Trial database (version 2). University
  of Edinburgh, Department of Clinical Neurosciences.
  DOI: **https://doi.org/10.7488/ds/104**
- **Database paper:** Sandercock PAG, Niewada M, Członkowska A; the
  International Stroke Trial Collaborative Group. *The International Stroke
  Trial database.* Trials 2011;12:101.
  DOI: https://doi.org/10.1186/1745-6215-12-101
- **Erratum:** Sandercock PAG, Niewada M, Członkowska A, et al. *Erratum
  to: The International Stroke Trial database.* Trials 2012;13:24.
  DOI: https://doi.org/10.1186/1745-6215-13-24
- **Primary trial report:** International Stroke Trial Collaborative Group.
  *The International Stroke Trial (IST): a randomised trial of aspirin,
  subcutaneous heparin, both, or neither among 19435 patients with acute
  ischaemic stroke.* Lancet 1997;349(9065):1569–1581.
  DOI: https://doi.org/10.1016/S0140-6736(97)04011-7

> Contains information from the **International Stroke Trial database
> (version 2)** (https://doi.org/10.7488/ds/104), made available under the
> **ODC Attribution License** (https://opendatacommons.org/licenses/by/1-0/).

---

## License

The database is licensed under the **Open Data Commons Attribution License
(ODC-By) v1.0**. The full license text as distributed by the original
depositor is included verbatim in [`LICENSE`](LICENSE); the depositor's
own notes are preserved in the `docs/` files (see below), unmodified.

Redistribution conditions honored here (ODC-By §4.2): this mirror is
conveyed only under ODC-By (a); the full license text and its URI are
included in the repository and referenced in this documentation (b); and
all notices shipped by the depositor are kept intact — nothing was
stripped (c). This mirror imposes no further restrictions.

**Scope of the license (ODC-By §2.4):** ODC-By governs rights in the
*database* (its structure and arrangement). Rights in the individual
records were cleared upstream: the data are **anonymised** patient records,
released for public use by the trial's own investigators via the Edinburgh
deposit. This mirror adds nothing to and removes nothing from that
clearance.

**No warranty.** The dataset is provided "as is" (ODC-By §7). This mirror
adds no warranty of any kind and asserts no claim over the data beyond
faithful, unmodified redistribution.

---

## Contents

Data (verbatim from the Edinburgh deposit; **not modified**):

| File | What it is |
|---|---|
| `data/IST_corrected.csv` | The trial dataset — corrected version incorporating the 2012 erratum. **This is the authoritative data file.** 19,435 patients, one row per randomised patient. |
| `LICENSE` | ODC-By v1.0, the depositor's own license file, verbatim. |

Documentation (verbatim; provenance and codebook):

| File | What it is |
|---|---|
| `docs/IST_variables.csv` | Variable dictionary (machine-readable) — column names, codes, meanings. |
| `docs/IST_variables.pdf` | Variable dictionary (human-readable). |
| `docs/IST_database_paper.pdf` | The Trials 2011 database paper. |
| `docs/IST_version_2_additional_commentary.pdf` | Depositor commentary on the version-2 corrections. |
| `docs/DataShare_curator_preservation_action_ISTv2.txt` | Edinburgh curator's preservation note. |

**On the two data files in the original deposit.** The Edinburgh deposit
contains both the original 2011 CSV and a later `IST_corrected.csv`. This
mirror pins the **corrected** version, as it is the authoritative current
form the depositors stand behind (per the 2012 erratum). If you need the
uncorrected original for exact reproduction of pre-erratum analyses,
retrieve it from the canonical source above.

---

## Integrity

The exact bytes of this snapshot are pinned by cryptographic hash. To
verify the data file matches the sealed record:

```
sha256sum data/IST_corrected.csv
```

The authoritative hash, dimensions, and provenance for this snapshot are
recorded in the seal `seals/SEAL-IST.md` in the `icebergsim-integrity`
repository, which references this mirror by commit and hash. If the hash
here does not match the seal, do not use this copy.

---

## Why this mirror exists

This snapshot is used as a **calibration template**: the joint structure of
its baseline covariates (a real Table 1 and its correlation structure)
informs a synthetic honest-trial generator. That downstream use estimates
statistical summaries from the data; it does not alter or redistribute the
records beyond this faithful mirror. The mirror is deliberately minimal,
verbatim, and frozen so that the provenance of everything built on top of
it is unambiguous and independently checkable.

This repository is part of the **IcebergSim** program
(https://icebergsim.com). It contains no analysis and no derived data —
only the pinned source dataset and its documentation.
