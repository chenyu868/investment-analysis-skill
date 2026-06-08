---
name: investment-analysis-skill
description: Create human-in-the-loop investment value reports for course projects, company research, industry research, and investor-style enterprise analysis. Use when the user needs an AI-assisted workflow that evaluates whether a company is worth investing in through industry trends, company trend fit, policy trend fit, SWOT, opportunities, peer comparison, value chain, customers, supporting industries, assumptions, risks, iteration notes, and a final deliverable.
---

# Investment Analysis Skill

## Overview

Use this skill to help a user complete an investor-style enterprise investment value report through a repeatable human-AI collaboration process. The output should be a defensible report, not an automatic buy/sell recommendation.

Always keep an iteration trail: record what the user provided, what assumptions were made, what changed after discussion, and which sections still need human verification.

## Workflow

### 0. Choose the mode

Use single-target mode when the user wants one complete report. Use multi-company testing mode when the user asks to test the skill, compare several companies, screen candidates, or improve the skill based on analysis results.

In multi-company testing mode:

- Choose 3-5 companies with different business models or risk profiles unless the user names specific companies
- Produce a short analysis plan for each company
- Keep each company output brief and comparable
- Add a cross-company comparison table
- End with a "Skill Improvement Notes" section that identifies where the workflow struggled
- Label outputs as drafts or course research, not investment advice

### 1. Confirm the task

Ask only for missing essentials:

- Investment target: company, stock code, industry, fund, commodity, or investment theme
- Report purpose: course assignment, internal memo, personal research, pitch, or comparison
- Required length, format, language, deadline, and citation style
- Available materials: financial statements, data files, links, class notes, screenshots, or prior drafts

If the user has no target, propose 3 practical options and ask them to choose.

### 2. Define the report scope

Use `references/report-framework.md` to choose the right structure. Keep the scope realistic:

- For a company: industry trend, company trend fit, policy trend fit, SWOT, opportunities, peer advantages/disadvantages, upstream and downstream value chain, customers, supporting industries, financials, valuation, risks, conclusion
- For an industry: market size, value chain, competition, policy/technology drivers, key companies, risks
- For an investment theme: thesis, catalyst, beneficiaries, constraints, evidence, risks

Write a short "analysis plan" before drafting the report. Include data needed, sections to write, and places where the user must verify facts.

For company investment value reports, treat these sections as required unless the user explicitly asks for a short version:

1. Industry development trend
2. Whether the company's development trend matches the industry trend
3. Industry policy trend
4. Whether the company's development trend matches the policy trend
5. SWOT analysis
6. Enterprise development opportunities
7. Peer comparison: advantages and disadvantages versus competitors
8. Upstream and downstream industry chain, customers, and supporting industries
9. Financial quality and valuation or scenario analysis
10. Overall investment value conclusion

### 3. Build the evidence base

Separate facts, assumptions, and judgments:

- Facts: sourced financial numbers, market data, company disclosures, policy documents
- Assumptions: growth rate, margin trend, valuation multiple, discount rate, scenario probabilities
- Judgments: competitive advantage, risk level, investment attractiveness

When current facts are required, browse or ask the user for sources. Do not invent current market prices, financial results, policies, or rankings.

Use this source priority for current company facts:

1. Company annual reports, interim reports, exchange filings, investor-relations pages, or official announcements
2. Securities exchange disclosures and official regulator databases
3. Reputable financial news summarizing filings
4. Analyst commentary or third-party databases, only when clearly labeled as secondary

If sources disagree, state the conflict and prefer official filings.

### 4. Draft the report

Use `assets/investment-report-template.md` as the default structure. Keep the report readable:

- Start with an executive summary
- Make the investment thesis explicit
- Put industry trend and policy trend before company-level judgment
- Explicitly judge whether company strategy matches industry and policy direction
- Use a SWOT table for company strengths, weaknesses, opportunities, and threats
- Compare the company with peers on concrete dimensions, not vague praise
- Map upstream suppliers, downstream customers, and supporting industries
- Put assumptions in tables when possible
- Explain causal logic, not only conclusions
- Include a risk section that can challenge the thesis
- End with a balanced conclusion and next verification steps

Avoid unsupported language such as "must rise", "guaranteed", or "risk-free". If the user asks for a recommendation, frame it as research judgment under stated assumptions.

### 5. Iterate with the user

After each draft, ask the user to react to one concrete issue at a time, such as:

- Is the investment target correct?
- Is the report too broad or too narrow?
- Should the conclusion be more cautious or more thesis-driven?
- Which assumption should be changed?

Maintain a change log:

```markdown
## Human-AI Collaboration Log

- Round 1: User selected target and report purpose.
- Round 2: AI proposed report structure; user adjusted scope.
- Round 3: AI drafted analysis; user corrected assumptions.
- Round 4: AI revised conclusion and risk section.
```

### 6. Finalize deliverables

Produce:

- Final investment analysis report
- Human-AI collaboration log
- Source and assumption list
- Open questions or verification checklist

For multi-company testing, also produce:

```markdown
## Cross-Company Comparison

| Company | Core thesis | Key evidence | Main risk | Best report angle |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
```

```markdown
## Skill Improvement Notes

- What worked:
- What failed or felt underspecified:
- What should be added to the Skill:
- What still needs human verification:
```

If the task is for a course, make the process visible enough that a teacher can see the report was produced through discussion and revision.

## Quality Checks

Before final output, verify:

- The report answers the user's chosen target and scope
- Industry trend is analyzed before company trend
- The report explicitly says whether company development matches industry trend
- Policy trend is analyzed and connected to the company's direction
- SWOT includes company-specific points rather than generic labels
- Peer advantages and disadvantages are compared against named competitors when possible
- Upstream, downstream, customers, and supporting industries are included
- Each major claim is supported by a source, user-provided material, or clearly labeled assumption
- The conclusion follows from the analysis instead of being pasted on
- Risks are specific to the target, not generic filler
- The collaboration log records real iteration
- No confidential credentials, private keys, or unrelated local files are included

## Reference Files

- `references/report-framework.md`: report structures, question prompts, and analysis standards
- `assets/investment-report-template.md`: reusable markdown template for the final report
