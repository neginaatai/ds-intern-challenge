# AI Usage Note

## Did I use AI?
Yes — I used Claude to help structure my analysis approach and suggest 
initial pandas code.

## What AI helped with
- Suggesting which pandas aggregation functions to use
- Initial code structure for groupby and agg operations
- README formatting suggestions
- Identifying which columns to prioritize in the summary table

## What I verified and decided myself
- Manually reviewed each row's notes column to identify anomalies
- Decided to exclude the demo account spike rather than just flag it — 
  the notes explicitly said "traffic spike from demo account" which 
  would inflate Lead summary metrics unfairly
- Chose acceptance_rate over median_confidence as the primary signal 
  because the domain packet explicitly warned that confidence does not 
  equal quality
- Noticed the August 7 Reply draft anomaly independently — flag rate 
  jumped from ~15% to 40% in one day, and user rating dropped to 2.1
- Decided to remove the duplicate row rather than average it — treating 
  it as a data quality issue not a real session
- Chose to focus on one clear angle (which workflow is most useful) 
  rather than trying to answer everything

## What I would do differently
- Ask the team whether the August 7 policy change was intentional 
  before drawing conclusions about Reply draft quality
- Validate whether avg_minutes_saved estimates come from a consistent 
  methodology across teams
