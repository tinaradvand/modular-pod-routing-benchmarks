# Manhattan Static GTFS Data

These files describe the scheduled MTA bus service used in the study. IDs connect the files: routes contain trips, trips contain stop times, and stop times reference stops.

## Files and columns

### `agency.txt`

- `agency_id`: identifier for the transit agency.
- `agency_name`: agency name.
- `agency_url`: agency website.
- `agency_timezone`: time zone used by the schedule.
- `agency_lang`: primary agency language.
- `agency_phone`: agency contact number.

### `routes.txt`

- `route_id`: identifier for a route.
- `agency_id`: agency operating the route.
- `route_short_name`: short rider-facing route name, such as M1.
- `route_long_name`: full route name.
- `route_desc`: route description.
- `route_type`: GTFS transport mode; `3` means bus.
- `route_color`: route display color.
- `route_text_color`: text color used with the route color.

### `trips.txt`

- `route_id`: route served by the trip.
- `service_id`: service calendar followed by the trip.
- `trip_id`: identifier for a scheduled trip.
- `trip_headsign`: rider-facing destination or direction.
- `direction_id`: distinguishes the two directions of a route; `0` and `1` are labels, not universal compass directions.
- `block_id`: group of consecutive trips assigned to the same vehicle block.
- `shape_id`: route geometry associated with the trip.

### `stop_times.txt`

- `trip_id`: trip associated with the stop record.
- `arrival_time`: scheduled arrival time.
- `departure_time`: scheduled departure time.
- `stop_id`: referenced stop.
- `stop_sequence`: order of the stop within the trip.
- `pickup_type`: whether passenger pickup is allowed or requires special arrangements.
- `drop_off_type`: whether passenger drop-off is allowed or requires special arrangements.
- `timepoint`: whether the listed time is exact (`1`) or approximate (`0`).

### `stops.txt`

- `stop_id`: identifier for a stop.
- `stop_name`: rider-facing stop name.
- `stop_desc`: optional stop description.
- `stop_lat`: stop latitude.
- `stop_lon`: stop longitude.
- `zone_id`: fare zone, when provided.
- `stop_url`: stop information URL, when provided.
- `location_type`: GTFS location category; `0` represents a stop or platform.
- `parent_station`: parent station identifier, when applicable.

### `calendar.txt`

- `service_id`: identifier for a service schedule.
- `monday` through `sunday`: `1` when the service normally runs on that weekday and `0` otherwise.
- `start_date`: first date of the service period in `YYYYMMDD` format.
- `end_date`: last date of the service period in `YYYYMMDD` format.

### `calendar_dates.txt`

- `service_id`: service schedule being modified.
- `date`: exception date in `YYYYMMDD` format.
- `exception_type`: `1` adds service and `2` removes service on that date.

### `shapes.txt`

- `shape_id`: identifier for a route path.
- `shape_pt_lat`: latitude of a point on the path.
- `shape_pt_lon`: longitude of a point on the path.
- `shape_pt_sequence`: order of the point along the path.

Column definitions follow the [GTFS Schedule reference](https://gtfs.org/documentation/schedule/reference/).
