# Data-Knowledge

Data knowledge is an ACES kernel component that delivers comprehensive insights about ML-based workload characterization and resource allocation and utilization

We provide in the repository applications (use case 1 and use case 2): 

- Use case 1 (named Aces_wp3_Alibaba_Ml-UPMv0): has a deployment file where we set requests and limits. Here when we run the application, we can see pods running and crashing when they reach their limits as configured (this is done in repetition).  

- Use case 2 (named Aces_wp3_Alibaba_Ml-UPMv1): has a deployment file where we remove these parameters.  Here the 3 pods will run without trouble since there are no limits, and the consumption is minimal and does not cause trouble to the whole cluster. In this case, to push the system to its limits, we increased the number of replicas. This led to pod failures depending on the number of replicas specified and the system's available resources.  

To deploy the two applications to a Kubernetes cluster and run it, the command to run in the specific folder of the application is as follows: 
 
 - kubectl apply -f k8s_manifests/deployment.yaml -n (the-namespace) 

To create more replicas for use case 2, the used command is as follows:

 - kubectl -n (the-namespace)  scale deployment aces-w3-alibaba-ml-upm --replicas 10 
