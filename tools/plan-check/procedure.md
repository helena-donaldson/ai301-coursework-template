# Procedure: how this skill grades a plan package

<!--
THIS IS THE PART YOU WRITE, and it is a new kind of part. Weeks 1 and
2, SKILL.md carried a numbered workflow and you only wrote judgment
files. This week the workflow is gone from the frame: SKILL.md says
"execute procedure.md", and these are the operating steps you author.
The machinery is in your hands now.

Your operator swap is the design brief. When your executor stalled
because your rubric said WHAT to decide but not HOW to find the
evidence, that was a procedure gap. This file is where those gaps get
closed: a complete procedure lets someone who has never seen a plan
package before (a groupmate, or the skill itself) grade one exactly the
way you would.

Under each stage heading below, write the concrete steps for that
stage. The one-line note under each heading says what a complete
procedure must decide there. Write steps, not intentions: "read the
repro evidence before the plan, and note what behavior it pins down"
is a step; "understand the context" is a wish.
-->

## Read order

<!-- What gets read, in what order, before any check is graded, and
what to note down from each part while reading. A complete procedure
decides the order (issue first? repro evidence first?) and says why
the order matters for the checks that come later. -->

| diagnosis vs evidence | Diagnosis in candidate plan and issue description and repo evidence | The problem or bug being described in the issue must make sense with what the reproduction described and what the diagnosis also labeled as the cause of the issue | required |
| scope creep | Scope and files and diagnosis of candidate plan | The scope of changes and the files to be changed must be limited to what the diagnosis describes is relevant | required |
| test | Test plan under candidate plan and diagnosis | The diagnosis of the issue must be shown to be meaningfully tested and solved with the test plan | required |
| AI Use | Repo facts under contribution policy as well as the plan/reproduction section | If the repo requires AI usage to be disclosed, AI use must be disclosed in the plan and/or reproduction sections | required |

First read the repo facts, in the contribution policy. Then read the body of the issue description. Next overview the reproduction of the issue, and thden the diagnosis. Finally review the scope and the files that will be changed in the candidate plan. 

## Evidence gathering

<!-- For each evidence family your rubric's checks name, the concrete
gathering move: which part of the package (or, live, which page or
thread location per your evidence guide) to pull the fact from, and
what to record. A complete procedure leaves no check whose evidence an
executor would have to hunt for. -->

For the repo facts, in the contribution policy, note if AI usage should be disclosed. For the body of the issue description, note the described issue, and then when reading the reproduction of the issue and the diagnosis, ensure that the diagnosis and reproduction make sense with the original described issue. The scope and the files being changed should be limited to what the diagnosis says the issue is.

## Check execution

<!-- How one check runs against gathered evidence: in what order the
checks execute, what an executor does when evidence for a check is
genuinely absent, and when a check may be graded without re-reading
the whole package. A complete procedure makes two executors grade the
same package the same way. -->

For the repo facts, in the contribution policy, note if AI usage should be disclosed. For the body of the issue description, note the described issue, and then when reading the reproduction of the issue and the diagnosis, ensure that the diagnosis and reproduction make sense with the original described issue. The scope and the files being changed should be limited to what the diagnosis says the issue is.
If evidence for a check is absent, fail the check.

## Verdict assembly

<!-- How the per-check grades become the final accept or reject:
apply your rubric's verdict rule, state how unclear grades enter it,
and say what gets quoted in the output for the deciding check. A
complete procedure produces the same verdict from the same grades,
every time. -->

Reject if at least one check fails, accept if all checks pass. If it is uncertain whether a check passes or fails (the evidence for the check is not there), default to failing it.
