# Troubleshotting  12%
https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application-introspection/

 * Troubleshoot application failure.
   https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application/

 * Troubleshoot control plane failure.
   https://kubernetes.io/docs/tasks/debug-application-cluster/debug-cluster/

 * Troubleshoot worker node failure.
   https://kubernetes.io/docs/tasks/debug-application-cluster/debug-cluster/

 * Troubleshoot networking
   * Troubleshooting services
     * Make sure you’re connecting to the service’s cluster IP from within the cluster, not from the outside.
     * Don’t bother pinging the service IP to figure out if the service is accessible (remember, the service’s cluster IP is a virtual IP and pinging it will never work).
     * If you’ve defined a readiness probe, make sure it’s succeeding; otherwise the pod won’t be part of the service.
     * To confirm that a pod is part of the service, examine the corresponding Endpoints object with kubectl get endpoints.
     * If you’re trying to access the service through its FQDN or a part of it (for example, myservice.mynamespace.svc.cluster.local or myservice.mynamespace) and it doesn’t work, see if you can access it using its cluster IP instead of the FQDN.
     * Check whether you’re connecting to the port exposed by the service and not the target port.
     * Try connecting to the pod IP directly to confirm your pod is accepting connections on the correct port.
     * If you can’t even access your app through the pod’s IP, make sure your app isn’t only binding to localhost.