# Programmable Workflow Engine

## Short Description
A REST API that executes user-defined sequences of conditional logic and data processing tasks based on a structured JSON instruction set.

## Functional Requirements
- Workflow Definition: Create a multi-step "plan" that includes a sequence of actions.
- Execution Engine: A background process that parses the plan, maintains the current state, and executes steps in order.
- Conditional Branching: The ability to skip or run specific steps based on the output of a previous step.
- Error Handling & Retries: Automatically retry a failed step up to 3 times before marking the entire workflow as "Failed."
- Status Monitoring: Retrieve the real-time status of a running workflow, showing which steps are completed, running, or failed.
- Variable Passing: The output of Step A must be accessible as the input for Step B.

## Examples

### A JSON input and an outcome
```json
{
  "workflow_id": "data-processor-01",
  "steps": [
    { "id": 1, "action": "TRANSFORM", "params": { "op": "multiply", "factor": 10 }, "input": 5 },
    { "id": 2, "action": "CONDITION", "params": { "greater_than": 40 }, "on_true": 3, "on_false": 4 },
    { "id": 3, "action": "LOG", "params": { "message": "High value detected" } },
    { "id": 4, "action": "STOP", "params": { "message": "Process complete" } }
  ]
}
```

Desired Outcome:

- Step 1 calculates `5 * 10 = 50`.
- Step 2 evaluates if `50 > 40`. Since it's `true`, it routes to Step 3.
- Step 3 writes "High value detected" to the server console/database.
- The API returns a `202 Accepted` initially, and a subsequent `GET /status/data-processor-01` returns a history log showing: `Step 1: Success (50) -> Step 2: Success (True) -> Step 3: Success.`