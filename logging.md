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

 * Manage application logs