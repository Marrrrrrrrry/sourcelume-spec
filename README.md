# Apache Sourcelume — Spec (`sourcelume-spec`)

## Overview

This repository contains our Apache Sourcelume specification.


```
sourcelume-spec/
├── LICENSE                     # Apache 2.0 (code/tooling)
├── README.md
├── NOTICE                      # required for ASF releases
├── CHANGELOG.md
├── VERSIONING.md               # semver rules for spec changes; the `latest` pointer
├── SETUP.md                    # dev setup; mvn install for downstream builds
├── pom.xml                     # packages context/ + schema/ resources into a JAR
├── pyproject.toml              # Python tooling (validator) dependencies
├── context/
│   └── 0.0.1/
│       └── sourcelume.jsonld   # the JSON-LD @context document, pinned
├── schema/
│   ├── 0.0.1/
│   │   ├── sourcelume.schema.json           # JSON Schema for structural validation (ProvenanceRecord)
│   │   ├── sourcelume-training.schema.json  # JSON Schema for TrainingProvenanceRecord
│   │   └── sourcelume.shacl.ttl             # SHACL shapes for RDF-level validation (optional but common for JSON-LD vocabs)
│   └── ...                     # future version directories (see VERSIONING.md)
├── spec/                       # the prose specification
│   └── 0.0.1/
│       └── index.md            # human-readable spec text, versioned alongside schema
├── examples/                   # records covering both record types
│   ├── acme-undisclosed-model.jsonld   # TrainingProvenanceRecord with undisclosed data
│   └── dfm-mimir-*.jsonld              # dataset and model records for the Mímir datasets
├── mappings/                   # crosswalks to related vocabularies
│   ├── croissant-crosswalk.md
│   ├── spdx-ai-profile-crosswalk.md
│   └── otdi-crosswalk.md
├── tools/
│   ├── validate.py             # reference validator — validates examples/ against schema + SHACL
│   └── render-docs.py          # generates a Markdown field reference from schema
├── tests/
│   └── test_validate.py        # unit tests for the validator
├── .github/workflows/
│   └── ci.yml                  # CI: Maven verify + Python validation (schema/SHACL + unit tests)
└── .gitignore
```

## Versioning
 
This project follows [Semantic Versioning](https://semver.org). See
`VERSIONING.md` for how MAJOR, MINOR, and PATCH apply to specification
changes, and for the rules around the `latest` pointer and immutable
released versions.


## Get involved

- Mailing list: dev@sourcelume.apache.org ([archives](https://lists.apache.org/list.html?dev@sourcelume.apache.org))
- ASF Slack: #sourcelume (Ask to be invited)

## License

This project is licensed under [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).