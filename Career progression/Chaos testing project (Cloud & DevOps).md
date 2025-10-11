<b>What is chaos testing?</b>
Chaos testing is injecting failures into a systems and observing its behaviours whilst under stress. The goal is to identify weaknesses and build confidence in the systems resilience.

Project layers
- Application
	- Basic service (node.js)
	- Containerised in Docker
- Orchestration
	- Kubernetes
- Chaos
	- Chaos mesh
- Monitoring
	- Prometheus & Grafana
	- Alerts


<b>Application</b>
REST API To-Do application

<i>Create - List - Delete</i>

Postgres in <font color="blue">container</font>

Orchestrated with Kubernetes

<b>Observability</b>
Prometheus (request count, error rate, latency)

Grafana dashboard (uptime, latency, error %)

<b>Chaos</b>
- Pod kill
	- Randomly kill the API pod - K8s should reschedule it.
- Network latency
	- Inject 2s delay between API and DB.
- DB pod failure
	- Kill the postgres pod, watch recovery/ failover.
- Resources stress
	- Fill CPU or memory to simulate load.

<b>Resilience patterns</b>
- Health checks/ readiness probes in K8s
- Configure auto-scaling with HPA (horizontal pod autoscaler)
- Use a catching layer (Redis) to reduce DB dependency
- Implement circuit breaker into API

<b>Report results</b>
Documentation
- What chaos tests where ran
- What broke
- How they were fixed/ addressed
- Before & after dashboards from Grafana.

