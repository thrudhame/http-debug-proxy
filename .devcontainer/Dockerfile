# syntax=docker/dockerfile:1.3-labs
FROM denoland/deno:bin AS deno
FROM mcr.microsoft.com/vscode/devcontainers/base:trixie
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get upgrade -y

COPY --from=deno /deno /usr/local/bin/deno
RUN deno --version

EXPOSE 8000

WORKDIR /workspace

USER vscode


