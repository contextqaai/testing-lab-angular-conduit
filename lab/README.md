# ContextQA learning lab: Angular Conduit

This is a public educational fork of [realworld-apps/angular-realworld-example-app](https://github.com/realworld-apps/angular-realworld-example-app). Original source, history, licenses and attribution are retained. It is not a customer production application.

## Status

Source is available. Hosted full-stack sessions and ContextQA reports are not yet verified for this track. The exercises below are a test-design guide, not a passing test report. Upstream starting commit: `dd99ed2cf39c805d719f943c5d7061a5683d98a8`.

## Run locally

Follow the upstream Bun setup command, including its realworld submodule. Host your own backend. Pin the submodule version and inspect its license before deployment. Do not load-test shared upstream demo services.

See the [upstream setup guide](../README.md#upstream-project-documentation) for the project's original instructions.

## Exercises

| Scenario | Required assertion |
|---|---|
| Authentication | A new synthetic user can sign up and sign in; invalid credentials are rejected. |
| Article creation | The published title and body match the entered values. |
| Article ownership | Only the author can modify their article. |
| Comment and favorite | The comment persists after reload and the favorite appears on the profile. |
| Pagination | Known fixture articles appear on the correct pages without duplication. |

## Reproduce the end-to-end workflow

1. Start your own local or hosted copy with synthetic fixtures. ContextQA's cloud runner needs a reachable address; localhost needs a separately supported connection.
2. Choose one scenario and write explicit expected results before generating the test.
3. Follow [ContextQA's getting-started guide](https://contextqa.com/tutorials/getting-started-with-contextqa-test-automation/) or the [MCP documentation](https://mcp.contextqa.com/docs/faq) using your own authenticated workspace.
4. Create/review the test steps, execute, and inspect the actual assertion and runner verdict.
5. Introduce one disclosed regression in a separate local branch. Repeat the same test, observe failure, fix the application and rerun.
6. Record the app commit, fixture/scenario version, browser, tool version, timestamp, step counts and evidence. Do not describe a recording as a fresh run.
7. Repeat on a URL you own or have permission to test. Use synthetic data and confirm actions that submit or alter records.

## Reports and limitations

No ContextQA report is included yet. Add only actual execution evidence. Public reports must contain synthetic data and explicit provenance. Private target results must stay private. Upstream tests remain upstream tests; they are not proof of a ContextQA run.

Recorded reports can be reused for the exact pinned fixture and version. Live runs need fresh isolated state and quotas. Code export, CI integration, automatic resets and embedded execution should be demonstrated only after independently verified.

## Teaching brief

Show the app, source and assertion; create and run the test; inspect evidence; reproduce a regression; show the fix; then test an authorized app of your own. Keep setup and execution time separate. Link the exact release and acknowledge upstream creators. Creator sponsorships should be disclosed.
