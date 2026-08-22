# The Validation · FinWise

> Module 5 · Experimentation Methods. The experiment brief that tests the bet.

## Step 1: Choose The Method

| Field | Decision |
| --- | --- |
| Method | Standard A/B test |
| Justification | This is the cleanest method for the FinWise hypothesis because we are testing one onboarding path against the current reverse-trial experience. New trial users can be randomized at account creation, the experience is user-level, and the primary readout is an activation event within the first 24 hours. A multi-armed bandit would be premature because we are not optimizing several prompt variants. A switchback test does not fit because onboarding happens once per user. A long holdout would slow learning on the trial-to-paid problem without adding much signal. |

## Step 2: Define The Experiment

| Field | Decision |
| --- | --- |
| Experiment name | First Forecast Activation A/B Test |
| Objective | Increase the number of new trial users who import or use financial data and reach their first modeling output. This connects to the North Star from Module 4: trial users who import financial data and reach a first modeling output. |
| Hypothesis | If FinWise replaces generic trial onboarding with a guided first-forecast path for new trial users, then first modeling output completion within 24 hours will increase because users will see a specific cash-flow forecast before they are asked to explore the broader product. |
| Primary metric | First modeling output completion rate within 24 hours of trial start |
| Success threshold | Treatment must produce at least a 20% relative lift over control in first modeling output completion within 24 hours. Trial-to-paid conversion should also move directionally toward the Module 1 target of 2.4-2.6%, but the first read is the activation metric. |
| Guardrail metric | Day-1 onboarding drop-off must not increase by more than 5% relative to control. |

## Step 3: Define What Is Being Tested

| Field | Decision |
| --- | --- |
| Current experience | New trial users enter the reverse trial through a broader setup and product experience before they see a personalized financial output. The path asks users to understand the product before FinWise proves value with their business numbers. |
| What is being tested | A guided first-forecast onboarding path: choose the first financial job, use pre-filled sample data or connect one data source, confirm one key assumption such as monthly overhead, view a personalized cash-flow forecast, and share it with an accountant, bookkeeper, or co-owner. |
| Target segment | Brand-new trial accounts where the first user is a small-business owner, founder, or operator. Exclude invited accountants, bookkeepers, co-owners, existing customers, and returning trial users. |

## Step 4: Predict The Outcome

| Field | Decision |
| --- | --- |
| Predicted outcome | If the hypothesis is correct, the treatment group will produce at least a 20% relative lift in first modeling output completion within 24 hours. Forecast share rate should also improve because the new path makes the forecast useful enough to send to a collaborator. |
| If successful | Ship the guided first-forecast path as the default onboarding experience. Keep measuring trial-to-paid conversion through the full trial window, then test the next highest-friction point: whether sharing should happen immediately after the forecast or after one scenario adjustment. |
| If unsuccessful | Do not ship the full flow. Break down the onboarding funnel by step: first job selected, data source chosen, assumption confirmed, forecast viewed, and forecast shared. If users stop before data selection, reduce setup further with stronger pre-filled data. If users reach the forecast but do not continue, the issue is forecast trust or usefulness rather than onboarding speed. |

## Part 2: Result Readout

Another FinWise team tested two landing-page versions. Their hypothesis was that Version B would produce higher conversion and higher engagement because it used a simpler call to action and stronger design.

Dataset check: 20 users, with 10 users assigned to Version A and 10 assigned to Version B.

| Metric | Version A | Version B | Read |
| --- | ---: | ---: | --- |
| Conversion rate | 70% | 60% | A converts better by 10 percentage points. |
| Converted users | 7 of 10 | 6 of 10 | B does not support the conversion part of the hypothesis. |
| Average session duration | 180 seconds | 207 seconds | B holds attention 27 seconds longer. |
| Average feature engagement | 56.3% | 57.9% | B is 1.6 percentage points higher. |

Experiment lenses:

| Lens | Read |
| --- | --- |
| Statistical significance | The sample is too small to call a reliable winner. With 10 users per version, the 95% confidence interval for the B-minus-A conversion difference is roughly -52 to +32 percentage points. |
| Practical significance | B misses the main practical goal because conversion is 10 percentage points lower than A. The engagement lift is small: 1.6 percentage points. |
| Confidence interval | The interval is wide enough that the true effect could favor either version. The result is directional evidence, not proof. |
| Guardrails | No explicit guardrail was provided in the dataset. If conversion is treated as the guardrail, B fails it. |

| Question | Answer |
| --- | --- |
| Support or refute? | The result refutes the original hypothesis on conversion. Version A converted 70% of users, while Version B converted 60%. Version B did better on average session duration, 207 seconds versus 180 seconds, and feature engagement, 57.9% versus 56.3%. Those engagement gains do not offset the weaker conversion result. |
| Which scenario? | Mixed Signal. B attracts more attention and slightly more feature engagement, but it does not produce more conversions. This is not a Modest Win because the primary business outcome moved the wrong way. It is not a J-Curve because there is no later-period recovery data. It is not a False Peak because B did not create a higher short-term conversion spike. |
| Recommendation | Keep Version A as the live landing page for now. Version B has useful design signals, but FinWise should not ship a landing page that converts worse based on this read. |
| Next steps | Iterate on Version B by keeping the elements that raised engagement, then simplify the conversion path. Test whether the longer sessions came from healthy interest or confusion. Rerun the experiment with a larger sample, a pre-set minimum detectable effect, and a conversion guardrail before replacing A. |
