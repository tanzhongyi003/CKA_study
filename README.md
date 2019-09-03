# study

# 
https://github.com/cncf/curriculum/blob/master/CKA_Curriculum_V1.14.1.pdf

# kubectl cheatsheet
https://kubernetes.io/docs/reference/kubectl/cheatsheet/

# schedule
  * Use label selectors to schedulePods
    * Ref: https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/
    * Sample: 
        *  kubectl label nodes node1 disktype=ssd
        *  kubectl get nodes --show-labels
        *  https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/
        nodeSelector:
          disktype: ssd
        *  kubectl get pods --output=wide

  


