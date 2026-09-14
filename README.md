# Modular Pod Routing Benchmark Graph Instances

This repository contains the benchmark graph instances used in the modular pod-routing study. They were constructed from New York City MTA static and real-time GTFS data.

- `instances/`: 133 CSV graph instances.
- `metadata/instance_summary.csv`: routes, trips, and stops in each instance.
- `*_d0` and `*_d1`: one travel direction; `*_cmb`: both directions; `*_multi`: multiple routes.

Each instance records trip and stop sequences, scheduled times, estimated passenger counts, and required pods. Raw and intermediate processed data are not included here.
