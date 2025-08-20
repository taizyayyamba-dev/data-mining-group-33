# data-mining-group-33

## assignment on Moodle

### data minning assignment

# Business Understanding (Draft for JoNAS Project)

## Problem Statement

The Journal of Natural Sciences (JoNAS), hosted by the University of Zambia, publishes a wide range of research articles across different disciplines of natural sciences. Currently, articles are archived online with minimal metadata, making it difficult for researchers, students, and librarians to quickly identify which field (e.g., Biology, Chemistry, Environmental Science, Physics, Agriculture) a paper belongs to. This lack of structured categorization reduces discoverability, hinders cross-disciplinary research, and increases the workload of editors and readers who must manually scan articles.
We aim to build a system that automatically classifies articles into scientific fields based on their content, improving discoverability and supporting efficient indexing for the JoNAS archive.

Currently, the lack of structured metadata in JoNAS articles limits visibility outside local academic circles. Implementing a classification system will organize content and make it more accessible internationally, potentially increasing citations and fostering collaborations. Additionally, this structured data can help identify research gaps across disciplines and support long-term monitoring of Zambian research output.

## Business Objectives

Improve the discoverability of articles in JoNAS by automatically tagging them with relevant fields.

Reduce manual workload of editors and librarians in organizing submissions.

Support students and researchers in finding relevant literature more quickly.

Lay the foundation for potential future features, such as article recommendation or citation impact prediction.

Primary Stakeholders & Decisions:

Owner: Journal Editorial Board (JoNAS, University of Zambia).

Users: Researchers, students, and librarians accessing the archive.

Decisions influenced: How articles are categorized, displayed, and searched in the online journal system.

## Data Mining Goals

Classification: Build a supervised model to predict the field of study of an article (e.g., Biology, Chemistry, Environmental Science, Physics, Agriculture) based on text features such as title, abstract, and keywords.

Regression/Forecasting: Predict potential citation impact or readership of articles.

Explainability: Provide interpretable outputs (e.g., feature importance, keywords driving classification) so editors understand why an article was assigned to a given category.

Inputs (initial hypothesis):

Features: article titles, abstracts, keywords, metadata from JoNAS archive.

Grain of data: article-level (one row per article).

Data availability: existing JoNAS issues (static, batch download).

## Initial Project Success Criteria

Technical:

Classification model achieves ≥ 80% accuracy and ≥ 0.75 F1 score in predicting correct field labels.

Baseline benchmark: majority class classifier accuracy.

Explainability available through word importance visualization.

Business:

Article classification reduces manual tagging workload by at least 50% for editors.

Categorized articles improve searchability (demonstrated through prototype search by field).

Outputs can be integrated into a one-page metadata summary for JoNAS archive.

## Scope, Assumptions & Constraints

In-scope: Research articles in JoNAS archive (titles, abstracts, keywords).

Out-of-scope: Full-text parsing of PDFs; non-Natural Science articles.

Assumptions: Abstracts and metadata are available and clean enough for classification.

Constraints: Potentially small dataset; imbalanced categories; metadata inconsistencies.

Ethics & Privacy: No personal or sensitive data—only published research. Ensure transparency in how classifications are assigned.

## Stakeholders & RACI

Responsible (builders): Taizya, Adel, Reginald, Royd, Gift

Accountable: Course Instructor/TA

Consulted: JoNAS editors (hypothetical domain experts)

Informed: University research community

## Risks & Mitigations

Small or imbalanced dataset → Use data augmentation or resampling.

Noisy or inconsistent article metadata → Apply text preprocessing (cleaning, tokenization).

Overfitting due to limited categories → Use cross-validation and simpler interpretable models initially.
