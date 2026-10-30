Dissertation / Project / Project Work Title

Explainable NLP Assistant for Suspicious Activity Report Drafting

Project Abstract and Outline Report

Course No.: [To be filled]

Course Title: Dissertation

Student Name: [To be filled]

BITS ID: [To be filled]

Degree Program: M.Tech. Artificial Intelligence and Machine Learning

Research Area: Operational Risk Management

Broad Academic Area: Natural Language Processing and Explainable Artificial Intelligence

Organization and Location: [To be filled]

BIRLA INSTITUTE OF TECHNOLOGY & SCIENCE, PILANI

VIDYA VIHAR, PILANI, RAJASTHAN - 333031

Month and Year: [To be filled]

## Contents

Project Abstract

1. Broad Area of Work

2. Background

3. Objectives

4. Scope of Work

5. Plan of Work

6. Literature References

7. Particulars of the Supervisor and Examiner

8. Remarks of the Supervisor

Outline Identification and Signatures

## Project Abstract

Investigators reviewing financial transaction alerts must combine transaction records, customer information and case notes into clear, evidence-based narratives. Manual drafting can be time-consuming, while language-model-generated text may introduce unsupported statements, omit relevant facts or conceal gaps in the available information. This project proposes an explainable natural language processing assistant for preparing Suspicious Activity Report (SAR) narrative drafts from synthetic case records.

The proposed system will combine information extraction, retrieval-augmented generation and structured narrative generation. It will normalize case information, construct a chronological transaction timeline, compute transaction totals using deterministic code and retrieve supporting passages from the active case. Each material claim in the generated narrative will be linked to a source record, note excerpt or reproducible calculation. Missing information and conflicting evidence will be presented as questions or review flags rather than completed through inference.

The prototype will provide a reviewer interface for inspecting evidence, editing the narrative and exporting a versioned draft. Evaluation will compare a template baseline, direct language-model drafting, basic retrieval-augmented drafting and the proposed evidence-validation pipeline. Measures will include factual consistency, citation support, completeness, missing-information detection and reviewer feedback. Expert review will be sought where available. The intended outcome is a reproducible academic prototype that supports narrative preparation and evidence verification. Outputs will remain human-reviewed drafts; the system will neither file reports automatically nor determine that a crime has occurred.

## 1 Broad Area of Work

The project applies natural language processing and explainable artificial intelligence to operational risk management, with a focus on financial investigation documentation. The technical areas are information extraction, retrieval-augmented generation, structured text generation and evidence-based evaluation. Explainability will be provided through source attribution, transaction timelines, reproducible calculations and explicit uncertainty.

## 2 Background

Financial investigation teams review alerts together with transaction histories, customer profiles and investigator notes. Preparing a coherent narrative requires organizing events, checking dates and amounts, explaining the documented reason for review and distinguishing verified facts from observations. In financial-services operations, this work creates a practical need for tools that improve documentation consistency and make the basis of each statement easy to inspect.

A general-purpose language model can produce fluent text without reliably preserving every fact. Retrieval can supply relevant evidence, but a citation alone does not establish that the attached claim is supported. An assistant therefore needs both structured evidence and validation. Narrative guidance from FinCEN and FFIEC informs the organization of the prototype narrative [1, 2], while research on RAG and citation generation informs the technical approach [3, 4].

The proposed study is relevant to operational risk and investigation-support workflows in the employing organization. It will use synthetic records and will not depend on confidential employer data or access to production systems. Any later organization-specific adoption would require separate assessment. The academic prototype will not claim regulatory compliance or automate a reporting decision.

## 3 Objectives

1. Define a structured synthetic-case schema with stable references to transactions, customer information, alerts and case notes.

2. Extract relevant entities, dates and attributed observations, and construct an accurate transaction timeline with deterministic calculations.

3. Generate structured narrative drafts using case-scoped retrieval, with evidence references for each material factual claim.

4. Identify missing information, contradictory evidence and unsupported claims, and make these visible to the reviewer.

5. Implement a review interface that supports source inspection, editing, version tracking and draft export.

6. Evaluate factual consistency, evidence support, completeness and reviewer effort against simpler drafting baselines.

## 4 Scope of Work

## Independent work by the student

The student will undertake the literature review, define the data and annotation schemas, create the synthetic dataset, implement the prototype, conduct the experiments and prepare the dissertation. The supervisor will guide scope and methodology and review progress. Domain feedback will be sought to assess scenario realism and narrative quality where suitable reviewers are available.

## Inputs and processing

Inputs will be English-language synthetic case bundles containing an alert description, customer and account attributes, transaction records, and investigator notes in CSV, JSON and plain text. The pipeline will validate records, preserve exact source references, extract note facts and retrieve evidence only from the active case. Guidance documents may inform narrative structure but will not serve as evidence about a customer.

Dates, transaction status and currencies will be normalized explicitly. Totals will be computed with decimal arithmetic and kept separate by currency and transaction direction. Reversals, duplicates and attempted transactions will be handled through defined rules. The generator will receive validated facts and selected excerpts, then return structured claims with evidence identifiers. Validation will flag missing, incorrect or insufficient support.

## Outputs and reviewer workflow

Outputs will include a narrative draft, transaction timeline, evidence appendix and missing-information checklist. A reviewer will be able to open the source supporting a claim, edit or reject text and record review comments. Edits will trigger revalidation and create a new draft version. The final export will remain labelled as a human-review draft.

## Evaluation and deliverables

A target of 120 synthetic scenario families will be divided into development, validation and held-out test sets, with related variants kept in the same split. Cases will include incomplete information, contradictory notes, reversals and documented benign explanations. Gold annotations will identify required facts, valid supporting evidence and information gaps.

The evaluation will compare deterministic templates, direct LLM drafting, basic RAG and the proposed pipeline. Factual consistency will measure supported material claims; evidence evaluation will distinguish citation presence from actual support. Completeness will measure required facts correctly represented. Missing-information precision and recall, numerical accuracy, latency and cost will also be reported. Independent reviewer feedback will supplement automated checks; proxy review will be identified if a domain expert is unavailable.

Deliverables will comprise the prototype, synthetic-data generator, annotation guide, baseline implementations, evaluation results, source repository and dissertation report. Real customer data, automatic SAR submission, crime determination, production banking integration and model training at scale are excluded.

## 5 Plan of Work

The work is planned over 16 weeks. Relative weeks will be mapped to the approved semester dates before submission. Literature notes, implementation decisions and experiment results will be documented throughout the project.

| Phase | Period | Work and deliverable |
| --- | --- | --- |
| Problem definition and literature review | Weeks 1–2 | Confirm scope, narrative terminology and review criteria. Prepare the literature matrix, schema and project outline. |
| Synthetic data and annotations | Weeks 3–4 | Create and review synthetic cases, annotate facts and evidence, freeze dataset splits and implement the template baseline. |
| Ingestion and evidence processing | Weeks 5–6 | Implement source tracking, note extraction, normalization, transaction timeline and deterministic calculations. |
| Retrieval and generation | Weeks 7–8 | Implement case-scoped retrieval and structured drafting. Establish direct-LLM and basic-RAG baselines and demonstrate the pipeline. |
| Validation and information gaps | Weeks 9–10 | Validate evidence references and numerical claims. Detect missing information and contradictions. Test failure cases. |
| Reviewer interface and integration | Weeks 11–12 | Implement evidence navigation, editing, versioning and draft export. Complete integration tests and freeze evaluation settings. |
| Evaluation and review | Weeks 13–14 | Run held-out comparisons, analyze factuality and completeness, gather reviewer feedback and document limitations. |
| Report and submission | Weeks 15–16 | Prepare the dissertation, incorporate supervisor feedback, verify reproducibility and complete the final demonstration and submission. |



## Milestones and progress review

The major milestones are an agreed outline by week 2, a dataset and template baseline by week 4, an end-to-end demonstration by week 8, a reviewable prototype by week 12, evaluation results by week 14 and the final report by week 16. Progress will be reviewed against these deliverables, with optional enhancements deferred if needed to protect evaluation and report quality.

## Feasibility

The prototype will use a modular Python backend, a lightweight web interface and a single configurable language-model provider. Model selection will follow a small development-set pilot. API use will remain within an agreed budget. Synthetic data avoids dependence on confidential records; the final report will acknowledge limits on generalization to real investigations.

## 6 Literature References

The preliminary literature covers narrative quality, retrieval-augmented generation, citation-based evidence verification and reporting terminology. These sources will guide the methodology; they do not establish that the prototype meets an official filing standard.

[1] Financial Crimes Enforcement Network (FinCEN). Guidance on Preparing a Complete & Sufficient Suspicious Activity Report Narrative. Available at: https://www.fincen.gov/sites/default/files/shared/sar_guidance_narrative.pdf

[2] Federal Financial Institutions Examination Council (FFIEC). BSA/AML Examination Manual, Appendix L: SAR Quality Guidance. Available at: https://bsaaml.ffiec.gov/manual/Appendices/13

[3] P. Lewis et al. (2020). Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks. Advances in Neural Information Processing Systems, 33, 9459–9474. Available at: https://arxiv.org/abs/2005.11401

[4] T. Gao, H. Yen, J. Yu and D. Chen (2023). Enabling Large Language Models to Generate Text with Citations. Proceedings of EMNLP 2023, pp. 6465–6488. Available at: https://aclanthology.org/2023.emnlp-main.398/

[5] Financial Intelligence Unit–India. Frequently Asked Questions. Available at: https://fiuindia.gov.in/files/FAQs/FAQs.html

## Relationship to the proposed study

References [1] and [2] motivate clear chronological narratives and explicit descriptions of the available evidence. Reference [3] provides the foundation for retrieving relevant context before generation. Reference [4] motivates separate evaluation of correctness and citation quality. Reference [5] provides the Indian reporting context, where Suspicious Transaction Report (STR) terminology is used.

The project title retains SAR terminology. If an India-specific framing is selected, the terminology and narrative template will be aligned consistently before implementation. No filing thresholds or regulatory reporting decisions will be encoded in the prototype.

## 7 Particulars of the Supervisor and Examiner

| Particulars | Supervisor | Additional Examiner |
| --- | --- | --- |
| Name |  |  |
| Qualification |  |  |
| Designation |  |  |
| Employing Organization and Location |  |  |
| Phone No. with STD Code |  |  |
| Email Address |  |  |



## 8 Remarks of the Supervisor

The proposed project addresses a practical problem in financial investigation documentation and provides an appropriate setting for applying natural language processing, information retrieval and explainable artificial intelligence. Its focus on evidence-linked narrative drafting, missing-information detection and reproducible transaction calculations gives the work a clear technical scope.

The proposed evaluation against template-based and language-model baselines should enable a systematic assessment of factual consistency, evidence support and completeness. Particular attention should be given to independent review of synthetic annotations, separation of development and test cases, and transparent reporting of unsupported claims and omitted evidence.

The work should remain limited to synthetic case records and human-reviewed drafts. The student should complete the implementation and evaluation independently under supervision, document limitations and avoid claims of regulatory compliance or automated determination of wrongdoing. The scope and schedule may be refined in line with the approved semester requirements and available reviewer support.

Additional remarks: __________________________________________________

__________________________________________________________________

Supervisor signature: _______________________    Date: _________________

BIRLA INSTITUTE OF TECHNOLOGY & SCIENCE, PILANI

WORK INTEGRATED LEARNING PROGRAMMES (WILP) DIVISION

Semester: [To be filled]    Academic Year: [To be filled]

Course No.: [To be filled]    Course Title: Dissertation

## Outline Identification and Signatures

| Identification information | Details |
| --- | --- |
| STUDENT ID No. |  |
| NAME OF THE STUDENT |  |
| STUDENT’S EMAIL ADDRESS |  |
| STUDENT’S EMPLOYING ORGANIZATION & LOCATION |  |
| SUPERVISOR’S NAME |  |
| SUPERVISOR’S EMPLOYING ORGANIZATION & LOCATION |  |
| SUPERVISOR’S EMAIL ADDRESS |  |
| ADDITIONAL EXAMINER’S NAME |  |
| ADDITIONAL EXAMINER’S EMPLOYING ORGANIZATION & LOCATION |  |
| ADDITIONAL EXAMINER’S EMAIL ADDRESS |  |
| DISSERTATION / PROJECT / PROJECT WORK TITLE | Explainable NLP Assistant for Suspicious Activity Report Drafting |



The project outline comprises the broad area of work, background, objectives, scope, semester work plan, literature references, supervisor and examiner particulars, and supervisor remarks.

| Student | Supervisor | Additional Examiner |
| --- | --- | --- |
| Signature:  __________________ | Signature:  __________________ | Signature:  __________________ |
| Name: | Name: | Name: |
| Date: | Date: | Date: |

