Inserted values:

```
Worker vcore    20
Worker spindles 12
Worker RAM      128
Workload factor 2
Worker nodes    10
```
i accept above value and the derivated one. The only observation is about the OS Memory (12.8GB) that could be reduced if YARN application use more CPU than I/O.

The purpose of workload factor is to determine the number of map and reduce task, relative to one job, that will run on each node in the cluster. So, for example, a workload factor of 1 will run 1 map and 1 task on each node, a workload factor of 2 will run 2 map and 2 task on each node, and so on. The choice of this factor depend on the use cases of the cluster: if on the cluster will run many concurrent lightweight YARN application, it is better to keep this factor low. On the other side if on the cluster will not run many concurrent YARN application, and each application will be heavy in term of needed resources, it is better to keep this value high.
