# Evidence guide: where proof lives in a reproduction package

<!--
THIS IS THE PART YOU WRITE (new this week: Unit 1 handed you this file
finished; the scaffolding fades). The skill uses this guide as its map:
for every kind of proof a rubric check names, this file says WHERE to
find it in a package and WHAT GOOD LOOKS LIKE when you do.

Under each family heading below, write:

- Where it lives: the exact places to look. In an eval bundle (which
  section of the package: the issue context, the repo-facts block, the
  claim comment, the repro report and its parts). In live mode (where
  on GitHub or in the draft: the issue thread, the repo's docs, the
  student's draft comment).
- What good looks like: one or two sentences someone else could apply.
  Prefer observable conditions ("the versions named match what the
  issue targets, or the difference is called out") over adjectives
  ("environment is thorough").

A rubric check whose evidence this guide cannot locate is a check
nobody else can execute; the rubric swap showed you what that feels
like. Write the map you wish your grader had.
-->

## Environment

<!-- Where the environment record lives, and what a sufficient one
looks like against the issue's stated target. -->

Should be located in the claim_comment_markdown, and should describe  tool version, OS used.
It should also match with the environment described in the body_markdown of the issue attribute.

## Steps

<!-- Where the reproduction steps live, and what makes them followable
by a stranger, starting state to trigger. -->

Should be within the within claim_comment_markdown and in the body_markdown of the issue attribute.
It should include steps taken to achieve actual output, must be in enough detail to be reproducible and must match with the steps described to reproduce the bug in the issue description.

## Behavior shown

<!-- Where the artifacts live (output excerpts, logs, screenshots),
and what it means for an artifact to show the issue's behavior rather
than an adjacent one. -->

It should be within claim_comment_markdown and in the body_markdown of the issue attribute. The actual result, with an artifact like an error log, should match the expected result described in the issue description or the claim describes that they were unable to reproduce the bug.

## Honesty

<!-- Where claims and their backing meet: how to tell a report that
says exactly what happened (including an honest cannot-reproduce) from
one that claims more than its evidence shows. -->

It should be within claim_comment_markdown. Claims of being able to reproduce something must be backed by specific evidence.

## Comms

<!-- Where the words meet the repo: the claim comment against the
issue, the comments against the repo's stated templates and
contribution policy (including AI-use disclosure requirements), and
what specific-and-honest looks like next to boilerplate. -->

It should be within the repo_facts raw_markdown and claim_comment_markdown.
If the repo policies require AI usage to be disclosed, the claim must in some way describe AI usage (the asusmption is that every claim should be utilizing AI in some way).
