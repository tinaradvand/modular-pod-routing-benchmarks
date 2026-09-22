# Trips with Required Pods

This folder contains 14,713 Manhattan bus trips for which passenger counts were estimated and converted into a required number of modular pods. Each CSV represents one scheduled trip, and each row represents one stop on that trip.

For the estimation methodology and required citation, see [*Hierarchical Pod Routing for Modular Transit Systems*](https://doi.org/10.48550/arXiv.2508.18643) and the repository's [citation instructions](../README.md#citation).

## File names

Each filename is the trip's GTFS `trip_id` followed by `.csv`. For example, `MQ_A5-Weekday-003000_SBS14_701.csv` contains the stops for trip `MQ_A5-Weekday-003000_SBS14_701`. The identifier is not repeated as a column inside the file.

## Columns

- `arrival_time`: scheduled arrival time at the stop.
- `departure_time`: scheduled departure time from the stop.
- `stop_id`: GTFS identifier for the stop.
- `stop_sequence`: order of the stop within the trip.
- `Required_Pods`: estimated number of modular pods required to serve the trip.
