# ADR 0274: Step conclusion

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

### Terminology aligns with runs API

The term `conclusion` aligns with the runs API.

The following is a snippet from the runs API response payload:

```json
      "steps": [
        {
          "name": "Set up job",
          "status": "completed",
          "conclusion": "success",
          "number": 1,
          "started_at": "2020-01-09T11:06:16.000-05:00",
          "completed_at": "2020-01-09T11:06:18.000-05:00"
        },
```

## Consequences

- Update runner
- Update [docs](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/contexts-and-expression-syntax-for-github-actions#steps-context)