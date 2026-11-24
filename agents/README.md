# Organization Agents

This directory contains approved GitHub Copilot agents published for contributors to the robe-land organization.

Canonical agent definitions, original candidate sources, evaluation evidence, and adoption status are maintained in robe-engineering.

Only adopted agents may be published here. Published definitions are distribution artifacts, not independently maintained implementations.

Changes to published agents must originate from the approved canonical implementation in Engineering.

## Publication review and verification

Each publication pull request must identify the approved canonical Engineering
revision and verify that the published profile matches it. Reviewers verify
the resource's display name and tool access, applicable license and
attribution, resource-qualified version tag, and publication catalog entry.
The `publication-verify` check validates lifecycle JSON syntax and checks the
pull request diff for whitespace errors; it does not validate resource
content or license compatibility.

## Shared lifecycle

This repository uses the shared `eng-lifecycle` workflow with `main` as its
base, `publication-verify` as a required check, and a required approving
GitHub review. Lifecycle approval and GitHub review are independent
requirements. This configuration does not itself enable GitHub branch
protection or rulesets; repository administrators must enforce the required
check and review on `main` to protect against changes outside the lifecycle
tool.

The lifecycle bootstrap branch was created manually as a one-time exception
because `eng-lifecycle start` requires `.github/lifecycle.json` to exist.
After this bootstrap is integrated, all work must start with
`eng-lifecycle start --repo .`; this exception does not authorize manual
branching or lifecycle bypass for later publication work.
