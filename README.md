Decision 1: Include company_id in JWT

Chosen: YES - include in token payload
Rationale: Performance (eliminates DB lookup per request) + makes company context explicit & tamper-evident
Trade-off: Requires token refresh if user switches companies (acceptable - rare operation)
Decision 2: Denormalize company_id to child tables

Chosen: YES - add to PayrollItem, PTOBala
