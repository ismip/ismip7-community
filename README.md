# ISMIP7 community scripts

Scripts, notebooks and snippets shared by people working on
[ISMIP7](https://www.ismip.org/), for anyone to use. They are checked only
to see that they are in the right place and look safe, not that they are
correct. Each one has a README saying who wrote it and what they used it
for; ask them if you are unsure.

## What's here

| Folder | For |
|---|---|
| [AIS/](AIS/) | Antarctica only |
| [GrIS/](GrIS/) | Greenland only |
| [cloud/](cloud/) | Cloud platforms: reading data from source.coop, working on CryoCloud |
| [general/](general/) | Everything else, including tools for both ice sheets |

Each contribution is a folder with its own README.

## Maintained tools

For standard processing, use the maintained ISMIP7 tools. They are tested
and documented, and everyone gets the same answer from them.

- [ISM_SimulationChecker](https://github.com/ismip/ISM_SimulationChecker):
  checks model output against the data request before submission
- [ismip7-interpolation](https://github.com/ismip/ismip7-interpolation):
  regrids model output onto the ISMIP7 grids
- [ismip7-scalar-processing](https://github.com/ismip/ismip7-scalar-processing):
  computes scalar time series, for whole ice sheets and IMBIE3 basins

## Contributing

Anyone in the ISMIP7 community can add something, and it does not need to
be polished. [CONTRIBUTING.md](CONTRIBUTING.md) says where it goes, what
it needs and how to submit it.

## Questions

Ask in the [ISMIP discussions](https://github.com/orgs/ismip/discussions).
Report a problem with a contribution as an
[issue](https://github.com/ismip/ismip7-community/issues), naming its
folder.

Distributed under the MIT License; see [LICENSE](LICENSE).
