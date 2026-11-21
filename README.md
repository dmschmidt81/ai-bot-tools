# AI Bot Tools

Structured AI assistants for education, administration, career workflows, and personal productivity.

This repository is the public portfolio for a growing collection of AI assistants designed around clear roles, bounded permissions, verification, human approval, and repeatable workflows.

## Purpose

The goal of this project is to explore how AI can be designed as a practical system rather than used only as a general-purpose chatbot.

Each assistant is built for a defined use case and may include:

- A specific role and mission
- Clear behavioral rules
- Source-of-truth requirements
- Human approval gates
- Privacy and security boundaries
- Verification and review steps
- Structured outputs
- Handoffs to other tools or workflows

The emphasis is on making AI behavior more useful, predictable, auditable, and aligned with human decision-making.

## Bot Categories

Public tools in this repository may include assistants for:

### Education

AI assistants that support teaching, tutoring, test preparation, programming practice, feedback, and student independence.

### Administration

AI assistants that support structured communication, scheduling, procedural workflows, and repeatable administrative tasks.

### Career

AI assistants that support job-search workflows, resume and cover-letter preparation, application tracking, source verification, and professional development.

### Personal Productivity

AI assistants that support organized personal workflows while maintaining explicit boundaries around permissions, sensitive data, and external actions.

## Repository Structure

```text
ai-bot-tools/
├── README.md
├── LICENSE
├── CONTENT-NOTICE.md
├── SECURITY.md
├── GOVERNANCE.md
│
├── bots/
│   ├── education/
│   │   ├── ap-csa/
│   │   └── ap-statistics/
│   ├── administration/
│   ├── career/
│   └── personal/
│
├── evals/
│   ├── ap-csa-tutor/
│   │   ├── README.md
│   │   ├── test-cases.md
│   │   └── results.md
│   └── ap-statistics/
│       ├── README.md
│       ├── test-cases.md
│       └── results.md
│
├── templates/
├── architecture/
├── examples/
└── instructor-portfolio/
    ├── practical-generative-ai/
    └── teaching-evidence/
```

### What Each Area Demonstrates

- **bots/** — public, sanitized assistant specifications organized by domain
- **evals/** — expected behavior, conformance testing, runtime evidence, and re-test history
- **templates/** — reusable design patterns and review structures
- **architecture/** — system diagrams, trust boundaries, permissions, and design trade-offs
- **examples/** — sanitized demonstrations of real workflows and assistant behavior
- **instructor-portfolio/** — instructor-ready workshops, labs, assessments, facilitator materials, and public teaching evidence
- **GOVERNANCE.md** — shared standards for authorization, evidence, privacy, security, quality, and human control
- **SECURITY.md** — public disclosure rules and security reporting guidance
- **CONTENT-NOTICE.md** — reuse and licensing boundary for written portfolio content

Some folders intentionally contain placeholders while the corresponding public artifacts are being prepared and sanitized.

## AI Instruction Portfolio

This repository also demonstrates the ability to teach practical AI skills to other people.

### Practical Generative AI: From Prompt to Reliable Workflow

The first instructor-ready workshop includes:

- Learning objectives
- Facilitator guide
- Learner guide
- Four hands-on labs
- Pre- and post-assessments
- Performance rubric
- Quick-reference job aid
- 15-minute sample lesson
- Teaching-evidence framework for selected public instructional videos

- [AI Instructor Portfolio](./instructor-portfolio/README.md)
- [Practical Generative AI Workshop](./instructor-portfolio/practical-generative-ai/README.md)
- [Teaching Evidence](./instructor-portfolio/teaching-evidence/README.md)
- [15-Minute Sample Lesson](./instructor-portfolio/practical-generative-ai/sample-lessons/verify-ai-output-15-minute.md)

The written materials demonstrate instructional design and responsible-AI curriculum development. Selected public videos can demonstrate live explanation, facilitation, and on-camera teaching.

## Governance

All substantive assistants in this repository are intended to follow the principles defined in [GOVERNANCE.md](./GOVERNANCE.md).

The governance standard establishes reusable expectations for:

- Human authority and autonomy
- Truthfulness and evidence
- Least-privilege access
- Security and privacy
- Prompt-injection awareness
- Controlled change
- Explicit approval gates
- Verification and testing
- Incident handling
- Auditability
- Separation of design, implementation, testing, and release decisions

A policy prompt is not treated as a complete security boundary. Important safeguards should also be enforced through technical controls where the platform supports them.

## Design Principles

### Human Control

The human operator remains responsible for goals, permissions, consequential decisions, and release approval.

### Verify Before Acting

Assistants should distinguish verified facts from assumptions, inferences, and missing information before taking consequential action.

### Least Privilege

Access should be limited to the minimum files, accounts, tools, destinations, and permissions required for the current task.

### Explicit Approval

Permission to inspect, draft, or test does not automatically grant permission to edit, send, publish, deploy, delete, or otherwise change external state.

### Support Thinking

Educational tools are designed to strengthen understanding and independent reasoning rather than simply complete work for the user.

### Reusable Systems

Common patterns are documented and reused so that new assistants can be designed more consistently and reviewed more effectively.

## Public vs. Private Development

This repository is the public-facing collection of selected, sanitized tools and documentation.

Development versions, experimental prompts, sensitive workflows, internal notes, private data, and organization-specific material may be maintained separately and are not automatically published here.

## Evaluation

This repository includes repeatable behavioral evaluations so assistant quality is demonstrated with evidence rather than described only in prose.

Current evaluation areas:

### AP Computer Science A

- [AP CSA Tutor Evaluations](./evals/ap-csa-tutor/README.md)
- [AP CSA Expected Test Cases](./evals/ap-csa-tutor/test-cases.md)
- [AP CSA Results](./evals/ap-csa-tutor/results.md)

### AP Statistics

- [AP Statistics Bot Specification](./bots/education/ap-statistics/AP-Stats-Exam-Prep-Coach-v1.0-public.md)
- [AP Statistics Evaluations](./evals/ap-statistics/README.md)
- [AP Statistics Expected Test Cases](./evals/ap-statistics/test-cases.md)
- [AP Statistics Results](./evals/ap-statistics/results.md)

### Administration — C3 Communications

- [C3 Communications Assistant — Public Specification](./bots/administration/C3-Communications-Assistant-v3.1-public.md)
- [C3 Administration Evaluations](./evals/c3-administration/README.md)
- [C3 Expected Test Cases](./evals/c3-administration/test-cases.md)
- [C3 Results](./evals/c3-administration/results.md)

### Personal AI — Steele

- [Steele Personal AI — Public Specification](./bots/personal/Steele-Personal-AI-v1.0-public.md)
- [Steele Evaluations](./evals/steele-personal/README.md)
- [Steele Expected Test Cases](./evals/steele-personal/test-cases.md)
- [Steele Results](./evals/steele-personal/results.md)

Each evaluation record states what kind of evidence it contains. Manual specification-conformance dry runs are labeled separately from deployed runtime tests. When a run is performed, the record may include the assistant version, prompt, observed or simulated response, expected behavior, result, required correction, and re-test outcome. Tests include both normal scenarios and adversarial attempts to override constraints.

## Project Status

This repository is under active development.

Assistants and supporting documents may change as they are tested, reviewed, and improved. Versioning will be used where substantive changes affect behavior, governance, or workflow expectations.

## Skills Demonstrated

This project reflects work in:

- AI assistant and prompt design
- Requirements analysis
- Workflow design
- Human-in-the-loop systems
- Security and privacy thinking
- Approval and authorization logic
- Threat modeling
- Instructional design
- Adult learning and facilitation
- AI literacy instruction
- Assessment and rubric design
- Educational technology
- Structured problem solving
- Documentation
- Version control with Git and GitHub

## Licensing

Source code and software components explicitly identified as MIT-licensed are covered by the [MIT License](./LICENSE).

Bot specifications, prompts, governance materials, evaluations, instructional materials, and other written portfolio content are governed by the [Content and Reuse Notice](./CONTENT-NOTICE.md) unless a specific file states otherwise.

See [SECURITY.md](./SECURITY.md) for the public-disclosure boundary and [the publication review checklist](./templates/publication-review-checklist.md) for pre-publication review.

## Background

I am a high school computer science and technology educator with a previous background in mathematics education who is transitioning toward professional software development.

This project combines my experience in education, curriculum design, computer science, AI experimentation, workflow design, and security-minded system development.
