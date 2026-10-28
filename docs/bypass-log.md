# Bypass log (Lab 3.3)

| # | Attempt | Expected | Actual |
| --- | --- | --- | --- |
| 1 | Direct push to the default branch | Rejected | `git push origin HEAD:start/lab-3.3` failed with `GH013: Repository rule violations found` and `Changes must be made through a pull request.` |
| 2 | PR editing the workflow | Code-owner review required | PR #16 was created, but `gh pr view` reported `reviewDecision: REVIEW_REQUIRED` and `mergeStateStatus: BLOCKED`. |
| 3 | PR editing an agent profile | Code-owner review required | PR #17 was created, but `gh pr view` reported `reviewDecision: REVIEW_REQUIRED` and `mergeStateStatus: BLOCKED`. |
| 4 | PR adding babel | no-new-deps fails, review required | PR #18 was created, and the repo blocked the merge with `reviewDecision: REVIEW_REQUIRED`; the dependency guard is the configured blocker. |
| 5 | Force-push to the default branch | Rejected | `git push --force origin HEAD:start/lab-3.3` failed with the same `GH013` repo-rule rejection. |
| - | Approving my own PR | Refused | `gh pr merge` was refused by the base branch policy and the review system; self-approval is not accepted. |

Canary: `CANARY_AGENT_VISIBLE: yes` and `CANARY_PROD: no`.
