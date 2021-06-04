# Terraform Cloud Agent with Basic Tools

A Dockerfile for building a Terraform Cloud Agent container image that has some basic tools installed:

* curl
* jq

## Build

To build the image, inside this directory run:

```bash
docker build -t tfc-agent-basic-tools .
```