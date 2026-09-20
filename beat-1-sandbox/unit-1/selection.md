# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

[The individual Path Review issue page. A link to the repository or the issue list
does not satisfy this field.]

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
paste the output here, including the closing JSON block
```

2. #73 — README and .env.example disagree about which LLM API key to set — ACCEPT
- Same six grades, all pass; body names the mismatch and both files.
- Fit: clean and safe, but docs-only reconciliation — it exercises the PR workflow rather than any code skill you have.

Tie on preferred checks (1/1 each), so the fit profile broke the ordering; it did not change either verdict.

[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/72",
    "checks": [
      {"name": "active-work", "grade": "pass", "evidence": "GitHub API repo object: \"archived\": false"},
      {"name": "contibution", "grade": "pass", "evidence": "docs/CONTRIBUTING.md is the only policy doc; no AI-use restriction in it, no AI_POLICY.md, PR template requires only green CI"},
      {"name": "no-assignee", "grade": "pass", "evidence": "issue #72 assignees: [] (empty)"},
      {"name": "no-prs", "grade": "pass", "evidence": "repo has 0 pull requests (state=all); #72 timeline shows no cross-referenced PR, only a commit reference from a classmate's fork rafiatasafi/ai301-coursework"},
      {"name": "clear-scope-closure-requirements", "grade": "pass", "evidence": "body: \"Verification against a malformed hash should fail closed (return False), not raise\" plus relevant files and xfail-marker removal step"},
      {"name": "commits-recent", "grade": "pass", "evidence": "last default-branch commit 2026-09-16T21:42:18Z, within the last year"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73",
    "checks": [
      {"name": "active-work", "grade": "pass", "evidence": "GitHub API repo object: \"archived\": false"},
      {"name": "contibution", "grade": "pass", "evidence": "docs/CONTRIBUTING.md contains no AI-use ban; no AI_POLICY.md in repo root or .github/"},
      {"name": "no-assignee", "grade": "pass", "evidence": "issue #73 assignees: [] (empty)"},
      {"name": "no-prs", "grade": "pass", "evidence": "repo has 0 pull requests (state=all); #73 timeline contains only 4 'labeled' events"},
      {"name": "clear-scope-closure-requirements", "grade": "pass", "evidence": "body: \"README.md tells you to add OPENROUTER_API_KEY ... Make the two files agree\" with both relevant files listed"},
      {"name": "commits-recent", "grade": "pass", "evidence": "last default-branch commit 2026-09-16T21:42:18Z, within the last year"}
    ],
    "verdict": "accept"
  }
]

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

categories: claimed 4/4  clear-accept 8/8  dead-repo 3/3  policy 1/1  scope 2/4
agreement: 18/20 scored items  (bar: 18/20: PASS)

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

issue-20

My rubric passed it while the gold label failed it.

Golden Label: {"id": "issue-20", "source": "excalidraw/excalidraw#11811", "category": "scope", "calibration": false, "verdict": "reject", "note": "one-line feature wish with no spec and a product decision hiding inside"}

I believe my rubric passed it instead of failing it like the golden label because my check on scope only specifies that a problem/request is present, instead of examining the exact detail of the issue description.

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

| no-prs| In repo facts block, in linked prs attribute | There should be no linked PRs that are not closed present | required |

Reasoning: I created this to ensure that no one was already contributing to the issue. I specified that closed PRs are ok because that suggests that the issue's work is not already completed. I put it as required because I don't want to start work on an issue that will be closed soon due to current work.

**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

The check might give up an edge case where the PR that is not closed has poor work quality (for example, it might have comments from the maintainer that say significant changes are requested). My check would fail to capture that.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

[Answer all three:

1. The issue's fit to your interests and to the time available.
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
3. The anticipated difficulty in claiming it.]

The issue doesn't fit well to my interested, because I am interested in C/C++ work, but that is to be expected because the repo doesn't use those languages. It wouldn't fit well to my time available because I have a lot of time available to work on the issue, but the issue itself would likely last just an hour or two. The verdict correctly identified that it was unclaimed, that a problem was identified (in scope), and that the maintainer is active due to recent commits. I think the rubric captured everything I wanted it to capture fairly accurately. I think it will be difficult to claim it because the issue is fairly easy, so many people might try to claim it due to low bar of entry.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
