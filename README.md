# JSON - Freedom or Chaos: How to Trust Your Data

A conference presentation by Bart Dorlandt.

## Summary

Many teams end up with large, hand-crafted JSON files that grew organically over time — no schema, no contract, no way to know who depends on what. This talk follows a real-world journey of bringing structure and confidence to exactly that kind of "freedom data."

Starting from the constraints of an existing system that couldn't be replaced, the talk walks through a practical four-part approach using **pydantic** and **pytest**:

1. **Model the data** — iteratively build pydantic models that validate field types, formats, and allowed values, surfacing inconsistencies along the way.
2. **Validate in both directions** — parse the real data through the model, then regenerate it and diff the output to confirm nothing was missed.
3. **Keep the model honest** — use pytest to catch fields that are optional but always populated (should be required) or optional but never populated (should be removed).
4. **Go beyond single fields** — write pytest tests for cross-field dependencies, uniqueness constraints, and conditional logic that pydantic alone can't express.

The talk also covers the human side: resistance to change, cross-team challenges, and how to build trust incrementally by making validation a pipeline concern rather than a one-off effort.

## Tools

- [pydantic v2](https://docs.pydantic.dev/)
- [pytest](https://pytest.org/)
- [DeepDiff](https://github.com/seperman/deepdiff)

## Presented by

Bart Dorlandt — Freelance Network Automation Solution Architect

- https://linkedin.com/in/bartdorlandt/
- https://dreamnetworking.nl/