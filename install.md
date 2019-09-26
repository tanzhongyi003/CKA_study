# Instalation,Configuration &Validation 12%
https://cka-exam.blog/installation-configuration-validation/

  ## The hard way https://github.com/kelseyhightower/kubernetes-the-hard-way

 * Design a Kubernetes cluster.
   * https://kubernetes.io/docs/setup/#designing-and-preparing
     * Minikube
     * cloud

 * Install Kubernetes masters and nodes.
   * Using kubeadm to install
     * Running kubeadm init on master to create the cluster's master
     * Running kubeadm join on worker node to join the cluster

 * Configure secure cluster communications.
   * securing a cluster https://kubernetes.io/docs/tasks/administer-cluster/securing-a-cluster/
     * Using TLS
     * API Authentication
     * API Authorization(RBAC)
   * https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/   


 * Configure a Highly-Available Kubernetes cluster https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/high-availability/
 
   * Two type
     * etcd and API server are co-located
     * using an external etcd cluster
   * At least 3 servers, need kubeadm/kubelet
   * Steps: 
     * Create load balancer for 3 server
     * On 1st server, run kubeadmin init with control-plane-endpoint paramater set to load balancer 
     * on remain servers run kubeadm join

 * Know where to get the Kubernetes release binaries
   * https://kubernetes.io/docs/setup/release/notes/

 * Provision underlying infrastructure to deploya Kubernetes cluster

 * Choose a network solution.
   * Cluster Networking https://kubernetes.io/docs/concepts/cluster-administration/networking/
     * pod to localhost
     * pod to pod
     * pod to service (by service)
     * External to service(by service)
   * The Kubernetes network model
     * Every pod gets its own IP (containers on one pod share the same IP, but need to use seperate port, IP-per-pod model)
     * Many implentations such as Calico, Weave Net

 * Choose your Kubernetes infrastructure configuration.

 * Run end-to-end tests on your cluster.

 * Run Node end-to-end tests.
 
 * Install and use kubeadm toinstall,configure, and manage Kubernetes clusters.