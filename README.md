# ITGC Assessment: ERP General Controls Review

A worked IT General Controls (ITGC) assessment of a finance ERP, built as a hands-on exercise to learn the IT audit workflow end to end: scoping, control design, testing, findings and remediation tracking.

> **Note on scope.** This is a self-directed learning project. The company (Meridian Group plc) and its results are illustrative, not a real engagement. The control framework, test procedures and findings logic are realistic and reusable.

## What this is

ITGCs are the controls that let an auditor trust that a financial system behaves as intended. They sit under the four standard domains:

| Domain | Question it answers |
|---|---|
| **A. Access to Programs & Data** | Who can get into the system and data, and what can they do once in? |
| **B. Program Changes** | How are changes to the live system requested, tested, approved and released? |
| **C. Program Development** | How are new systems and major enhancements built and brought live? |
| **D. Computer Operations** | How is the system run day to day: jobs, backups, incidents, recovery? |

The assessment covers **32 controls** across these domains, each tested against a documented procedure and sample, with results rolled up into an opinion.

## Framework basis

Controls are mapped to **COBIT 2019** and **NIST SP 800-53**, following the control structure commonly used in SOX ITGC work.

## The workbook

`ITGC_Assessment_Meridian_ERP.xlsx` has five tabs:

- **Overview** - engagement scope, period, framework and overall opinion.
- **Control Matrix** - the working paper: 32 controls with objective, risk, owner, control type, test procedure, sample, result and rating.
- **Findings Register** - 10 exceptions written up as deficiencies with root cause, recommendation, owner and target date.
- **Dashboard** - live roll-up (COUNTIF/COUNTIFS) of results and ratings by domain; recalculates when the matrix changes.
- **Legend** - rating scales and definitions.

## Headline results

| Metric | Value |
|---|---|
| Controls tested | 32 |
| Effective | 22 |
| Partially effective | 7 |
| Ineffective | 3 |
| High-rated deficiencies | 3 |
| Overall opinion | Partially effective |

The three high-rated findings are the ones that would block audit reliance before year-end:

1. **Excessive privileged access** (AC-04) - 8 admin accounts against 5 approved, register 14 months stale.
2. **Broken build/release segregation** (CM-04) - developers retain production deploy rights.
3. **Unmitigated segregation-of-duties conflicts** (AC-06) - users able to both create and approve payments with no monitoring.

Each is logged in the Findings Register with a root cause and a remediation owner and date.

## What I took from it

- How an ITGC control is actually structured: objective, risk, control activity, test procedure, result.
- The difference between a design gap and an operating failure, and why that changes the rating.
- Why privileged access, change segregation and SoD are where most real findings land.
- How to turn raw exceptions into a findings register that a control owner can act on.

## Reusing it as a template

Keep columns A to I of the Control Matrix, clear the results from column J onwards, and run your own testing. The Dashboard follows automatically.

---

**Rohan Khatri** - BSc Computer Science (Cyber Security), Oxford Brookes
[GitHub](https://github.com/krovix-1902) · [LinkedIn](https://linkedin.com/in/rohan-khatri18) · [krovix.in](https://krovix.in)
