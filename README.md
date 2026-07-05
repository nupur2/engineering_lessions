Engineering Lessons & Production Findings

This repository captures technical findings, production learnings, debugging notes, and design lessons from backend engineering work across Java, Spring Boot, Kafka, databases, and platform operations.

The goal is to document not just the fix, but also the reasoning, trade-offs, root cause, and long-term lesson behind each issue.

Topics Covered

* Kafka consumer behavior, rebalancing, and poll configuration
* Retry handling and failure recovery patterns
* Dependency vulnerability remediation challenges
* Database timeout handling and HikariCP behavior
* OpenShift / HPA scaling observations
* API contract design and uniqueness constraints
* Production debugging learnings and implementation trade-offs

Lessons Index

Kafka / Messaging

* Lesson 1 – Kafka Consumer Rebalance Due to Long Processing Time
* Lesson 2 – max.poll.interval.ms vs max.poll.records Trade-off
* Lesson 10 – Scheduler vs Consumer Poll Design

Security / Dependency Management

* Lesson 5 – Excluding a Vulnerable Dependency Isn’t Always a Fix

Database / Performance / Timeout Handling

* Lesson 3 – Why setQueryTimeout May Not Be Enough with HikariCP
* Lesson 9 – Database Lock Timeout vs Socket Timeout in Long-Running Calls

Reliability / Retry / Failure Analysis

* Lesson 6 – Retry Logic Can Succeed in Code but Still Fail Operationally
* Lesson 7 – Idempotency and Duplicate Request Handling in APIs

API / Design / Contracts

* Lesson 8 – API Contract Assumptions Can Break Cancellation Flow Design

Platform / Infrastructure

* Lesson 4 – HPA Scaling Changes Don’t Always Reduce Pod Count Immediately
