# ADR 0000: Step conclusion

**Date**: 2020-01-13

**Status**: Accepted

## Context

This ADR proposes adding `steps.<id>.conclusion` to the steps context.

Reminder, currently the steps contains `steps.<id>.outputs`.

## Decision

For steps that have completed, populate `steps.<id>.conclusion` with one of the following values:

- `success`
- `failure`
- `cancelled`
- `skipped`

## Consequences

- Update runner
- Update [docs](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/contexts-and-expression-syntax-for-github-actions#steps-context)