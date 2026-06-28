# observatorio-data

**Entity:** Observatorio de Sostenibilidad (association — OS)  
**Status:** Ported from `os-open-data` (2026-06-28) — 20 dataset packages, DCAT-AP catalog  
**Constitution:** [observatorio-sostenibilidad](https://github.com/observatorio-sostenibilidad/observatorio-sostenibilidad)

## Purpose

Public open data catalog for the Observatorio. DCAT-AP 3.0 index, Frictionless Data packages, and dataset metadata. Replaces `os-open-data`.

## Layout

```
catalog/index.yaml
catalog/references.yaml
datasets/{id}/datapackage.json
```

Dataset bytes (Parquet, GeoParquet, PMTiles) are stored in object storage in production; this repository holds catalog metadata and references.

**CNIG boundary blobs** (~430M) are gitignored locally. Mount them separately for full geo dev, or use GCS in production (legacy policy).

## Role in the ecosystem

| Related repository | Relationship |
|--------------------|--------------|
| [observatorio-platform](https://github.com/observatorio-sostenibilidad/observatorio-platform) | DAR registry and admin UI |
| [os-kernel](https://github.com/observatorio-sostenibilidad/os-kernel) | Query plane for Parquet datasets |
| [platform-saas](https://github.com/observatorio-sostenibilidad/platform-saas) | May license OS datasets for commercial modules |

Re-port with `./scripts/port-observatorio-data.sh` from the constitution repo.

## Documentation

- [port-phase-1-content-data.md](https://github.com/observatorio-sostenibilidad/observatorio-sostenibilidad/blob/main/docs/implementation/port-phase-1-content-data.md)

## License

Apache License 2.0 — see [LICENSE](./LICENSE).

Individual datasets may carry additional attribution or terms when content is published; those will be documented per dataset.
