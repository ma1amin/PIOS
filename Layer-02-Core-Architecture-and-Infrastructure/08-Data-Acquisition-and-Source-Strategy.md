# Data Acquisition and Source Strategy

## Principle
PIOS only acquires and processes data through lawful, permitted, documented mechanisms. Technical ability to retrieve data does not constitute permission to ingest, reproduce, store, or commercially use it.

## Source Classes
- Licensed commercial APIs.
- Official business feeds.
- Mapping/location providers.
- Public/open datasets with compatible licenses.
- Partner datasets.
- Business-submitted data.
- User/community contributions.
- Government/open-data sources where terms allow intended use.

## Source Registry
Every source must have a registry record containing:
- Source owner.
- Source type.
- Legal/contractual basis.
- Integration method.
- Permitted fields.
- Display rights.
- Storage rights.
- Attribution requirements.
- Refresh constraints.
- Rate limits.
- Geographic coverage.
- Reliability classification.
- Data owner.
- Technical owner.
- Suspension procedure.

## Acquisition Agent
The acquisition agent may:
- Retrieve data from approved endpoints.
- Validate transport and schema.
- Store permitted raw references.
- Attach provenance.
- Detect source failures.
- Respect quotas.
- Enqueue normalization.

It may not:
- Invent missing fields.
- Circumvent access controls.
- Ignore contractual restrictions.
- Rank places.
- Treat provider content as system instructions.

## Freshness
Refresh policies are field-specific. Opening hours may require more frequent validation than a stable address. Ratings may change frequently. Business ownership may change rarely but has high correctness impact.

Each published field should expose an internal freshness state:
- Current.
- Aging.
- Stale.
- Unknown.

## Failure Handling
When a source fails:
- Record the failure.
- Preserve last permitted known value with freshness status.
- Do not silently represent stale data as current.
- Avoid cascading platform failure.
- Retry according to policy.
- Escalate prolonged degradation.

## Multi-Source Conflict
Conflicting values are not resolved by arbitrary overwrite order. Resolution considers source authority, freshness, corroboration, field type, and verified business/user correction processes. Material conflicts remain visible internally for review.
