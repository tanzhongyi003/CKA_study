# Security 12%


4C of security on Cloud Native(Code/Container/Cluster/Cloud)
https://kubernetes.io/docs/concepts/security/overview/

 * Know how to configure authentication and authorization.
   * TLS->Authentication(ServiceAccount/x509)->Authorization(RBAC) 
   https://kubernetes.io/docs/reference/access-authn-authz/controlling-access/
   https://kubernetes.io/docs/tasks/administer-cluster/securing-a-cluster/
     * Authentication: https://kubernetes.io/docs/reference/access-authn-authz/authentication/
     * Ahthorization: https://kubernetes.io/docs/reference/access-authn-authz/authorization/

 * Understand Kubernetes security primitives.
   https://kubernetes.io/docs/concepts/security/overview/

 * Know to configure network policies
   https://kubernetes.io/docs/concepts/services-networking/network-policies/
   https://kubernetes.io/docs/tasks/administer-cluster/declare-network-policy/

 * Create and manage TLS certificates for cluster components
 https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/

 * Work with images securely.
   * Ensure images are free of vulnerabilities
   * Implement Continuous Security Vulnerability Scanning – Containers might include outdated packages with known vulnerabilities (CVEs). This cannot be a ‘one off’ process, as new vulnerabilities are published every day. An ongoing process, where images are continuously assessed, is crucial to insure a required security posture.
   * Regularly Apply Security Updates to Your Environment – Once vulnerabilities are found in running containers, you should always update the source image and redeploy the containers. Try to avoid direct updates (e.g. ‘apt-update’) to the running containers, as this can break the image-container relationship. Upgrading containers is extremely easy with the Kubernetes rolling updates feature - this allows gradually updating a running application by upgrading its images to the latest version.
   * Ensure That Only Authorized Images are Used in Your Environment
   * Use private registries to store your approved images - make sure you only push approved images to these registries.

 * Define security contexts.
   https://kubernetes.io/docs/tasks/configure-pod-container/security-context/

 * Secure persistent key value store.
   * Using Secret: https://kubernetes.io/docs/concepts/configuration/secret/