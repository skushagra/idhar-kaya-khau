# Idhar Kya Khau

An AI-powered restaurant intelligence and recommendation system built using n8n, Google Places APIs, Gemini, and OpenAI.

The workflow analyzes restaurant metadata and customer reviews to generate actionable dining recommendations, identify must-try dishes, evaluate risks, and provide restaurant insights.

---

# Problem Statement

Choosing where to eat often requires manually browsing ratings, reviews, and recommendations across multiple platforms.

Idhar Kya Khau automates this process by:

* Collecting restaurant information from Google Places
* Analyzing customer reviews using AI agents
* Extracting dishes, themes, and service insights
* Generating recommendation scores and dining suggestions
* Persisting restaurant intelligence for future reference

---

# Workflow Architecture

```text
User Query
    ↓
Google Places Search
    ↓
Place Details API
    ↓
 ┌──────────────┬──────────────┐
 │              │
 ▼              ▼
Insight Agent   Review Agent
 │              │
 └───────┬──────┘
         ↓
       Merge
         ↓
Recommendation Agent
         ↓
Google Sheets Storage
```

---

# Agents

## Insight Agent

Analyzes restaurant metadata and operational information.

Outputs:

* Restaurant profile
* Service information
* Restaurant categories
* Customer fit insights
* Operational observations

---

## Review Agent

Analyzes customer reviews and extracts review intelligence.

Outputs:

* Must-try dishes
* Positive themes
* Negative themes
* Service observations
* Crowd insights
* Review summary

---

## Recommendation Agent

Combines restaurant metadata and review intelligence to generate the final recommendation.

Outputs:

* Recommendation category
* Match score
* Confidence score
* Top strengths
* Potential risks
* Best time to visit

---

# Technologies Used

* n8n
* Google Places Search API
* Google Place Details API
* Google Gemini
* OpenAI GPT-4.1 Mini
* Google Sheets

---

# Agentic Practices Demonstrated

## Clear Agent Roles

The workflow consists of specialized agents with distinct responsibilities:

* Insight Agent
* Review Agent
* Recommendation Agent

## Structured Outputs

* Schema-based agent outputs
* Structured Output Parsers
* Consistent JSON communication between agents

## Tool Usage

The workflow integrates multiple external systems:

* Google Places APIs
* HTTP Requests
* Google Sheets
* Gemini Models
* OpenAI Models

## Branching and Routing

Conditional routing is implemented using validation and threshold checks:

* Restaurant existence validation
* Minimum review count validation
* Conditional workflow progression

## Deterministic Validation

Rule-based checks are applied before AI-driven analysis:

* Place validation
* Review threshold checks
* Structured output validation

## Fallback and Error Handling

The workflow includes dedicated fallback paths for:

* Restaurant not found
* Insufficient review data
* Invalid analysis requests

## Human-in-the-Loop

Not currently implemented.

Potential extension:

* Manual approval of low-confidence recommendations
* Human review before persistence
* Quality assurance workflows

---

# Future Enhancements

* Human approval workflows
* Vector database for restaurant memory
* Multi-platform review aggregation
* Personalized recommendations
* Restaurant comparison assistant
* Cuisine-specific recommendation engine
* Retrieval-based restaurant memory system
