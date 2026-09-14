# Modular Pod Routing Data and Benchmark Instances

This repository contains the New York City MTA data and benchmark graph instances used in the modular pod-routing study.

## Contents

- `static_gtfs_manhattan/`: static GTFS schedules, routes, trips, stops, and shapes for Manhattan.
- `realtime_gtfs_raw/`: raw real-time GTFS data collected from the MTA in February 2025.
- `instances/`: benchmark graph instances created from the processed transit data.
- `metadata/instance_summary.csv`: route composition and numbers of routes, trips, and stops for every instance.

## File names

`bus_data_2025-02-18_07.csv` contains real-time observations saved during hour `07` on February 18, 2025. Raw files follow `bus_data_YYYY-MM-DD_HH.csv`, using New York local time.

Instance files begin with an instance number. `_d0` and `_d1` contain one route direction, `_cmb` combines both directions of one route, and `_multi` combines multiple routes. For example, `001_cmb.csv` is combined-direction instance 001. Use `metadata/instance_summary.csv` to identify its route and size.

Each instance row records a trip stop, scheduled times, estimated passenger count, and required number of pods. Intermediate processed data are not included yet.

The raw real-time files use Git LFS. Clone the repository with Git LFS installed to download their full contents.
