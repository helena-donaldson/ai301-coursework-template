# Unit 3 — Plan and Build

Path: `beat-1-sandbox/unit-3/plan-and-implement.md`

Record of your plan, the branch you built it on, and the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in the
repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the wrong
label is not graded.

---

## Posted upstream

**GitHub username**

[Your GitHub username, exactly as it appears on your profile - no @, no
profile URL. Your comment upstream is identified by this name, and it is
the only thing that ties it to you. Several students may plan the same
house issue, so this is what keeps their comments off your score and
yours off theirs.]

helena-donaldson

**Plan comment**

[Link to the comment where you posted your plan on the issue. Use the comment's own
permalink. **Then paste the text of that comment underneath the link** — the pasted text is
what this field is graded on, so copy across what you actually posted.]

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73#issuecomment-6027639491

# Candidate Plan

My plan for [#73](https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73#issue-5480324316), built on my reproduction above.

## Diagnosis

The file `core/config.py` uses the env variable OPENROUTER_API_KEY, and `README.md` and `docs/SETUP.md` describe how OPENROUTER_API_KEY is a needed part of the setup of the project, but `.env.example` lacks OPENROUTER_API_KEY.

## Scope

`.env.example` is the only file that will be changed. This issue does not require added functionality using the variable OPENROUTER_API_KEY, or documentation elsewhere, so it is appropriate to just make additions to `.env.example.

## Approach

Added the line `OPENROUTER_API_KEY=sk-or-v1-your-openrouter-key-here` to `.env.example`, next to the other AI related environment variables since `docs/SETUP.md` described it being a needed part to enable certain AI functionality.

Also added a small comment to `.env.example` to ensure users of the project know the purpose of the env variable.

## Test Plan
Ran `cp .env.example .env` to ensure that the resulting `.env` file now has the previously missing env variable OPENROUTER_API_KEY.

## Limitations
As the scope of this issue focused on a environment variable addition, not ensuring that features involved with the environment variable worked, I did not focus on ensuring all features related to the environment variable, beyond its addition to the `.env.example` file, worked.

---

# LLM provider
# Options: "mock" (default, no API key needed), "openai", "openrouter"
LLM_PROVIDER=mock
OPENAI_API_KEY=sk-your-key-here
OPENROUTER_API_KEY=sk-or-v1-your-openrouter-key-here

## Your branch

**Branch**

[The name of the branch you built the change on, exactly as it appears in your fork. The
naming shape is a type prefix, then the issue number, then a short description. **The issue
number in the branch name must be the number of the issue you claimed** — a name carrying
any other number does not satisfy this field.]

fix/73-env-var-addition

**Evidence**

[Your Unit 2 reproduction steps re-run against the built change: the before, then the
after. Paste both, including the commands you ran and their output.]

Note: My reproduction steps also included repo setup steps. Since that has already been done with no excepted difference, I will omit that description.

Before, I ran the command `cp .env.example .env`, and the resulting environment file, with its relevant snippet, looked like this:

```
# LLM provider
# Options: "mock" (default, no API key needed), "openai"
LLM_PROVIDER=mock
OPENAI_API_KEY=sk-your-key-here
```

After I made the change, I ran `cp .env.example .env` and the new environment variable looked like this:

```
# LLM provider
# Options: "mock" (default, no API key needed), "openai", "openrouter"
LLM_PROVIDER=mock
OPENAI_API_KEY=sk-your-key-here
OPENROUTER_API_KEY=sk-or-v1-your-openrouter-key-here
```

Since it now has the OPENROUTER_API_KEY with a placeholder value, the issue of it being missing has been resolved.

## Eval iterations

Answer all four sections. Quote source text directly; paraphrase does not satisfy these
fields.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

categories: clear-accept 7/7  scope-creep 4/4  thread-convention 2/2  unbuildable 3/3  wrong-cause 4/4
agreement: 20/20 scored items  (bar: 18/20: PASS)


**Package analysis**

[Pick one scored package (`pkg-01` through `pkg-20` — the four `calib-` packages are never
scored). Name it by id, say what your rubric decided and what the gold label said, and
explain why your rubric read it that way.]

The id is pkg-20.
My rubric rejected it, and the golden label also rejected it.
My rubric likely agreed with the golden label because my rubric required AI usage be disclosed should it be the repository's contribution policy, and this package failed to disclose.

**Check rationale**

[Quote one check from the `rubric.md` you uploaded to `tools/plan-check/`, exactly as it reads now.
Then say why it reads that way — what you revised to get there, or what you rejected in
favour of it.]

Check: | scope creep | Scope and files and diagnosis of candidate plan | The scope of changes and the files to be changed must be limited to what the diagnosis describes is relevant | required |

It reads this way because I wanted to ensure the number of files being edited would be limited to the scope of the change. I considered also requiring the files that would be changed would make sense given the description of the bug in the issue, but since I already had another check that looked to see if the change proposed made sense with the description of the bug, so I did not add that to this check.

**Trade-offs**

[Every check gives something up. Any one of these is a complete answer: a package whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

A case that I accept it might miss is if there is a conventioning in contributing other than disclosing AI usage. I only check to see if AI usage is required, but there could be any number of conventions both in the official repo contribution policy or described in the issue thread. However, I feel like this kind of check might just end up being too convoluted.

---

Related paths: `plan.md` and `eval-run.txt` in this directory; your skill's files in
`tools/plan-check/`.
