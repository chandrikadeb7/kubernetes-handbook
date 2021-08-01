# Kinds of Controllers

## ReplicaSets

* Specified number of replica pods are running at all times
* Else will start a new pod when it crashes
* Used within deployment

## Deployments

* Declarative updates for pods and ReplicaSets
* Describe desired state of deployment in yaml file and deployment controller aligns actual state to match
* Create/replace replicaSets
* Deployments manages ReplicaSets which manages Pods \(quick and flexible rollback\)
* Use Cases
  * Pod Management
  * Scaling a ReplicaSet
  * Pod Updates/Rollbacks
  * Pause \(only updates are paused not traffic\) /Resume deployments \(larger change sets\)
  * Status - pod health issues

## Daemon Sets

* Ensures all nodes run a copy of the specific pod
* Add/remove pods according to add/remove nodes in cluster
* Deleting this deletes all pods it created
* Use Case
  * Log aggregator
  * Monitoring agent on node

## Jobs

* Supervisor for pods carrying out batch jobs
* Cron job - specific job at specific time
* Eg. nightly report, database backups etc.

## Services

* Allows communication btw sets of deployment with another
* Unique IP \(unchanging\)
* Pods configured to rely on service IP
* Allows 2 deployments \(set of pods\) to talk 
* Types:
  * Internal: IP reach within cluster
  * External: EP available through Node IP: port \(NodePort\)
  * Load balancer: K8s in cloud

