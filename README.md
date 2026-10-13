# Accessibility-First Engineering

*A sanitized case study on shifting accessibility from reactive remediation to a development-time consideration.*

> **Context:** This case study describes the problem, approach, and lessons from work on an enterprise wealth-management application. It intentionally excludes proprietary source code, internal architecture, customer information, screenshots, and other confidential details.

## The problem

Accessibility issues are often discovered after code has been written. Engineers then have to identify violations, understand what needs to change, implement fixes, and validate the results. In a large application, this can turn accessibility remediation into a time-consuming, repetitive task.

In the workflow I worked on, engineers could spend entire days fixing accessibility violations.

I wanted to make accessibility less of a downstream cleanup exercise and more of a consideration throughout development.

## The idea: an accessibility-first mindset

I use the term **accessibility-first mindset** to describe an approach in which accessibility is considered while code is being created—not only after implementation, when violations are discovered.

The goal was to help engineers move from:

**Write code → discover accessibility issues → remediate → validate**

toward a workflow where accessibility checks and guidance are incorporated earlier, reducing the amount of avoidable rework.

## The approach

I designed and built an accessibility testing and remediation workflow that combined three elements:

1. **Automated analysis** to surface accessibility violations in web code, including HTML, CSS, and JavaScript.
2. **AI-assisted workflows** to help engineers understand and address issues and to encourage accessibility considerations during code generation.
3. **Human validation** to review results and verify remediation rather than treating automated output as proof of correctness.

The central design principle was that automation should help engineers identify and resolve problems more efficiently, while human judgment remains part of the validation process.

This page intentionally stays at a high level and does not disclose internal implementation details.

## Impact

Based on the measurements available for the workflow:

- **Time:** Work that previously could take engineers entire days was brought to under 30 minutes in the workflow.
- **Detection:** The workflow was designed to identify approximately **85–90% of accessibility violations**.

These figures describe the reported workflow outcomes; they should not be interpreted as a universal benchmark or a guarantee that every detected issue was automatically fixed. Detection and successful remediation are different measures, and human validation remains important.

## What I learned

The most valuable change was not simply making an existing task faster. It was moving accessibility earlier in the development process.

A useful engineering workflow should do more than flag issues after the fact. It should give engineers feedback when they can still act on it, make the right path easier to follow, and support validation of the result.

The broader lesson is that automation is most useful when it improves both **developer workflow** and **the experience of the people who use the resulting software**.

## My contribution

I designed and built the core accessibility testing and remediation workflow described here, combining automated analysis, AI-assisted workflows, and human validation.

This is a sanitized account of the work. It does not include proprietary code, internal tools or architecture, confidential screenshots, or information about customers or systems.

## Limitations and next steps

Accessibility is broader than what any automated workflow can detect. Automated checks can surface many issues, but they cannot establish that an experience is accessible in every real-world context. Human review and, where appropriate, testing with assistive technologies and people with disabilities remain important.

Potential next steps for a standalone demonstration would include:

- Building a small example web page with common accessibility issues.
- Running public accessibility checks against it.
- Showing suggested fixes and validating the resulting page.
- Documenting what the automated checks catch—and what still requires human judgment.

Such a demo would be an independent illustration of the ideas in this case study, not a reproduction of the internal BNY implementation.

---

*Written as a public, high-level description of engineering work. All metrics should be confirmed as appropriate for external disclosure before publication.*
