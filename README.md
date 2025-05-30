# GIG Cymru NHS Wales - Software development standards

[![mkdocs](https://github.com/Geoff1900/software-development-standards/actions/workflows/publish.yml/badge.svg)](https://github.com/GIG-Cymru-NHS-Wales/software-development-standards/actions/workflows/publish.yml)

This documents in this repository are published to [https://geoff1900.github.io/software-development-standards](https://geoff1900.github.io/software-development-standards/)


## Introduction

When you're building software, especially in healthcare, good guidance really matters. It helps everyone work in a consistent way, so the code is easier to understand, safer, and more reliable. 

A handbook brings together all the important know-how: how to write clear, secure code; how to manage changes properly; how to work well across teams; and how to meet the expectations of modern software development. 

It's there to help you make good decisions, avoid mistakes, and deliver software that others can trust and build on.

## Documentation

Our standards are published using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)

### Running via a Container (Podman / Docker)

Ensure you have [Podman](https://podman.io/) installed first.

```sh
podman build --tag standards .
podman run -p 8000:8000 standards
```

Navigate to ``http://127.0.0.1:8000/``

### Building docs with make

If you are a developer, or you want to generate documentation on your own system, then you can use the command `make`.

To see options for the command `make`:

```sh
make help
```

To do everything to build the documentation and run it:

```sh
make
```

### Building docs manually

Install 'uv' for Python package/env management e.g. :

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Setup the local environment and install dependencies:

```bash
uv sync
```

Run mkdocs locally:

```bash
uv run mkdocs serve
```

Navigate to ``http://127.0.0.1:8000/``

## Licence

This repository is licensed under the [MIT License](LICENSE)
