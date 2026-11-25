# Nebula Pipeline

An index for the Nebula Pipeline, a modular production pipeline for animation and VFX built between
2019 and 2021.

The code lives in a public [Bitbucket workspace](https://bitbucket.org/nebulapipeline/workspace/repositories).
This repository is the map, because twenty-nine repositories read better as an architecture than as a
list.

## What it is

Nebula was a studio pipeline assembled from small services rather than one monolith: production
planning, asset management, DCC integration, packaging and render-farm submission, each as its own
repository with its own history. It grew out of pipeline work at ICE Animations and was used as the basis
for the Nebula Pipeline Toolbox, whose [documentation is public on Read the Docs](https://nebula-pipeline-toolbox-docs.readthedocs.io/en/master/).

## The modules

| Repository | Responsibility |
|---|---|
| [`nebula-core`](https://bitbucket.org/nebulapipeline/nebula-core) | Core services and shared plumbing |
| [`nebula-gui`](https://bitbucket.org/nebulapipeline/nebula-gui) | Artist-facing interface layer |
| [`nebula-backends`](https://bitbucket.org/nebulapipeline/nebula-backends) | Pluggable backends behind the core |
| [`nebula-proplan`](https://bitbucket.org/nebulapipeline/nebula-proplan) | Production planning |
| [`nebula-packer`](https://bitbucket.org/nebulapipeline/nebula-packer) | Packaging |
| [`nebula-auth`](https://bitbucket.org/nebulapipeline/nebula-auth) · [`nebula-login`](https://bitbucket.org/nebulapipeline/nebula-login) | Access control and sign-in |
| [`nebula-tools`](https://bitbucket.org/nebulapipeline/nebula-tools) · [`nebula-util`](https://bitbucket.org/nebulapipeline/nebula-util) | Tooling and utilities |
| [`nebula-imaya`](https://bitbucket.org/nebulapipeline/nebula-imaya) | Maya utilities |
| [`nebula-maya-loader`](https://bitbucket.org/nebulapipeline/nebula-maya-loader) | Loads scripts into Maya and presents them as a menu |
| [`nebula-ideadline`](https://bitbucket.org/nebulapipeline/nebula-ideadline) | Deadline render-farm integration |
| [`nebula-main`](https://bitbucket.org/nebulapipeline/nebula-main) · [`nebula-pipeline`](https://bitbucket.org/nebulapipeline/nebula-pipeline) | Entry points |
| [`createshots`](https://bitbucket.org/nebulapipeline/createshots) · [`checkoutin`](https://bitbucket.org/nebulapipeline/checkoutin) · [`matteids`](https://bitbucket.org/nebulapipeline/matteids) · [`legacyyaml`](https://bitbucket.org/nebulapipeline/legacyyaml) | Production utilities |
| [`nebula-pipeline-toolbox-docs`](https://bitbucket.org/nebulapipeline/nebula-pipeline-toolbox-docs) | Sphinx documentation, published to Read the Docs |

## What I did not write

This matters as much as the rest, so it is stated plainly rather than buried.

- **TACTIC** is the asset management and production tracking system that Nebula integrates with. It is
  made by [Southpaw Technology](https://www.southpawtech.com/). The `tactic`, `tactic-client`,
  `tacticutils`, `tacticui` and `tacticobjects` repositories in that workspace are TACTIC and its client
  libraries, or thin wrappers around them. They are not my work. Nebula extended TACTIC rather than
  reimplementing it.
- **Qt.py** is Marcus Ottosson's ([mottosso](https://github.com/mottosso/Qt.py)) Qt binding shim, kept
  alongside the pipeline so the same GUI code runs under PySide and PyQt. Not my work.
- **PySide2 and Qt** belong to the Qt Company. **Deadline** belongs to Thinkbox and then AWS.

## Authorship

I designed this pipeline and led the small team that built it between 2019 and 2021.

**Qurban Ali** wrote substantial parts of `nebula-core` and `nebula-gui` under my direction, and
contributed to several other modules. `nebula-ideadline` is entirely my own code and `nebula-imaya` is
nearly so.

The commit history in each repository shows the split honestly. Leading a system and writing every line
of it are different claims, and this repository makes the first one.

## Licence

See each repository for its licence. Nothing in this index repository is a copy of the code; the links
point at the originals.

One module, [`nebula-ideadline`](https://github.com/MagicRedDeer/nebula-ideadline), is also mirrored to
GitHub. It is the one where the entire history is mine, and a render-farm integration reads better with
the file open than behind a link.
