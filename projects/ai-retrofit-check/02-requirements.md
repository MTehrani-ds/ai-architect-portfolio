# AI Retrofit Check — Requirements

## 1. Functional requirements

### Assessment

The system must allow an SME user to:

- enter company information such as company name, industry, company size, and contact details
- complete a structured AI-readiness questionnaire
- save assessment answers during the session
- submit the completed assessment

### Scoring and analysis

The system must:

- calculate overall AI readiness
- calculate separate scores for:
  - process maturity
  - data readiness
  - system integration readiness
  - team readiness
  - governance and risk readiness
- identify major bottlenecks and opportunities
- recommend a suitable first AI or automation sprint
- generate a 30-day implementation roadmap

### Results dashboard

The system must display:

- company snapshot
- readiness score
- category scores
- key bottlenecks
- recommended first sprint
- 30-day roadmap
- clear call to action to contact Novixx

### Report generation

The system must:

- generate a downloadable PDF report
- include company information and assessment results
- include recommendations and roadmap
- clearly state that recommendations are indicative and require validation by Novixx

### Lead capture

The system must:

- collect contact details with consent
- provide a consultation-request option
- send or store a qualified lead for Novixx follow-up

---

## 2. Non-functional requirements

### Security

- User data must be transmitted securely using HTTPS.
- Secrets, API keys, and passwords must never be stored in source code.
- Access to internal admin functions must require authentication.
- Sensitive data must not be sent to an AI provider without a clear purpose.

### Privacy

- The platform should collect only data necessary for the assessment.
- Users should be informed how their data will be used.
- Personal data should be removable on request.
- Assessment data should not be used to train external AI models without explicit consent.

### Reliability

- The assessment should not lose user input if a page reload occurs.
- If the AI service fails, the platform should still show rule-based scoring and recommendations.
- PDF generation failures should not prevent users from seeing their dashboard results.

### Performance

- Dashboard results should appear within 5 seconds after submission where possible.
- AI-generated recommendations should be returned within 30 seconds.
- PDF reports should be generated within 60 seconds.

### Scalability

- The architecture should support growth from a few assessments per week to hundreds per month.
- AI generation and PDF creation should be separable from the user interface.
- The design should allow future CRM, email, and ERP integrations.

### Cost control

- AI usage must have token or cost limits per assessment.
- The system should log AI calls, model used, response time, and estimated cost.
- Expensive tasks such as report generation should not run repeatedly without need.

### Maintainability

- Business scoring rules must be separated from the user interface.
- Prompts and AI logic must be versioned.
- Architecture decisions must be documented.
- Errors and system activity must be logged.

---

## 3. Success criteria for version 1

The first version is successful when:

- an SME can complete the assessment without support
- the system generates understandable results and a practical next step
- Novixx receives a qualified lead or consultation request
- the report provides enough value to support a first client conversation
- the platform can be demonstrated professionally to potential partners and clients
