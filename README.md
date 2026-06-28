# observatorio-data

**Entity:** Observatorio de Sostenibilidad (association — OS)  
**Status:** Scaffold — documentation only, no datasets yet  
**Constitution:** [observatorio-sostenibilidad](https://github.com/observatorio-sostenibilidad/observatorio-sostenibilidad)

## Purpose

Public open data catalog for the Observatorio. DCAT-AP 3.0 index, Frictionless Data packages, and dataset metadata. Replaces `os-open-data`.

## Expected layout

```
catalog/index.yaml
catalog/references.yaml
datasets/{id}/datapackage.json
```

Dataset bytes (Parquet, GeoParquet, PMTiles) are stored in object storage in production; this repository holds catalog metadata and references.

## Role in the ecosystem

| Related repository | Relationship |
|--------------------|--------------|
| [observatorio-platform](https://github.com/observatorio-sostenibilidad/observatorio-platform) | DAR registry and admin UI |
| [os-kernel](https://github.com/observatorio-sostenibilidad/os-kernel) | Query plane for Parquet datasets |
| [platform-saas](https://github.com/observatorio-sostenibilidad/platform-saas) | May license OS datasets for commercial modules |

## Documentation

Detailed architecture docs are pending publication in the constitution repository.

## License

Apache License 2.0 — see [LICENSE](./LICENSE).

Individual datasets may carry additional attribution or terms when content is published; those will be documented per dataset.
