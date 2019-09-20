# Logging/Monitoring 5%
https://cka-exam.blog/logging-monitoring-5/


 * Understand how to monitor all cluster components.
   * Monitor Node Health https://kubernetes.io/docs/tasks/debug-application-cluster/monitor-node-health/
   * Tools for monitoring Resources https://kubernetes.io/docs/tasks/debug-application-cluster/resource-usage-monitoring/
     *  kubectl top node
     *  kubectl top pod

 * Understand how to monitor applications.
 https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-probes/
   * liveness probes - periodically executed and container restarted if probe fail
   * readiness probes - periodically executed and determines if pod is read to receive client requests
   * liveness probes will start a new pod if check failed( pod's restartPolicy need to set Always or OnFailure ), readiness probes will remove the node from the services if check failed

 * Manage cluster component logs.
   * Master
     * /var/log/kube-apiserver.log - API Server, responsible for serving the API
     * /var/log/kube-scheduler.log - Scheduler, responsible for making scheduling decisions
     * /var/log/kube-controller-manager.log - Controller that manages replication controllers

   * Worker Nodes
     * /var/log/kubelet.log - Kubelet, responsible for running containers on the node
     * /var/log/kube-proxy.log - Kube Proxy, responsible for service load balancing

 * Manage application logs
 https://kubernetes.io/docs/concepts/cluster-administration/logging/
   * Basic logging in Kubernetes
     * kubectl logs pod xxx
   * Logging at the node level
   * Cluster-level logging architecture
     * Use a node-level logging agent that runs on every node.
     * Include a dedicated sidecar container for logging in an application pod.
     * Push logs directly to a backend from within an application.
  