# ApplicationLifecycle Management  5%

  * Understand Deployments and how to perform roling updates and rolbacks.
    * A Deployment is a higher-level resource meant for deploying applications and updating them declaratively, instead of doing it through a ReplicationController or a ReplicaSet, which are both considered lower-level concepts.
      * kubectl set image deployment/frontend www=image:v2            
      * kubectl rollout history deployment/frontend
      * kubectl rollout undo deployment/frontend
      * kubectl rollout undo deployment/frontend --to-revision=2         
      * kubectl rollout status -w deployment/frontend                   
  * Know various ways to configure  applications.
  * Know how to scale applications.