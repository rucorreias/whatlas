# Whatlas

> **Explore history through the questions that connect it.**

**What. Why. When. Who. Where. What's next.**

Whatlas is an open-source project for exploring the history of the world through interconnected facts, events, people, places, organisations and timelines.

The idea is to make history explorable through six fundamental questions:

* **What?** — What happened?
* **Why?** — Why did it happen?
* **When?** — When did it happen?
* **Who?** — Who was involved?
* **Where?** — Where did it happen?
* **What's next?** — What happened afterwards?

Instead of treating historical information as isolated facts, Whatlas aims to build a connected map of history that can be explored, searched and eventually queried using AI.

---

## The Six Questions

The six questions are the foundation of Whatlas.

### What?

**What happened?**

Events, discoveries, wars, revolutions, inventions, treaties, political changes, cultural events and other historical facts.

---

### Why?

**Why did it happen?**

Context, causes, motivations, circumstances and consequences surrounding an event.

---

### When?

**When did it happen?**

Dates, periods, chronology and relationships between events across time.

---

### Who?

**Who was involved?**

People, rulers, scientists, organisations, countries, populations, dynasties and other historical entities.

---

### Where?

**Where did it happen?**

Locations, regions, countries, cities and geographical contexts connected to historical events.

---

### What's next?

**What happened afterwards?**

Consequences, reactions, developments and subsequent events.

This question is particularly important to Whatlas because it allows history to be explored as a chain of connected events rather than a collection of isolated facts.

```text
Event A
   │
   ├── consequence
   ▼
Event B
   │
   ├── consequence
   ▼
Event C
   │
   └── ...
```

The goal is to make it possible to move naturally through these connections.

---

## Vision

The long-term goal of Whatlas is to create a large, structured and interconnected knowledge base of human history.

Imagine starting with:

> **The French Revolution**

and exploring:

```text
French Revolution
│
├── What?
│   ├── Revolution in France
│   ├── Storming of the Bastille
│   ├── Declaration of the Rights of Man
│   └── Reign of Terror
│
├── Why?
│   ├── Economic crisis
│   ├── Social inequality
│   ├── Political conflict
│   └── Enlightenment ideas
│
├── When?
│   └── 1789–1799
│
├── Who?
│   ├── Louis XVI
│   ├── Marie Antoinette
│   ├── Maximilien Robespierre
│   └── ...
│
├── Where?
│   └── France
│
└── What's next?
    ├── Rise of Napoleon
    ├── Napoleonic Wars
    └── Political transformation of Europe
```

The same people, places and events should then connect to other parts of history.

The goal is not simply to store more information.

The goal is to make **connections between information explorable**.

---

## Project Goals

Whatlas aims to:

* 🌍 Explore history from a global perspective
* 🧩 Connect historical events, people, places and organisations
* 📅 Explore history by date and period
* 🗺️ Explore the geographical context of historical events
* 🔎 Search historical information
* 🕸️ Build a connected knowledge graph
* 🔗 Follow chains of historical events and consequences
* 📚 Preserve references to original sources
* 🌐 Support multiple languages
* 🤖 Eventually use AI to help explore the knowledge base
* 💻 Serve as a practical project for learning modern software development

---

## Core Concept

At the heart of Whatlas is the idea that a historical event should not exist as an isolated record.

Instead, it should be connected to its context.

```text
                         ┌─────────────┐
                         │    WHAT?    │
                         │ What was it?│
                         └──────┬──────┘
                                │
              ┌─────────────────┼─────────────────┐
              ▼                 ▼                 ▼
         ┌─────────┐       ┌─────────┐       ┌─────────┐
         │  WHY?   │       │  WHEN?  │       │  WHO?   │
         │  Why?   │       │ When?   │       │ Who?    │
         └────┬────┘       └────┬────┘       └────┬────┘
              │                 │                 │
              └─────────────────┼─────────────────┘
                                ▼
                         ┌─────────────┐
                         │   WHERE?    │
                         │    Where?   │
                         └──────┬──────┘
                                │
                                ▼
                       ┌────────────────┐
                       │ WHAT'S NEXT?   │
                       │   What next?   │
                       └───────┬────────┘
                               │
                               ▼
                         Another Event
```

This model can be applied to anything from a single historical event to an entire period of history.

---

## Architecture

Whatlas is planned as a full-stack application.

```text
┌─────────────────────┐
│      Next.js        │
│      Frontend       │
└──────────┬──────────┘
           │
           │ REST API
           ▼
┌─────────────────────┐
│      FastAPI        │
│       Backend       │
└──────────┬──────────┘
           │
     ┌─────┼──────────────┐
     │     │              │
     ▼     ▼              ▼
 Database  External APIs  AI
     │
     ▼
Knowledge Graph
```

### Frontend

Planned technologies:

* Next.js
* React
* TypeScript
* Tailwind CSS
* shadcn/ui

The frontend will be responsible for presenting and exploring the information.

### Backend

Planned technologies:

* Python
* FastAPI
* Pydantic
* HTTPX
* PostgreSQL
* SQLAlchemy
* Alembic

The backend will be responsible for:

* retrieving data
* normalising data
* validating data
* deduplicating information
* storing historical data
* connecting entities
* exposing the API
* managing external sources
* preparing data for future AI features

---

## Data Sources

The project is intended to combine information from multiple public sources and APIs.

Potential sources include:

* On This Day API
* MediaWiki API
* HistoryLabs Events API
* Wikidata
* Alpha Vantage
* NOAA Climate Data Online
* Other public datasets and historical sources

External information should not simply be copied into Whatlas.

The backend should transform different sources into a common internal data model while preserving the original source and references.

---

## Knowledge Graph

One of the long-term goals is to transform the collected information into a connected knowledge graph.

For example:

```text
                ┌──────────────┐
                │    France    │
                └──────┬───────┘
                       │
                    location
                       │
                       ▼
              ┌─────────────────┐
              │ French Revolution│
              └───────┬─────────┘
                      │
          ┌───────────┼────────────┐
          │           │            │
          ▼           ▼            ▼
       involved      caused      followed
          │           │            │
          ▼           ▼            ▼
      Louis XVI   Economic      Rise of
                   Crisis       Napoleon
```

Entities may eventually include:

* People
* Places
* Countries
* Organisations
* Events
* Wars
* Dynasties
* Empires
* Discoveries
* Inventions
* Political movements
* Treaties
* Books
* Scientific concepts
* Cultural events

Relationships may include:

* happened at
* happened during
* involved
* caused
* influenced
* preceded
* followed
* succeeded
* participated in
* located in
* related to

The graph should allow users to move naturally from one subject to another.

---

## AI

AI is a future layer of Whatlas, not the foundation of its knowledge.

The intended architecture is:

```text
Sources
   ↓
Structured data
   ↓
Validated knowledge
   ↓
Knowledge graph
   ↓
Retrieval
   ↓
AI
```

The AI should use the project's structured information and retrieved sources to help users explore history.

Possible future features include:

* Natural-language questions
* Historical explanations
* Entity discovery
* Automatic relationship suggestions
* Summaries
* Timeline generation
* Semantic search
* Retrieval-Augmented Generation (RAG)

A key principle is:

> **The LLM should help explore the knowledge base, not become the knowledge base.**

AI-generated information should remain connected to sources and be treated as a layer over the underlying data.

---

## Multilingual

Whatlas is intended to support multiple languages.

The initial focus will be:

* 🇵🇹 Portuguese
* 🇬🇧 English

The architecture should allow additional languages to be introduced later without duplicating the underlying historical entities.

For example:

```text
Entity
  │
  ├── Portuguese name
  ├── English name
  ├── Other names
  └── Wikidata / external identifiers
```

This allows the same historical entity to be explored in different languages.

---

## Planned Features

### MVP

* [ ] Next.js frontend
* [ ] FastAPI backend
* [ ] `/health` endpoint
* [ ] Backend ↔ frontend communication
* [ ] Historical events API integration
* [ ] Search by date
* [ ] Event cards
* [ ] Event details
* [ ] Source references
* [ ] Loading and error states
* [ ] Responsive interface

### Phase 2 — Data

* [ ] PostgreSQL
* [ ] Persistent events
* [ ] Data normalisation
* [ ] Deduplication
* [ ] Caching
* [ ] Source management
* [ ] Automated data ingestion
* [ ] Tests

### Phase 3 — Knowledge Graph

* [ ] Wikidata integration
* [ ] Entity model
* [ ] Relationships
* [ ] People pages
* [ ] Place pages
* [ ] Organisation pages
* [ ] Historical timelines
* [ ] Graph visualisation
* [ ] Event chains

### Phase 4 — AI

* [ ] Local LLM experimentation
* [ ] Embeddings
* [ ] Semantic search
* [ ] RAG
* [ ] Source-aware answers
* [ ] AI-assisted entity extraction
* [ ] AI-assisted relationship discovery

### Phase 5 — Exploration

* [ ] Interactive world map
* [ ] Advanced timelines
* [ ] Knowledge graph exploration
* [ ] Historical comparisons
* [ ] Cross-period exploration
* [ ] Natural-language search
* [ ] Conversational history explorer

---

## Development Philosophy

Whatlas is also a learning project.

The development process is intentionally incremental.

Rather than starting with a complex architecture, the project will evolve through small working steps:

```text
Next.js
   ↓
FastAPI
   ↓
External API
   ↓
Normalised data
   ↓
Database
   ↓
Entities
   ↓
Relationships
   ↓
Knowledge graph
   ↓
AI / RAG
```

Each stage should produce something usable before the next layer is introduced.

---

## Learning Goals

The project is being developed with the following learning objectives.

### Frontend

* React fundamentals
* Next.js
* TypeScript
* Component architecture
* State management
* API consumption
* Responsive UI
* Data visualisation

### Backend

* Python
* FastAPI
* REST APIs
* Pydantic
* HTTP clients
* Databases
* SQL
* Testing
* Background processing

### Data

* Data modelling
* Normalisation
* Deduplication
* Entity resolution
* Knowledge graphs
* Graph relationships
* Search

### AI / ML

* Embeddings
* Vector search
* Local LLMs
* RAG
* Information extraction
* Evaluation
* Source grounding

---

## Repository Structure

The project is planned as a monorepo:

```text
whatlas/
├── frontend/
├── backend/
├── docs/
│
├── README.md
├── .gitignore
└── docker-compose.yml
```

---

## Data Principles

Whatlas should prioritise:

**Sources over assumptions.**

**Structured data over unverified text.**

**Connections over isolated facts.**

**Transparency over black-box answers.**

**Incremental development over premature complexity.**

When possible, historical information should retain:

* Original source
* Source URL
* External identifier
* Publication information
* Date information
* Confidence / quality metadata
* Relationships to other entities

---

## Status

🚧 **Early development**

Whatlas is currently in the initial setup phase.

The first objective is to establish a working pipeline:

```text
Next.js
   ↓
FastAPI
   ↓
JSON
   ↓
Next.js
```

Once that foundation is stable, historical data sources and persistent storage will be introduced incrementally.

---

## Contributing

The project is currently primarily a personal learning and portfolio project.

As the project matures, contribution guidelines will be added.

Ideas, discussions and improvements are welcome.

---

## License

License information will be added as the project matures.

---

## Name

### Whatlas

**What + Atlas**

**What** represents questions, facts and events.

**Atlas** represents exploration, geography, connections and a map of knowledge.

Together:

> **Whatlas — an atlas of history explored through questions.**

### The Whatlas Questions

> **What. Why. When. Who. Where. What's next.**
