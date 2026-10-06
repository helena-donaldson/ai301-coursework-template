Replace this file with your unit-3 plan: the same `plan.md` your
plan-check run graded.

Keep the deviations heading below, and fill it before you submit. It is
graded on being answered, not on there being deviations to report.


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


## Deviations

[What changed between the plan you posted and the change you built, and
why. If nothing changed, say so in your own words - "nothing changed;
the plan held" earns these points in full. Leaving this blank does not.]

Nothing changed- this was just a simple environment variable addition, with a bit of extra documentation.
