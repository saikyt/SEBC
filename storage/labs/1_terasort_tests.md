## Terragen command 
```
time hadoop jar  /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -D dfs.block.size=33554432 -Dmapred.map.tasks.speculative.execution=false 100000000 terasort-input
```
## Terrasort command
```
time hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapred.map.tasks=300 -Dmapred.reduce.tasks=150 -Dmapred.reduce.tasks.speculative.execution=false terasort-input terasort-output
```

## Terragen time results
```
real    2m43.277s
user    0m5.294s
sys     0m0.289s
```

## Terrasort time results
```
real    4m6.872s
user    0m8.431s
sys     0m0.395s
```


