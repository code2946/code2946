# Aryan Saxena

**Backend and AI engineer.** B.Tech Computer Science, IIIT Nagpur, June 2026. Based in Pune, India — available immediately.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java%2017-E76F00?logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![OpenSearch](https://img.shields.io/badge/OpenSearch-005EB8?logo=opensearch&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)

Three internships so far, all of them shipping. At **Lumora** I built an LLM chat product with a
retrieval-backed memory layer, and owned the wallet and credits path behind it. At **Airtel
(Xtelify)** I built the document-extraction pipeline behind their AI Expense Chatbot — receipts and
meeting transcripts through an OCR-first LLM stage into Oracle EBS, replacing manual form-filling for
15,000+ employees at 95% data accuracy. Accuracy and throughput were instrumented and reported
upward, so it was a number rather than an opinion.

Most of what I do is the engineering around a model rather than the model itself: retrieval, the API
in front of it, the database behind it, and the deploy. These are the repos worth opening.

---

### [agentic-rag](https://github.com/saxena-aryan-dev/agentic-rag)

`Python` · `LangGraph` · `OpenSearch` · `FastAPI` · `PostgreSQL` · `Redis` · `Docker`

Answers questions about arXiv papers, with citations. Hybrid retrieval fuses BM25 and dense vectors
by Reciprocal Rank Fusion; a LangGraph agent grades its own retrieval and rewrites the query up to
twice before it generates. One `docker compose up`, healthcheck-gated, seeded straight from the arXiv
API.

### [payment-authorization-switch](https://github.com/saxena-aryan-dev/payment-authorization-switch)

`Java 17` · `Spring Boot 3` · `PostgreSQL` · `Docker` · `GitHub Actions`

A card authorization switch — the component at the centre of a payment network. The ISO 8583 codec is
hand-written: message type indicator, 64-bit primary bitmap, `FIXED` / `LLVAR` / `LLLVAR` data
elements. Luhn, expiry and limit checks map to standard field-39 response codes, PANs are masked
before they reach storage, and every transaction is persisted. An acquirer's `0100` comes back as a
`0110` in one synchronous call. Tested with JUnit 5, Mockito, AssertJ and MockMvc against H2; CI
holds the build to a 60% coverage gate.

### [screenonfire](https://github.com/saxena-aryan-dev/screenonfire)

`Next.js 14` · `TypeScript` · `Supabase` · `TMDB`

Movie discovery, running live. Pick a few films you like and it builds a feature profile out of their
genres, cast, directors, ratings and release years, then scores the catalog against it by weighted
similarity — with the weights exposed as sliders, so you can decide that director matters more than
genre and watch the list move.

### [lexer](https://github.com/saxena-aryan-dev/lexer)

`C++`

Tokenizer for C/C++ source. Classifies keywords, identifiers, operators, literals, preprocessor
directives and comments, and reports the failures a real compiler front-end has to survive:
unterminated strings, unterminated block comments, malformed numeric literals.

### [otp-auth-android](https://github.com/saxena-aryan-dev/otp-auth-android)

`Kotlin` · `Jetpack Compose`

Passwordless email and OTP authentication. Generation and validation with expiry and attempt limits,
a live session timer, sealed classes for UI state.

---

**Certification** — [IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/account/accomplishments/professional-cert/FX8SRL9459H9), August 2026. Ten courses: RAG, vector databases, multimodal generative AI, LangChain and LangGraph agents, MCP.

**Reach me** — [saxena.aryan.dev@gmail.com](mailto:saxena.aryan.dev@gmail.com) · [LinkedIn](https://www.linkedin.com/in/saxena-aryan-dev) · [LeetCode](https://leetcode.com/u/iamcodezero1)
