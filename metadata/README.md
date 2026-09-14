# Instance Metadata

`instance_summary.csv` identifies the source, contents, and size of all 134 graph instances.

## Columns

- `instance_number`: number of the matching local `Graphs` folder.
- `instance_file`: CSV file in `instances/`.
- `scope`: `route` for a single-route instance or `cumulative` for a multi-route instance.
- `direction`: included route direction or directions.
- `routes`: included bus routes, separated by semicolons.
- `num_routes`: number of included routes.
- `num_trips`: number of source trip CSV files.
- `num_graph_records`: number of requester and releaser rows.
- `num_stops`: number of distinct stop identifiers.
