# Raw MTA Bus Time Data

These CSV files contain the real-time data collected from the MTA Bus Time SIRI VehicleMonitoring API in February 2025. Each API record describes a bus, its assigned trip, its location, the referenced stop, and passenger-count fields when supplied by the feed.

For the collection methodology and required citation, see [*Hierarchical Pod Routing for Modular Transit Systems*](https://doi.org/10.48550/arXiv.2508.18643) and the repository's [citation instructions](../README.md#citation).

## File names

Files follow `bus_data_YYYY-MM-DD_HH.csv`. For example, `bus_data_2025-02-18_07.csv` is the file for February 18, 2025, hour 07 in New York local time. The files retain the names created during collection.

## Columns

- `Bus Data for Vehicle`: vehicle-based row label created when the API records were saved.
- `LineRef`: fully qualified route identifier.
- `DirectionRef`: GTFS direction identifier (`0` or `1`) for the assigned trip.
- `DataFrameRef`: service date for the assigned trip.
- `DatedVehicleJourneyRef`: identifier of the scheduled trip, prefixed by the agency identifier.
- `JourneyPatternRef`: GTFS shape identifier, prefixed by the agency identifier.
- `PublishedLineName`: rider-facing route name.
- `OperatorRef`: agency identifier.
- `OriginRef`: identifier of the first stop of the trip.
- `DestinationName`: rider-facing trip destination or headsign.
- `ProgressRate`: reported movement state, such as normal progress, no progress, or layover.
- `Longitude`: reported or inferred bus longitude.
- `Latitude`: reported or inferred bus latitude.
- `BlockRef`: assigned vehicle block identifier, when available.
- `VehicleRef`: bus identifier, prefixed by the agency identifier.
- `AimedArrivalTime`: scheduled arrival time at the referenced stop, when available.
- `AimedDepartureTime`: scheduled departure time at the referenced stop, when available.
- `StopPointRef`: identifier of the referenced stop.
- `StopPointName`: name of the referenced stop.
- `StrollerVehicle`: stroller-accessibility indicator supplied by the feed, when available.
- `EstimatedPassengerCount`: estimated number of passengers supplied by the feed, when available.
- `EstimatedPassengerCapacity`: estimated passenger capacity supplied by the feed, when available.

Blank values mean that the field was not supplied for that record. MTA field definitions are documented in the [SIRI VehicleMonitoring](https://bustime-classic.mta.info/wiki/Developers/SIRIVehicleMonitoring) and [MonitoredVehicleJourney](https://bustime-classic.mta.info/wiki/Developers/SIRIMonitoredVehicleJourney) references.

The CSV files are stored with Git LFS. Git LFS must be installed to download their full contents.
