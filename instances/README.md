# Benchmark Graph Instances

These CSV files are the benchmark graph instances created for the modular pod-routing experiments.

## File names

Each name begins with an instance number. `_d0` and `_d1` contain one direction of one route, `_cmb` combines both directions of one route, and `_multi` combines multiple routes. For example, `001_cmb.csv` is combined-direction instance 001. The corresponding routes and instance sizes are listed in `metadata/instance_summary.csv`.

## Columns

- `trip_id`: scheduled trip identifier.
- `route`: bus route name.
- `direction`: route direction label (`d0` or `d1`).
- `stop_sequence`: order of the stop within the trip.
- `arrival_time`: scheduled arrival time.
- `departure_time`: scheduled departure time.
- `stop_id`: stop identifier.
- `estimated_passenger_count`: passenger count assigned or estimated for the trip at the stop.
- `required_pods`: number of modular pods required at the stop.
