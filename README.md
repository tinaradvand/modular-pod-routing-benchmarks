# Modular Pod Routing Data and Benchmark Instances

This repository contains the Manhattan MTA GTFS data, derived trip-level pod requirements, and graph instances used in [*Hierarchical Pod Routing for Modular Transit Systems*](https://doi.org/10.48550/arXiv.2508.18643).

## Citation

If you use any part of this dataset, please cite the paper:

> Tina Radvand, Alireza Talebpour, and Yanfeng Ouyang. “Hierarchical Pod Routing for Modular Transit Systems.” arXiv:2508.18643, 2025. https://doi.org/10.48550/arXiv.2508.18643

```bibtex
@article{radvand2025hierarchical,
  title   = {Hierarchical Pod Routing for Modular Transit Systems},
  author  = {Radvand, Tina and Talebpour, Alireza and Ouyang, Yanfeng},
  journal = {arXiv preprint arXiv:2508.18643},
  year    = {2025},
  doi     = {10.48550/arXiv.2508.18643}
}
```

GitHub can also generate this citation from [`CITATION.cff`](CITATION.cff).

## Contents

- [`manhattan_static_gtfs/`](manhattan_static_gtfs/): MTA static GTFS schedules, trips, stops, and route geometry.
- [`manhattan_realtime_gtfs/`](manhattan_realtime_gtfs/): raw MTA Bus Time observations collected over 10 weekdays in February 2025.
- [`manhattan_trips_with_pod_requirements/`](manhattan_trips_with_pod_requirements/): 14,713 scheduled trips with estimated modular-pod requirements.
- [`pod_routing_graph_instances/`](pod_routing_graph_instances/): 134 graph instances used in the modular pod-routing experiments.
- [`graph_instance_metadata/`](graph_instance_metadata/): routes, directions, and size information for every graph instance.

Each folder has a README describing its files, filenames, and columns. The paper explains the collection and preparation methodology.

## Download

The raw real-time CSV files total approximately 3.0 GiB and are stored with [Git LFS](https://git-lfs.com/). To download the complete repository:

```bash
git lfs install
git clone https://github.com/tinaradvand/modular-pod-routing-benchmarks.git
cd modular-pod-routing-benchmarks
git lfs pull
```

The 14,713 trip-level CSV files are also available as one archive from the [latest release](https://github.com/tinaradvand/modular-pod-routing-benchmarks/releases/latest/download/manhattan_trips_with_pod_requirements.zip).

## Version and provenance

Release `v1.0.0` is the dataset associated with the current arXiv paper. The source schedule and vehicle-observation fields originate from New York MTA static GTFS and MTA Bus Time. Derived pod requirements, graph instances, metadata, and documentation were prepared for the study.

## License

The derived datasets and documentation are available under [CC BY 4.0](DATA_LICENSE.md), which requires attribution. Original MTA source data remain subject to the MTA's applicable terms and policies. Any software subsequently added to this repository is covered by the existing [MIT License](LICENSE).
