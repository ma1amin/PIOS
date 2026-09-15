# Review Intelligence

## Purpose
Review intelligence converts permitted review evidence into structured insights without replacing the underlying evidence or inventing consensus.

## Capabilities
- Overall sentiment.
- Aspect-level sentiment.
- Recurring topics.
- Positive themes.
- Negative themes.
- Trend changes.
- Volume changes.
- Emerging issues.
- Comparison across time periods.
- Language-aware analysis.

## Example Aspects
General:
- Service quality.
- Staff behavior.
- Waiting time.
- Cleanliness.
- Price/value.
- Reliability.
- Accessibility.

Category-specific:
- Healthcare: appointment handling, communication, facility experience.
- Food: food quality, speed, atmosphere, consistency.
- Automotive: diagnostic quality, turnaround, transparency, workmanship.
- Retail: product availability, warranty, after-sales support.

## Language
Arabic and English should be processed natively where models meet evaluation standards. Translation can support cross-language aggregation but should not replace original-language evidence.

## Evidence Rules
A generated insight must be traceable to permitted source evidence. The system must:
- Distinguish direct review content from derived summary.
- Record model/version.
- Record evidence set.
- Avoid quoting text beyond permitted usage.
- Avoid claiming a theme is dominant when evidence is too sparse.

## Temporal Analysis
Insights should distinguish current experience from historical reputation. A place that improved recently should not be permanently anchored to old evidence, while a temporary burst should not erase long-term context.

## Safety
Reviews may contain PII, accusations, harassment, medical information, or other sensitive content. Processing and display rules must apply moderation, privacy, and source terms before content is exposed.
