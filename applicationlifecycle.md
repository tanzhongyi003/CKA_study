# Application Lifecycle Management  5%

  * Understand Deployments and how to perform rolling updates and rolbacks.
  https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
  
    * A Deployment is a higher-level resource meant for deploying applications and updating them declaratively, instead of doing it through a ReplicationController or a ReplicaSet, which are both considered lower-level concepts.
    * Rolling update
    https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
    #rolling-update-deployment
    * Rollback to 
    https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#rollback-to
    * exercise
      * kubectl set image deployment/frontend www=image:v2            
      * kubectl rollout history deployment/frontend
      * kubectl rollout undo deployment/frontend
      * kubectl rollout undo deployment/frontend --to-revision=2         
      * kubectl rollout status -w deployment/frontend                   
  * Know various ways to configure  applications.
    * Managing resources https://kubernetes.io/docs/concepts/cluster-administration/manage-deployment/
    * deployment change – things like image version change, port change, replica set count
    * Here is example to use replication controller rolling updates by doing change in the config file and replica set count https://kubernetes.io/docs/concepts/cluster-administration/manage-deployment/

  * Know how to scale applications.
  https://kubernetes.io/docs/reference/kubectl/cheatsheet/#scaling-resources
    * use replicasets or higher level deployments
      * kubectl scale
      * kubectl edit (replicas object)
      * --replicas
    * autoscale  

  * Understand the primitives necessary to create a self-healing application.
    * Kubernetes is self-healing
    * Self-healing as a feature of Kubernetes
    Use deployments (replicasets)
