# 1. Scheduling 5%

* Use label selectors to schedulePods
  * Ref: https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/
  * Sample: 
    *  kubectl label nodes node1 disktype=ssd
    *  kubectl get nodes --show-labels
    *  https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/
        * nodeSelector:
        * disktype: ssd
    *  kubectl get pods --output=wide
  * https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/#create-a-pod-that-gets-scheduled-to-specific-node
  
* Understand the role of DaemonSets
  * Ref: https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/
  Every Nodes run a daemonset

* Understand how resource limits can afect Pod scheduling.
  * Ref: https://kubernetes.io/docs/tasks/configure-pod-container/assign-cpu-resource/
  https://kubernetes.io/docs/tasks/configure-pod-container/assign-memory-resource/

* Understand how to run multiple schedulers and how to configure Pods
  * Ref: https://kubernetes.io/docs/tasks/administer-cluster/configure-multiple-schedulers/
  * set schedulerName=xxx in Pod spec

* Display scheduler events.
  * Sample: kubectl get events

* Know how to configure the Kubernetes scheduler.