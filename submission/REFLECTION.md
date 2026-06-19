# Reflection - Day 17

The quietest failure would be trace-to-Bronze flattening. If parent/child spans,
outcomes, or prompt metadata are lost, the pipeline still runs but the eval set
and DPO pairs become misleading. I would detect it with row-count checks per
trace, required `gen_ai.*` fields, and sample audits against raw traces.

Skipping decontamination would train on prompts also used for evaluation. The
model could look better because it memorized the benchmark, not because it
generalized. Metrics would show suspiciously high eval scores, especially on
seen prompts, while new production prompts would not improve as much.

A dangerous feature is a user's lifetime spend or number of support tickets. If
I predict churn on June 1, I must not join values updated after June 1. An ASOF
join keeps only facts known at prediction time.

The graph answers the multi-hop question "Where does a widget ship from?" well:
widget -> accessory -> Hanoi. Flat chunk retrieval struggles because the two
facts are split across chunks. For a simple question like "What is returnable?",
the graph is overkill; direct retrieval from the returns policy is enough.
