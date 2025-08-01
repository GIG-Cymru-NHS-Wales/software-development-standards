# GIG Cymru NHS Wales - Software development standards

[![mkdocs](https://github.com/GIG-Cymru-NHS-Wales/software-development-standards/actions/workflows/publish.yml/badge.svg)](https://github.com/GIG-Cymru-NHS-Wales/software-development-standards/actions/workflows/publish.yml)

The documents in this repository are published to [https://gig-cymru-nhs-wales.github.io/software-development-standards/](https://gig-cymru-nhs-wales.github.io/software-development-standards/).

## Introduction

When you're building software, especially in healthcare, good guidance really matters. It helps everyone work in a consistent way, so the code is easier to understand, safer, and more reliable.

A handbook brings together all the important know-how: how to write clear, secure code; how to manage changes properly; how to work well across teams; and how to meet the expectations of modern software development.

It's there to help you make good decisions, avoid mistakes, and deliver software that others can trust and build on.

## Getting Started

There are several ways to set up your development environment:

### 1. GitHub Codespaces (Recommended)

The fastest way to start contributing:

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/GIG-Cymru-NHS-Wales/software-development-standards?quickstart=1)

This provides:

* A pre-configured VS Code environment (with useful extensions installed)
* All required dependencies installed
* Automatic port forwarding for preview
* Git integration

Once you have successfully launched Codespaces you can run the
development server from the VS Code Terminal:

```bash
    uv run mkdocs serve
```

You will be prompted to **Open in Browser** to view the locally running site.

See the [Quickstart Guide](http://docs.github.com/en/codespaces/quickstart) for
more information.

Note: It can take a few minutes to fully launch Codespaces the first time, but
is faster on subsequent launches as the environment is then cached.

### 2. Local Development

**Prerequisites:**

* Python 3.11 or higher
* [uv](https://github.com/astral-sh/uv) for package/env management
* Git

**Setup Steps:**

Clone the repository:

```bash
    git clone https://github.com/GIG-Cymru-NHS-Wales/software-development-standards.git
    cd software-development-standards
```

Install uv (if not already installed):

```bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
```

Set up environment and dependencies:

```bash
    uv sync
```

Start the development server:

```bash
    uv run mkdocs serve
```

View the documentation at: ``http://127.0.0.1:8000/``

### 3. Container-based Development

If you prefer using containers:

**Prerequisites:**

* [Podman](https://podman.io/) or [Docker](https://www.docker.com/)

**Setup Steps:**

Build the container:

```bash
    podman build --tag mkdocs .
```

Run the development server:

```bash
    podman run -p 8000:8000 mkdocs
```

View the documentation at: ``http://127.0.0.1:8000/``

### 4. Make-based Workflow

For those familiar with Make:

```bash
    # See available commands
    make help

    # Full build and serve
    make
```

View the documentation at: ``http://127.0.0.1:8000/``

## Documentation

Our documentation is built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Contributing

1. Choose your preferred development environment from above
2. Create a new branch for your changes
3. Make your changes
4. Test your changes locally
5. Submit a Pull Request

## Licence

This repository is licensed under the [MIT Licence](LICENCE)
