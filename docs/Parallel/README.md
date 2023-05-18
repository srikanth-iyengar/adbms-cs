# Paralllel Database

- Moores law: Number of processors will double every 18-24 months
- CPU performance would increase by 50-60%
- I/O becomes bottleneck

## Parallel database systems
- Single Administrative system
- Homogenous working environment
- Close proximity of data storage
- Multiple processors

## Grid database systems
- Heterogenous collaboration of resources
- Provide seamless access to geographically distributed data sources

## Definitions:
- Throughput: The number of tasks that can be completed within a given interval of time.
- Response time: The amount of time it takes to complete a single task from the time it is submitted.
- Speed up: Performance improvement because of extra processing elements added.
Speed up = elapsed time on uniprocessor / elapsed tiem on multiprocessor
- Scale up: Performance improvement because of extra resource added.
Scale up = uniprocessor elapsed time on small system / multi processor elapsed time on larger system
### Transactional Scale up: 
- The increase in rate at which transactions are processed
- N-times as many users are submitting N-times as many requests or transactions against an N-times larger database

### Data Scale Up:
- The increase in size of the database, and the task is a large job who runtime depends on the size of the database (e.g. sorting)
- Typically found in online analytical processing (OLAP)


## Forms of parallelism
1. interquery
2. intraquery
3. intra operation
4. inter operation
5. mixed

### Interquery parallelism
- Parallelism among queries
- Different Queries executed in parallel with one another

### Intra query parallelism
- Parallelism within a query
- Execution of a single query in parallel or multi processor and disks

### Intraoperation
- Speeding up the processing of a query by parallelizing the execution of each individual operation (e.g. parallel sort, parallel search, etc)

### Interoperation
- Speeding up the processing of a query by executing in parallel different operations in a query expression (e.g. simultaneous sorting or searching)

### Pipeline Parallelism
- Output record of operation is given as input for another operation
- Useful with a small number of processors, but does not scale up well

### Independent Parallelism
- Operations in a query that do not depend on one another are executed in parallel
- Does not provide a high degree of parallelism 

## Parallel Database Architecture
- Shard Disk
- Shared Nothing
- Shared Something
