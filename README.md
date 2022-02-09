# Data Science Ultimate Docker image

[![Docker Hub: franzdiebold/datascience-ultimate](https://img.shields.io/badge/Docker%20Hub-franzdiebold%2Fdatascience--ultimate-2496ed)](https://hub.docker.com/r/franzdiebold/datascience-ultimate)
[![GitHub: FranzDiebold/docker-datascience-ultimate](https://img.shields.io/badge/GitHub-FranzDiebold%2Fdocker--datascience--ultimate-0969da)](https://github.com/FranzDiebold/docker-datascience-ultimate)
[![GitHub](https://img.shields.io/github/license/FranzDiebold/docker-datascience-ultimate)](./LICENSE)

> [This docker image] is all you need :wink:

A customized [JupyterLab](https://jupyter.org/) [Spark](https://spark.apache.org/docs/latest/api/python/) [Docker](https://www.docker.com/) image.

![docker-datascience-ultimate Screenshot](images/datascience-ultimate_screenshot.png)

## What's in?

- Everything from [jupyter/all-spark-notebook](https://hub.docker.com/r/jupyter/all-spark-notebook)
  - [Python v3.9](https://www.python.org/)
  - [Scala v2.12](https://www.scala-lang.org/) (via `spylon-kernel`)
  - [R v4.1](https://www.r-project.org/)
  - [Spark v3.2](https://spark.apache.org/docs/latest/api/python/)
  - [JupyterLab v3.2](https://jupyter.org/)
  - [Pandas v1.4](https://pandas.pydata.org/)
  - [Numpy v1.21](https://numpy.org/)
- More packages:
  - [Plotly v5.5](https://plotly.com/python/)
  - [Polars v0.12](https://www.pola.rs/)
  - [Git](https://git-scm.com/) support
- Theme: [JupyterLab Darkside UI](https://github.com/dunovank/jupyterlab_darkside_ui)

## How to use?

```bash
docker run -p 8888:8888 -p 4040:4040 franzdiebold/datascience-ultimate
```

The following web apps will be available:

- JupyterLab: [http://localhost:8888/lab/](http://localhost:8888/lab/)
- Spark Web UI: [http://localhost:4040/](http://localhost:4040/)

## Use it in your daily routine :rocket:

In your `.zshrc` / `.bashrc` file add:

```bashrc
alias jupyter='docker run --rm -p 8888:8888 -p 4040:4040 -v "${PWD}":/home/jovyan franzdiebold/datascience-ultimate:latest'
```

## Build image locally

```bash
make build
```
