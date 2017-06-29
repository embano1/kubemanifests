# Using labels for pod-to-node affinity (ignoring taints and more sophisticated affinity rules for the moment)
`kubectl get no -o wide --show-labels` # node not labeled  
`kubectl create -f node_affinity.yaml`  
`kubectl get po -w` # pod status will remain pending until node labeled  
`kubectl label node 172.17.4.201 gpu=true`  
`kubectl scale deploy nginx --replicas=5` # all pods will be scheduled to labeled node  

