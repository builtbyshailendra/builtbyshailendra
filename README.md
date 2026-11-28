# Hi, I'm Shailendra 👋

**Cloud, SRE and DevOps engineer** · AWS · Azure · GCP · Kubernetes · Terraform · Python · Go<br>
Certified Kubernetes Administrator (CKA) · Red Hat Certified System Administrator (RHCSA)

I work on the platform under a product: Kubernetes, Terraform, CI/CD, observability and cloud cost.
I also build the product itself when a team needs it end to end, and I test it the way production breaks it: crashed releases, database outages, network partitions.
I'm moving toward forward deployed engineering: understand a team's workflow, build the fix, and make the result easy to check.

## ⭐ Featured projects

<table>
<tr>
<td width="50%" valign="top">

### 🤖 [field-copilot](https://github.com/builtbyshailendra/field-copilot)

One AI copilot platform deployed for two fictional customers: an on-call copilot that investigates Kubernetes incidents and proposes fixes a person approves, and a policy copilot for nurses whose every quote is checked against the source.

- Retrieval MRR 0.87–0.88 on 48 labelled questions (hybrid search + reranker)
- Releases go out as Argo Rollouts canaries, promoted only if a quality self-check passes (healthy build 0.83, broken build 0.48)
- Found that the usual 0.90 cache threshold would give 5 of 13 look-alike questions the wrong answer; shipped 0.98 in shadow mode

<sub>Python · FastAPI · pgvector · Next.js · Helm · Argo CD · Terraform · AWS Bedrock</sub>

</td>
<td width="50%" valign="top">

### 🏥 [prior-auth-workbench](https://github.com/builtbyshailendra/prior-auth-workbench)

Prior-authorization intake for a fictional health plan, run like a customer deployment: a discovery pack with 33 requirements first, then the product.

- FHIR R4, X12 278, fax and CRM requests become one queue, sorted by CMS's 72-hour / 7-day deadlines
- AI pulls checklist facts from clinical notes, every quote is checked against the source, and only people decide
- 194 automated tests; CI rolls back a crashing release on Kubernetes with 327 calls and 0 failures

<sub>Python · PostgreSQL · TypeScript · HL7 FHIR R4 · X12 278 · Kubernetes · Playwright</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🚀 [deploy-baseline](https://github.com/builtbyshailendra/deploy-baseline)

A full-stack app taken to Docker, Compose and Kubernetes with Prometheus and Grafana, and proved again on every push.

- CI deploys a release that crashes on startup to a real kind cluster; it's rolled back with 331 calls and 0 failures
- Database stopped mid-run: the backend goes not-ready with 0 pod restarts
- Backup and restore checked in CI; all 8 dashboard queries run against Prometheus

<sub>Docker · Kubernetes · kind · Prometheus · Grafana · GitHub Actions · GHCR</sub>

</td>
<td width="50%" valign="top">

### 🗳️ [raft-kv](https://github.com/builtbyshailendra/raft-kv)

A replicated key-value store on etcd's Raft library, tested by deterministic simulation: one seed controls every delay and fault, so any failure replays exactly.

- 470,326 operations across 1,250 fault-injected runs, all linearizable (checked with Porcupine)
- 7 planted bugs, every one caught
- Lease-based reads went stale in 41 of 200 targeted runs even with equal clocks; ReadIndex reads in 0 of 200

<sub>Go · etcd raft · deterministic simulation · Porcupine</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🛡️ [mcp-gate](https://github.com/builtbyshailendra/mcp-gate)

A policy gateway between AI agents and their tools (MCP): every tool call is checked against Cedar policies, deny by default, and the agent is told why.

- Policy decision in 8–20 µs; about 0.5–1 ms added per tool call
- Refuses 12 tricks that two JSON parsers could read differently; none reaches the tool server
- Differential fuzzing found 2 real bugs, both fixed

<sub>Go · Cedar · MCP · JSON-RPC · Go fuzzing</sub>

</td>
<td width="50%" valign="top">

### 🗄️ [lakehouse](https://github.com/builtbyshailendra/lakehouse)

Apache Iceberg tables with a PostgreSQL catalog, read by DuckDB, tested by killing loaders mid-commit and racing writers.

- 30 random kills and six racing writers: never a partial or doubled day
- 92 of 92 snapshots identical in DuckDB and the source data, to the micro-dollar
- Write-audit-publish branches quarantined all 6 kinds of bad export; 27 of 27 injected incidents found

<sub>Python · Apache Iceberg · PyIceberg · PostgreSQL · DuckDB · Parquet</sub>

</td>
</tr>
</table>

## More projects

#### ☁️ Cloud, infrastructure as code and cost

| Project | What it does |
|---|---|
| 🌊 [driftwatch](https://github.com/builtbyshailendra/driftwatch) | Terraform drift detection from plan JSON in Go, with Markdown and JSON reports, GitHub issue and Slack outputs, and a GitHub Action |
| 💸 [aws-cost-sentinel](https://github.com/builtbyshailendra/aws-cost-sentinel) | Finds AWS cost waste (idle, oversized and orphaned resources) with dollar estimates, from a Cost Explorer CSV or a read-only scan tested against moto |
| 🧪 [iac-check-kit](https://github.com/builtbyshailendra/iac-check-kit) | Reads Terraform and flags S3 buckets that can go public and SSH open to the internet; says "can't tell" instead of guessing |

#### ⚙️ Platform, reliability and agents

| Project | What it does |
|---|---|
| 🧯 [drill-operator](https://github.com/builtbyshailendra/drill-operator) | A Kubernetes operator that runs chaos drills safely: validated custom resource, crash-safe steps, puts back what it changed |
| 🔭 [otel-pipeline](https://github.com/builtbyshailendra/otel-pipeline) | OpenTelemetry end to end: a custom Collector that scrubs card numbers and tokens, and tail sampling that keeps every error trace |
| 🔁 [durable-agent](https://github.com/builtbyshailendra/durable-agent) | An incident-remediation agent run that survives crashes and waits for a human's approval, on DBOS durable workflows |
| 🧩 [wasm-sandbox](https://github.com/builtbyshailendra/wasm-sandbox) | Runs untrusted WebAssembly plugins with no file, network or clock access by default, and hard limits on time and memory |

#### 🗃️ Distributed systems and data

| Project | What it does |
|---|---|
| 📒 [event-ledger](https://github.com/builtbyshailendra/event-ledger) | Transfers with a transactional outbox and NATS JetStream: every event published once and applied once, even with processes killed mid-way |
| ⏱️ [minitsdb](https://github.com/builtbyshailendra/minitsdb) | A small Prometheus-style time-series database: compression, write-ahead log, compaction, and PromQL answers checked against Prometheus's own engine |
| 🐘 [sql-performance-lab](https://github.com/builtbyshailendra/sql-performance-lab) | PostgreSQL on 25 million rows: slow queries made fast with the right index or rewrite, and two production incidents reproduced |
| 🧳 [fde-data-migration-kit](https://github.com/builtbyshailendra/fde-data-migration-kit) | Onboards a customer's legacy CSV and Excel data: profile, map in one YAML file, validate, deduplicate, dry-run diff, load idempotently and reconcile |

#### 🖥️ Full-stack and automation

| Project | What it does |
|---|---|
| 🛠️ [serviceops-workbench](https://github.com/builtbyshailendra/serviceops-workbench) | Next.js + FastAPI + PostgreSQL. A service request goes from intake to a human-approved action, with an audit trail the database won't let anyone edit |
| 🖥️ [react-ops-console](https://github.com/builtbyshailendra/react-ops-console) | Incident console: Protobuf API contract, ConnectRPC on Node, React with live updates and safe concurrent edits |
| 📝 [local-first-notes](https://github.com/builtbyshailendra/local-first-notes) | Incident notes that work offline and merge everyone's edits without conflicts (Yjs CRDTs, own sync server) |
| 📄 [doc-intake-pipeline](https://github.com/builtbyshailendra/doc-intake-pipeline) | Emailed PDF invoices in, clean SQL rows and a one-page report out; flags duplicates, impossible dates and totals that don't add up |

#### 🔩 Engineering simulation (BTech, Electrical Engineering)

| Project | What it does |
|---|---|
| 🔩 [cad-to-fea](https://github.com/builtbyshailendra/cad-to-fea) | A bracket from CAD to stress: modelled in CadQuery and build123d, meshed with Gmsh, solved in CalculiX and FEniCSx, and checked against beam theory |
| ⚙️ [motor-control-three-ways](https://github.com/builtbyshailendra/motor-control-three-ways) | One motor speed controller designed in python-control, built as an op-amp circuit in ngspice and as a physical model in OpenModelica; all three agree within 0.002% |
| 🔥 [flame-to-flow](https://github.com/builtbyshailendra/flame-to-flow) | Methane flames in Cantera, then the hot exhaust through a duct in OpenFOAM, checked against published data and channel-flow theory |

## How I work

Every repo keeps a build log: what I built, what broke, and what I measured and how.
Data is synthetic and customers are fictional.
Every project is held to the bar of a teammate's pull request: tests, CI on every push, and numbers I can reproduce.

## Stack

- **Cloud:** AWS, Azure, GCP
- **Containers and delivery:** Docker, Kubernetes, Helm, Argo CD, Argo Rollouts, GitHub Actions
- **Infrastructure as code:** Terraform
- **Observability:** Prometheus, Grafana, OpenTelemetry
- **Languages:** Python, Go, TypeScript, SQL
- **Data:** PostgreSQL, DuckDB, Apache Iceberg, NATS JetStream
- **Healthcare data:** HL7 FHIR R4, X12 278

## Find me

LinkedIn: [shailendra-singh-devops](https://www.linkedin.com/in/shailendra-singh-devops/)
