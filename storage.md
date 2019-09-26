# Storage 7%
https://cka-exam.blog/storage/

 * Understand persistent volumes and know how to create them.
   * Volume https://kubernetes.io/docs/concepts/storage/volumes/
     * At its core,Volume is just a directory, with some data in it, which is accessible to the containers in a Pod.
     * How that directory comes to be, the medium that backs it are determined by the particular volume type used.
   * Persistent Volume https://kubernetes.io/docs/concepts/storage/persistent-volumes/
     * Two API
       * PersistentVolume
       * PersistentVolumeClaim
     * PVs are resources in the cluster, PVCs are requests for those resources  
   
 * Understand access modes for volumes.
   * 3 modes https://kubernetes.io/docs/concepts/storage/persistent-volumes/#access-modes
     * ReadWriteOnce – the volume can be mounted as read-write by a single node
     * ReadOnlyMany – the volume can be mounted read-only by many nodes
     * ReadWriteMany – the volume can be mounted as read-write by many nodes

 * Understand persistent volume claims primitive
   * https://kubernetes.io/docs/concepts/storage/persistent-volumes/#persistentvolumeclaims

 * Understand Kubernetes storage objects.
   * https://kubernetes.io/docs/concepts/storage/volumes/#types-of-volumes

 * Know how to configure application with persistent storage.
   * Volumn as emptyDir will be kept within the pod's lifecycle https://kubernetes.io/docs/tasks/configure-pod-container/configure-volume-storage/
   * PV and PVC: https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/  

Excersise

https://kubernetes.io/docs/tasks/configure-pod-container/configure-volume-storage/
https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/