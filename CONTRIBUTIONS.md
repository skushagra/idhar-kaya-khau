# Contributions

## Kushagra

### Insight Agent

* Restaurant metadata analysis
* Customer fit identification
* Service extraction
* Operational insights
* Opening hours analysis
* Restaurant categorization
* Prompt engineering
* Output schema maintenance

### Review Agent

* Review analysis
* Dish extraction
* Theme extraction
* Sentiment analysis
* Service observations
* Crowd observations
* Prompt engineering
* Output schema maintenance

---

## Paramjeet

### Recommendation Agent

* Consumed Insight Agent and Review Agent outputs
* Recommendation scoring
* Confidence scoring
* Risk assessment
* Ranking logic
* Final recommendation generation
* Prompt engineering

### Workflow Integration

* Merge node handling
* JSON schema contracts
* Google Sheets storage
* End-to-end testing
* Error handling
* Output formatting

---

# Agentic Practices Demonstrated

## Clear Agent Roles

The workflow uses specialized agents with clearly defined responsibilities:

* Insight Agent: Restaurant metadata analysis and operational insights
* Review Agent: Review intelligence, dish extraction, and sentiment analysis
* Recommendation Agent: Final recommendation generation and scoring

## Structured Inputs and Outputs

* All agents use structured JSON schemas.
* Structured Output Parsers enforce consistent output formats.
* Agent outputs are merged and passed between workflow stages in a schema-driven manner.

## Tool and Integration Usage

The workflow integrates multiple external tools and services:

* Google Places Search API
* Google Place Details API
* Google Gemini models
* OpenAI GPT-4.1 Mini
* Google Sheets for persistent storage
* HTTP Request nodes for external data retrieval

## Branching and Routing Logic

The workflow includes conditional routing using IF nodes:

* Rejects restaurants with insufficient ratings or reviews.
* Routes valid restaurants through the intelligence and recommendation pipeline.
* Routes invalid cases to rejection responses.

## Deterministic Validation

The workflow applies rule-based validation before AI processing:

* Minimum review count thresholds.
* Place existence validation.
* Structured schema validation through output parsers.
* Recommendation scoring and confidence assessment.

## Fallback and Error Handling

The workflow includes fallback paths for:

* Restaurant not found scenarios.
* Insufficient review data.
* Rejected analysis requests that do not meet quality thresholds.

## Human-in-the-Loop Review

Not currently implemented in the workflow.
Potential future enhancement:

* Human review for low-confidence recommendations.
* Review queue for ambiguous or conflicting analysis results.
