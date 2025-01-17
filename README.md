# Vector Search Performance Benchmark of SingleStore, Pinecone and Zilliz  - Data Set

This repository contains the associated raw benchmark results of the benchANT blog post [Vector Search Performance Benchmark of SingleStore, Pinecone and Zilliz](https://benchant.com/blog/single-store-vector-vs-pinecone-zilliz-2025) and the associated SingleStore blog post [SingleStore Matches Vector Search Performance of Pinecone and Zilliz](https://www.singlestore.com/blog/singlestore-matches-vector-search-performance-of-pinecone-and-zilliz/). 

The `results` folder contains the data for the six benchmark cases:
- `SingleStore S2` 
- `SingleStore S4` 
- `Pinecone (S2 price equal)` 
- `Pinecone (S4 price equal)` 
- `Zilliz (recommended)`
- `Zilliz (S4 price equal)` 

For more details on the method and the benchmark objectives please refer to the blog post.

Each folder contains the data of a single run benchmark of one configuration. 

***

## Data Set Structure


In order to ensure full transparency and reproducibility,  each data folder contains benchmark configuration data,  performance data, monitoring data, cloud provider metadata, VM metadata and DBMS configuration data.
 

***

### Benchmark Configuration Data

All configurable benchmark parameters for each DBaaS and VectorDBBench are defined in the `evaluationScenario.json`.

The `benchANT_versions` contains the used versions of the benchANT software components to execute the benchmarks. 

The execution logs of the individual benchmark steps are contained in `airflowTaskInstanceDetails.json`. 

***

### Performance Data

The raw performance data output of the VectorDBBench is contained in the `0_load.txt`  for the LOAD, OPTIMIZE and QUERY phase. 

***

### Monitoring Data

The DBMS cluster and the benchmark instances are monitored with [Telegraf](https://github.com/influxdata/telegraf) and the data is stored in [InfluxDB](https://github.com/influxdata/influxdb). 

A full snapshot of the monitoring data of each run is contained in the  `influx_data.zip` file.


*** 

### DBaaS Metadata

The DBaaS metadata for each DBMS deployment is available in `dbaas_resources.json`. 


*** 

### Cloud Provider Metadata

The cloud provider metadata for the VectorDBBench benchmark deployment in the `benchmark_resources.json`. 


*** 

### VM Metadata

The VM metadata for the DBMS deployment is contained in the `dbms_data_hardware_facts.json` / `dbms_management_hardware_facts.json` and for the benchmark deployment in the `benchmark_hardware_facts.json`.  


*** 


## Contact

In case of questions or feedback on the data feel free to create an issue or reach out to info@benchant.com

