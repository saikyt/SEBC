## Terragen command 
```
hadoop jar  /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -D dfs.block.size=33554432 -Dmapred.map.tasks.speculative.execution=false 100000000 terasort-input
```
## Terrasort command

