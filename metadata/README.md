# Instance Metadata

`instance_summary.csv` identifies the source, contents, and size of all 134 graph instances.

## Columns

- `instance_number`: numerical identifier assigned to the graph instance.
- `instance_file`: CSV file in `instances/`.
- `type`: how routes and directions are grouped:
  - `d0`: direction 0 of one route.
  - `d1`: direction 1 of one route.
  - `cmb`: both directions of one route combined.
  - `multi`: multiple routes combined cumulatively.
- `routes`: included bus routes, separated by semicolons.
- `num_routes`: number of included routes.
- `num_trips`: number of source trip CSV files.
- `num_graph_records`: number of requester and releaser rows.
- `num_stops`: number of distinct stop identifiers.
