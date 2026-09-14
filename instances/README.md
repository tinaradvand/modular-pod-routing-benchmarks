# Graph Instances

Each CSV combines the trip records stored in the matching numbered folder in the local `Graphs` archive. Solver logs and experimental output files are not included.

## File names

`instance_NNN.csv` corresponds directly to `Graphs/NNN/Trips/`. For example, `instance_001.csv` comes from `Graphs/1/Trips/`, and `instance_134.csv` comes from `Graphs/134/Trips/`.

Instances 1–108 are route-level instances arranged in groups of three: `d0` is direction 0, `d1` is direction 1, and `cmb` combines both directions. Instances 109–134 are `multi` instances that cumulatively combine multiple routes. See `metadata/instance_summary.csv` for each instance's type, routes, and size.

## Columns

- `trip_id`: scheduled bus-trip identifier.
- `arrival_time`: scheduled time at the requester or releaser stop.
- `stop_id`: GTFS stop identifier.
- `stop_sequence`: position of the stop in the scheduled trip.
- `Required_Pods`: number of pods assigned to the trip.
- `pod_id`: pod number within that trip.
- `label`: `requester` when the trip requires the pod and `releaser` when the pod becomes available.
- `Node_id`: identifier shared by the requester and releaser records for the same pod movement.
