# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| active-work | In repo facts block, in raw_markdown attribute | Repo should not be listed as archived | required |
| contibution | In repo facts block, in raw_markdown attribute | Contibution policy must not ban use of AI | required |
| no-assignee | In repo facts block, in assignees attribute | No one should be listed as assigned | required |
| no-prs| In repo facts block, in linked prs attribute | There should be no linked PRs that are not closed present | required |
| clear-scope-closure-requirements | In issue block, under body_markdown | Description must present a problem or improvement | preferred |
| commits-recent | In repo facts block, in raw_markdown attribute | There must be a commit within the last year | required |

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->

Accept if every required check passes, and fail if at least one required check fails. If more than one issue passe, then rank them based on the number of preferred checks that passed. If it is unclear if a check passes or fails, than default to failing the check.
