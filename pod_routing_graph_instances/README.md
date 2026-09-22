# Graph Instances

Each CSV contains the trip records used to construct one graph instance for the modular pod-routing experiments. Solver logs and experimental output files are not included.

For the instance-construction methodology and required citation, see [*Hierarchical Pod Routing for Modular Transit Systems*](https://doi.org/10.48550/arXiv.2508.18643) and the repository's [citation instructions](../README.md#citation).

## File names

`NNN` is the three-digit instance identifier assigned when the instances were created. For example, `instance_001.csv` is instance 1 and `instance_134.csv` is instance 134. Leading zeros keep the files in numerical order.

Instances 1–108 are route-level instances arranged in groups of three: `d0` is direction 0, `d1` is direction 1, and `cmb` combines both directions. Instances 109–134 are `multi` instances that cumulatively combine multiple routes. See `graph_instance_metadata/instance_summary.csv` for each instance's type, routes, and size.

## Columns

- `trip_id`: scheduled bus-trip identifier.
- `arrival_time`: scheduled time at the requester or releaser stop.
- `stop_id`: GTFS stop identifier.
- `stop_sequence`: position of the stop in the scheduled trip.
- `Required_Pods`: number of pods assigned to the trip.
- `pod_id`: pod number within that trip.
- `label`: `requester` when the trip requires the pod and `releaser` when the pod becomes available.
- `Node_id`: identifier shared by the requester and releaser records for the same pod movement.
