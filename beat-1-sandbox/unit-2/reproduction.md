# Unit 2 — Claim and Reproduce

Path: `beat-1-sandbox/unit-2/reproduction.md`

Record of your claim and reproduction on the issue you chose in Unit 1, and of the
evaluation runs that produced `eval-run.txt`. This file is graded at the path above; a copy
kept anywhere else in the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the wrong
label is not graded.

---

## Your identity upstream

**GitHub username**

[Your GitHub username, exactly as it appears on your profile — no `@`, no profile URL. Your
comments upstream are identified by this name.]

helena-donaldson

---

## Posted upstream

**Claim comment**

[Link to the comment where you claimed the issue. Use the comment's own permalink, not the
issue page on its own. **Then paste the text of that comment underneath the link** — the
pasted text is what this field is graded on, so copy across what you actually posted.]

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73#issuecomment-5862102869

Hi- first time contributor, I'd like to work #73. I will follow the repo's setup instructions and examine the differences in environment variable configuration descriptions, specifically with how `.env.example` differs from `README.md` with the  OPENROUTER_API_KEY variable. I will report back on my environment used, steps to reproduce, and the actual outcome.

**Reproduction comment**

[Link to the comment where you posted your reproduction. It must record the environment
(OS, relevant versions, code state), steps a stranger could follow, and what you observed.
**Then paste the text of that comment underneath the link** — the pasted text is what this
field is graded on, so copy across what you actually posted.]

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73#issuecomment-5862162562s

## Reproduction Report — Issue #73

## Environment

My OS is Windows 11. I checked out the Pathreview repository at commit `2f4e82f52efbcfcc57d65b3fa5348672163ca088`, not making any local changes.

## Steps

1. Forked the repository.
2. Cloned the reppository.
3. Changed directories into the repository.
4. Followed the README's step related to the enviroment setup (ran `cp .env.example .env`)
5. Noted the README's description of the needed environment addition `add your OPENROUTER_API_KEY to .env`.
6. Searched for mentions of `OPENROUTER_API_KEY` in the project using my IDE's search features.
7. Found another mention of `OPENROUTER_API_KEY` in `SETUP.md` where it says `# Edit .env and set your OPENROUTER_API_KEY (required for AI features)`
8. Opened `.env.example` where the only AI related env variables mentioned are the following `# LLM provider # Options: "mock" (default, no API key needed), "openai" LLM_PROVIDER=mock OPENAI_API_KEY=sk-your-key-here`.

## Expected Behavior

My `.env` file, as a result of the cp step, should have needed environmental variables listed, including a note on `OPENROUTER_API_KEY`.

## Actual Behavior

Since the current `.env.example` does not list `OPENROUTER_API_KEY`, my `.env` file now only has the following env variables related to the AI features: `# LLM provider # Options: "mock" (default, no API key needed), "openai" LLM_PROVIDER=mock OPENAI_API_KEY=sk-your-key-here`.

## Result

There is a demonstrated mismatch between the `README.md` and `.env.example` that will cause issues when setting up `.env`.

## Eval iterations

Answer all four sections. Quote source text directly; paraphrase does not satisfy these
fields.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

categories: clear-accept 8/8  disclosure 1/1  no-evidence 4/4  unfollowable-comms 2/3  wrong-target 3/4
agreement: 18/20 scored items  (bar: 18/20: PASS)

**Package analysis**

[Pick one scored package (`pkg-01` through `pkg-20` — the four `calib-` packages are never
scored). Name it by id, say what your rubric decided and what the gold label said, and
explain why your rubric read it that way.]

id: pkg-10
rubric: accept
gold-label: accept
rubric explanation: The claim described the environment with specific versioning details, with the steps matched and were reproducible, the claimer was unable to reproduce the issue but stated that clearly with description of the actual results they did get.

**Check rationale**

[Quote one check from the `rubric.md` you uploaded to `tools/repro-check/`, exactly as it reads now.
Then say why it reads that way — what you revised to get there, or what you rejected in
favour of it.]

Steps| within claim_comment_markdown and in the body_markdown of the issue attribute | Includes steps taken to achieve actual output, must be in enough detail to be reproducible and must match with the steps described to reproduce the bug in the issue description | Required

This check reads this way because I want to ensure that the claimer followed the steps detailed in the description so that reproduction of te bug actually occurred. There is a tradeoff because the AI might misinterpret this to mean that a step difference that isn't actually a meaningful difference might cause it to reject the claim.

**Trade-offs**

[Every check gives something up. Any one of these is a complete answer: a package whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

For the AI contribution check, I included the specification to assume every claim should use some element of AI. I made this assumption because it was stated in the assignment description/golden validation, but it does constrict my tool to only be useful in the AI claim context.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/repro-check/`.
