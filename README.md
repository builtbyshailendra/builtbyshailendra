# Hi, I'm Shailendra

I build Python automation, full-stack features and the cloud setup that runs them.
I'm working toward forward deployed engineering: understand a team's workflow, build the fix, and make the result easy to check.

### What I'm building now

Small personal learning projects on synthetic data, one step at a time.
Each repo keeps a short build log: what I built, what broke, what I learned.

| Project | What it does | Status |
|---|---|---|
| 🏥 [prior-auth-workbench](https://github.com/builtbyshailendra/prior-auth-workbench) | Prior-authorization intake for a fictional health plan. FHIR, X12 278, fax and CRM requests become one queue; AI pulls checklist facts from clinical notes and every quote is checked against the source; nurses and medical directors decide on CMS's 72-hour / 7-day clocks. Discovery pack, business case and Kubernetes drills included | ✅ Working |
| 📄 [doc-intake-pipeline](https://github.com/builtbyshailendra/doc-intake-pipeline) | Emailed PDF invoices in, clean SQL rows and a one-page report out. Flags duplicates, impossible dates and totals that don't add up | ✅ Working |
| 🧪 [iac-check-kit](https://github.com/builtbyshailendra/iac-check-kit) | Reads Terraform and flags S3 buckets that can go public and SSH open to the internet. Passes a safe setup however it's written, and says "can't tell" instead of guessing | ✅ Working |
| 🛠️ [serviceops-workbench](https://github.com/builtbyshailendra/serviceops-workbench) | Next.js + FastAPI + PostgreSQL. A service request goes from intake to a human-approved action, with an audit trail the database won't let anyone edit | ✅ Working |
| 🚀 [deploy-baseline](https://github.com/builtbyshailendra/deploy-baseline) | Runs serviceops-workbench in Docker, compose and Kubernetes, with Prometheus and Grafana. On every push, CI deploys a broken release to a real cluster and checks it's rolled back without a single failed call | ✅ Working |

### Learning new tech, one project at a time

Built in November 2026, pairing with Claude Code, to learn each technology from the inside. Every repo has a build log with measured numbers, what broke, and `LEARN.md` notes.

| Project | What it does |
|---|---|
| 🗄️ [lakehouse](https://github.com/builtbyshailendra/lakehouse) | Apache Iceberg tables with a PostgreSQL catalog, read by DuckDB. Loads survive crashes and racing writers; bad files wait on a branch until checks pass |
| ⏱️ [minitsdb](https://github.com/builtbyshailendra/minitsdb) | A small Prometheus-style time-series database: compression, write-ahead log, compaction, and PromQL answers checked against Prometheus's own engine |
| 📒 [event-ledger](https://github.com/builtbyshailendra/event-ledger) | Transfers with a transactional outbox and NATS JetStream: every event published once and applied once, even with processes killed mid-way |
| 🗳️ [raft-kv](https://github.com/builtbyshailendra/raft-kv) | A key-value store on etcd's Raft library, tested by simulating partitions, crashes and clock drift, and checked for linearizability |
| 🖥️ [react-ops-console](https://github.com/builtbyshailendra/react-ops-console) | Incident console: Protobuf API contract, ConnectRPC on Node, React with live updates and safe concurrent edits |
| 🔭 [otel-pipeline](https://github.com/builtbyshailendra/otel-pipeline) | OpenTelemetry end to end: a custom Collector that scrubs card numbers and tokens, and tail sampling that keeps every error trace |
| 🐘 [sql-performance-lab](https://github.com/builtbyshailendra/sql-performance-lab) | PostgreSQL on 25 million rows: slow queries made fast with the right index or rewrite, and two production incidents reproduced |
| 📝 [local-first-notes](https://github.com/builtbyshailendra/local-first-notes) | Incident notes that work offline and merge everyone's edits without conflicts (Yjs CRDTs, own sync server) |
| 🧩 [wasm-sandbox](https://github.com/builtbyshailendra/wasm-sandbox) | Runs untrusted WebAssembly plugins with no file, network or clock access by default, and hard limits on time and memory |
| 🧯 [drill-operator](https://github.com/builtbyshailendra/drill-operator) | A Kubernetes operator that runs chaos drills safely: validated custom resource, crash-safe steps, puts back what it changed |
| 🔁 [durable-agent](https://github.com/builtbyshailendra/durable-agent) | An incident-remediation agent run that survives crashes and waits for a human's approval, on DBOS durable workflows |
| 🛡️ [mcp-gate](https://github.com/builtbyshailendra/mcp-gate) | A policy gate for AI agents' tool calls (MCP): Cedar policies decide which agent may call which tool, and where |

### Stack I work with

Python, TypeScript, React / Next.js, PostgreSQL, Docker, AWS, Kubernetes, Terraform, GitHub Actions. Healthcare data: HL7 FHIR R4, X12 278.

### Certifications earned

- Certified Kubernetes Administrator (CKA), The Linux Foundation
- Red Hat Certified System Administrator (RHCSA), Red Hat

### Find me

LinkedIn: [shailendra-singh-devops](https://www.linkedin.com/in/shailendra-singh-devops/)
