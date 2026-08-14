# Module2 Onboarding Prompt Template

Use this prompt to generate FinWise's personalized onboarding communication plan.

```text
I am a PM at FinWise Co. designing onboarding for new trial users.

FinWise is a financial-management SaaS product for small businesses. It uses a product-led growth model with a reverse trial. The product helps owners understand cash flow, expenses, payroll risk, invoices, and short-term runway.

Create a complete onboarding communication plan for new trial users.

Objective:
Move new trial users from sign-up to their first useful cash-flow forecast as fast as possible. The onboarding should help users import or use pre-filled financial data, see a specific cash-flow insight, and share that insight with an accountant, bookkeeper, or co-owner.

User segments:
Primary users are small-business owners, founders, and operators who manage cash flow without a full finance team. They are busy, skeptical of setup work, and care about immediate questions: can I make payroll, which invoices are creating risk, and how much runway do I have?

Secondary users are accountants, bookkeepers, and co-owners who may be invited to review a forecast, comment on assumptions, or help update the plan.

User journey:
1. Sign-up: choose the first financial job FinWise should do, such as forecast cash flow or plan payroll.
2. Setup: use pre-filled sample data, connect a bank account, import QuickBooks, or upload a CSV.
3. First model: confirm one key assumption, such as estimated monthly overhead.
4. Aha moment: review a personalized cash-flow forecast with a specific risk date, shortfall amount, and recommended action.
5. Collaboration: share the forecast with an accountant, bookkeeper, or co-owner.

Aha moment:
The Aha moment is when a trial user sees FinWise turn business financial data into a specific cash-flow forecast they can act on immediately, then shares that forecast with an accountant, bookkeeper, or co-owner.

Purpose of prompts:
Each message should move the user one step closer to a useful financial forecast. The prompts should reduce setup friction, explain why the next action matters, and make the forecast feel tied to the user's business rather than a generic dashboard.

Personalization rules:
Tailor messages by business type, selected financial goal, user role, data source, monthly overhead, cash balance, payroll amount, overdue invoices, projected risk date, shortfall amount, and collaborator role.

Frequency:
Keep prompts sparse and event-triggered. Use in-app prompts during onboarding. Use one follow-up email or reminder only if the user abandons before generating or sharing the forecast.

Timing:
Prompt immediately after sign-up to pick the first job. Prompt after data selection to confirm the key assumption. Prompt after the forecast appears to share it. If the user does not finish, send one reminder within 24 hours focused on completing the forecast.

Tone:
Clear, calm, financially literate, and specific. Avoid hype. Write like FinWise is helping the owner make a money decision, not selling software.

Success metrics:
Primary KPI: first cash-flow forecast completion rate.
Secondary KPI: forecast share rate with an accountant, bookkeeper, or co-owner.

Limitations:
Many users will not want to connect real financial accounts during the first session, so onboarding should offer pre-filled sample data as the fastest path. Do not require a full company profile, product tour, team setup, or multiple integrations before the first forecast. Keep sensitive financial copy concise and avoid implying certainty where the forecast depends on assumptions.

Please organize the onboarding plan as a table with these columns:
Stage, User Segment, Message Type, Frequency, Limitations, Prompt Message, Purpose, Message Content.

For Message Content, write the actual user-facing copy FinWise should show. Keep each message short and action-oriented.
```
