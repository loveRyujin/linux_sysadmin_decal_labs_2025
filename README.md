# linux_sysadmin_decal_labs — Spring 2025

## Overview
This repository collects my solutions for the **linux_sysadmin_decal** Spring 2025 offering. Each lab folder mirrors the structure distributed by the course staff and contains the scripts, configuration fragments, and written responses necessary for submission.

## Requirements
- Linux environment with a POSIX-compliant shell (`bash` 5.x recommended).
- Standard GNU utilities (`coreutils`, `grep`, `sed`, `awk`).
- Optional: `shellcheck` for linting shell scripts before submission.

## Repository Map
| Path | Purpose | Highlights |
| --- | --- | --- |
| `lab1/` | Introduction to basic tooling and file operations. | `answers.md`, supporting scripts in `b01/`. |
| `lab2/` | Phonebook management scripts and written analysis. | `answers.md`, runnable scripts in `phonebook/`, helper data in `bash_phonebook_entries/`. |

Future labs will follow the same template: a dedicated directory containing the exercise assets alongside an `answers.md` (or equivalent) documenting the reasoning behind each task.

## Getting Started
1. Clone this repository and move into it: `git clone … && cd linux_sysadmin_decal_labs`.
2. Pick a lab directory, e.g. `cd lab2`.
3. Review `answers.md` to understand the narrative solution.
4. Execute scripts from within their lab directory so relative paths resolve as expected. Most scripts include inline notes about expected inputs or configuration.

## Verifying Work
- Run `shellcheck` on any updated shell scripts prior to submission: `shellcheck ./phonebook/*.sh`.
- Manually test scripts against the sample data shipped in each lab (e.g. `./phonebook/phonebook.sh --help`).
- Keep instructor-provided test harnesses in sync with these solutions when they become available.

## Notes & Academic Honesty
- These solutions reflect my personal understanding and are subject to revision as the course evolves.
- Use them for reference and comparison only; always comply with the course's academic honesty guidelines when collaborating or submitting work.

Happy sysadmin-ing!
