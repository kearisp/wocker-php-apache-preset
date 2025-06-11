# PHP Apache preset for Wocker

[![Version](https://img.shields.io/badge/version-1.0.3-blue.svg)](https://github.com/kearisp/wocker)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)

A lightweight and efficient preset for developing php applications with the Wocker workspace.


## Installation

You can add this preset to an existing Wocker project:

```shell
ws preset:add php-apache
```


## Features


## Usage

### Initialization Scripts

You can mount a directory with custom initialization scripts that will run on container startup:

```shell
ws volume:mount ./my-scripts:/etc/wocker-init.d
```

Scripts are executed in alphabetical order. Consider using numeric prefixes (e.g., `10-setup.sh`, `20-migrate.sh`) to control execution order.

### Environment Variables

The preset supports common Wocker environment variables, plus:

- `VIRTUAL_PORT`: Default port your php application should listen on (provided by nginx-proxy)


### Docker Image

This preset uses the official php Docker image ([`php`](https://hub.docker.com/_/php)) with Alpine Linux by default. You can change the version: `php`

```shell
ws build-args:set IMAGE_VERSION=latest
```

Available options: `alpine`, `latest`, `slim`, or a specific version like `1.0.11`.

For a complete list of available php versions, see: [https://hub.docker.com/_/php/tags](https://hub.docker.com/_/php/tags)

## Prerequisites

- Docker installed and running
- Wocker CLI installed
- Basic understanding of php

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

_This preset is part of the [Wocker](https://kearisp.github.io/wocker) ecosystem._
