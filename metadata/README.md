# Instance Metadata

`instance_summary.csv` identifies the routes and size of every benchmark graph instance.

## Columns

- `instance_name`: instance filename without the `.csv` extension.
- `type`: instance type (`d0`, `d1`, `cmb`, or `multi`).
- `routes`: route or routes included; multiple routes are separated by `|`.
- `num_routes`: number of routes in the instance.
- `num_trips`: number of scheduled trips in the instance.
- `num_stops`: number of distinct stops in the instance.
