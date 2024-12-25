# Warehouses
Warehouse is used to provide <ins>compute resources</ins> to execute queries and operations.

## Typologies of the warehouse

Types of the warehouse :  
* Standard 
* Snowpark-optimized 

Standard is most suitable in most use cases 
Snowpark-optimized  is recommended for memory-intensive workloads such as ML training. 

Size : xs, s, m, l, xl, 2xl, 3xl 

Multi-cluster : add additional cluster and group queries in this one multi-cluster warehouse. Auto-scaling depending workflow. Great for concurrent users! 

For the complex workload it is better use bigger size of the warehouse! 

## Scaling policy 

**Standard (default)**- favors starting additional warehouses.  
**Economy** - favors conserving credits rather than starting additional warehouses. 
Cluster start only if the system estimates there's enough query load to keep the cluster <ins>busy for at least 6 minutes</ins>. Cluster shuts down after 5 to 6 consecutive successful checks. 
