# Data-Knowledge
We provide in the repository the two described applications: 
-Use case 1 (named Aces_wp3_Alibaba_Ml-UPMv0): has a deployment file where we set requests and limits. Here when we run the application, we can see pods running and crashing when they reach their limits as configured (this is done in repetition).  

- Use case 2 (named Aces_wp3_Alibaba_Ml-UPMv1): has a deployment file where we remove these parameters.  Here the 3 pods will run without trouble since there are no limits, and the consumption is minimal and does not cause trouble to the whole cluster. In this case, to push the system to its limits, we increased the number of replicas. This led to pod failures depending on the number of replicas specified and the system's available resources.  
