# Core Concepts 19%
https://cka-exam.blog/core-concepts/

* Understand the Kubernetes API primitives.
  * Kubernetes API Concepts
 https://kubernetes.io/docs/reference/using-api/api-concepts/
  * Kubernetes API overiview
  https://kubernetes.io/docs/concepts/overview/kubernetes-api/
  * Kubernetes API reference
  https://kubernetes.io/docs/reference/


* Understand the Kubernetes cluster architecture.
  * Kubernes components https://kubernetes.io/docs/concepts/overview/components/
    * Master
      * Kubernetes API Server
      * etcd
      * kube-scheduler
      * kube-controller-manager
      * cloud-controller-manager
      The following controllers have cloud provider dependencies:

        * Node Controller: For checking the cloud provider to determine if a node has been deleted in the cloud after it stops responding
        * Route Controller: For setting up routes in the underlying cloud infrastructure
        * Service Controller: For creating, updating and deleting cloud provider load balancers
        * Volume Controller: For creating, attaching, and mounting volumes, and interacting with the cloud provider to orchestrate volumes

    * Node
      * kubelet
      * kube-proxy
      * Container Runtime

  * Nodes https://kubernetes.io/docs/concepts/architecture/nodes/
  * Master-Node communication https://kubernetes.io/docs/concepts/architecture/master-node-communication/
    * Cluster to Master
      * Master listen on HTTPS Port 443
    * Master to Cluster
      * apiserver to kubelet
      * apiserver to node/pod/service through apiserver's proxy  
  * Cloud Controller Manager https://kubernetes.io/docs/concepts/architecture/cloud-controller/

* Understand Services and other network primitives.
  * Services: An abstract way to expose an application running on a set of Pods as a network service.https://kubernetes.io/docs/concepts/services-networking/service/
    * Two main stream modes 
      * iptables mode
        * need to set readiness probes
      * ipvs mode
    * Multi-Port Services
    * Four type of Service
      * ClusterIP: default
      * NodePort:
      * LoadBlancer:
      * ExternalName:

  * Connecting Applications with Service
  https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/
    * the part for SSL is great https://github.com/kubernetes/examples/tree/master/staging/https-nginx/

  * Ingress
  https://kubernetes.io/docs/concepts/services-networking/ingress/

