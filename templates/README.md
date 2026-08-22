# SignalDesk Workflow Health Check

## What I built
A Python analysis answering: which SignalDesk workflow is most useful right now?

## Who it is for
A product teammate deciding which workflow to trust and invest in next.

## Data source
product_usage_events.csv — internal SignalDesk export (7 days, 3 workflows)

## Assumptions
- Removed duplicate August 5 row noted in export
- Excluded demo account traffic spike from August 5 Sales data
- Standardized team name casing (product → Product)
- Treated avg_minutes_saved as directional only per domain notes

## Issues noticed
- Duplicate row on August 5
- Demo account spike inflates Sales Lead summary metrics
- Reply draft flag rate spiked to 40% on August 7 due to policy change
- Missing user ratings and confidence values in some rows
- Team name casing inconsistency (product vs Product)

## Key finding
Lead summary is the most trustworthy workflow — 78% acceptance rate, 
10% flag rate, consistent volume. Hold Reply draft expansion until 
August 7 anomaly is understood.

## What I would do next
- Monitor Reply draft flag rate daily after policy change
- Gather more Feedback clustering volume before drawing conclusions
- Clarify accepted_output definition with the team
- Build a simple weekly health check dashboard
