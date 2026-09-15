# API and Service Contracts

## API Principles
- Versioned paths.
- Explicit request/response schemas.
- Authentication where required.
- Resource-level authorization.
- Idempotency for retryable mutations.
- Pagination.
- Rate limiting.
- Correlation IDs.
- Stable machine-readable error codes.
- No internal stack traces in public responses.

## Representative Endpoints
- `GET /api/v1/search`
- `GET /api/v1/places/{placeId}`
- `GET /api/v1/places/{placeId}/ratings`
- `GET /api/v1/places/{placeId}/insights`
- `GET /api/v1/places/{placeId}/trust`
- `POST /api/v1/feedback`
- `POST /api/v1/contributions`
- `POST /api/v1/places/{placeId}/claim`
- `GET /api/v1/categories`
- `GET /api/v1/locations`

## Search Request
Typical parameters:
- `q`
- `lat`
- `lon`
- `city`
- `district`
- `category`
- `radius_m`
- filters
- sort
- language
- cursor/page

Precise coordinates must not be logged unnecessarily.

## Search Response
A result may include:
- `place_id`
- localized display name
- category
- location summary
- distance
- source rating summaries
- trust state
- key attributes
- recommendation reason
- freshness
- sponsorship state

## Errors
Use structured responses:
- `code`
- `message`
- `correlation_id`
- safe details

Examples:
- `VALIDATION_ERROR`
- `UNAUTHORIZED`
- `FORBIDDEN`
- `PLACE_NOT_FOUND`
- `RATE_LIMITED`
- `SOURCE_TEMPORARILY_UNAVAILABLE`

## Internal Contracts
Service-to-service contracts should use generated schemas/OpenAPI, event schemas, or strongly typed shared contracts with careful versioning. Avoid shared database tables as an integration mechanism.
