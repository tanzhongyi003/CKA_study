# 1. Scheduling 5%
https://cka-exam.blog/scheduling-5/


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
  * Run a pod on every Nodes of a cluster
  * Pods managed by DaemonSets bypass the scheduler

* Understand how resource limits can afect Pod scheduling
  * Ref: https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/memory-default-namespace/
  * Ref: https://kubernetes.io/docs/tasks/configure-pod-container/assign-cpu-resource/
  * Ref: https://kubernetes.io/docs/tasks/configure-pod-container/assign-memory-resource/

* Understand how to run multiple schedulers and how to configure Pods
  * Ref: https://kubernetes.io/docs/tasks/administer-cluster/configure-multiple-schedulers/
  * set schedulerName=xxx in Pod spec

* Manually schedule a pod without a scheduler
  * Ref: https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/

* Display scheduler events.
  * Sample: kubectl describe /kubectl get events/kubectl get evnt

* Know how to configure the Kubernetes scheduler.
  * taints - applies to nodes
    * master node typically has a taint of node-role.kubernetes.io/master:NoSchedule
  * tolerations:
    * apply to pods; to deploy to a node, they need to tolerate the taint
  * node selectors
  * pod affinity
    *  determine where pods are placed in respect to one another
  * pod anti-affinity
    *  determine where pods are not placed in respect to one another

 