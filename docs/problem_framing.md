# SmartLend Problem Framing

## Prediction Task

SmartLend is developing a machine learning model to predict whether a borrower will experience serious delinquency within the next two years. This is a supervised binary classification problem. The target variable is `SeriousDlqin2yrs`, where 0 represents no serious delinquency and 1 represents serious delinquency.

## Likely Users of the Prediction

The prediction could be used by SmartLend's lending and risk teams to support credit-risk assessment and lending decisions. Direct users may include loan officers, credit-risk analysts, and decision-making systems. Indirect stakeholders include applicants and existing borrowers, who may be affected by lending decisions, as well as compliance, governance, and management teams responsible for ensuring that the model is used appropriately.

## Potential Failure Modes

A false positive occurs when the model predicts that a borrower is likely to become seriously delinquent when they would not. This could result in a creditworthy applicant being refused a loan or receiving less favourable lending terms, potentially causing financial disadvantage to the applicant.

A false negative occurs when the model predicts that a borrower is unlikely to become seriously delinquent when they subsequently do. SmartLend could approve lending to a borrower who later defaults, resulting in financial losses and increased credit risk for the organisation.

The dataset is also highly imbalanced, with approximately 93.3% of records having no serious delinquency and 6.7% having serious delinquency. A model that simply favours the majority class could therefore appear accurate while performing poorly at identifying borrowers who are actually at risk.

## Definition of Success

The model should demonstrate reliable performance in identifying serious delinquency, with evaluation metrics that are appropriate for an imbalanced binary classification problem rather than relying on accuracy alone. Precision, recall, F1-score and suitable threshold-based evaluation should be considered.

The model should also be tested for consistent performance across relevant groups and checked for potential sources of unfair or discriminatory outcomes. Predictions should be sufficiently reliable and explainable for appropriate human oversight.

Before deployment, SmartLend should have suitable monitoring, documentation, data-quality checks, model validation, privacy and governance processes. The model should support human decision-making rather than being treated as an unquestionable decision-maker, with processes available to review potentially incorrect or disputed outcomes.
