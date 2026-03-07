FROM python:3.12.13-alpine3.23

ARG IMAGE_VERSION="dev"
ARG IMAGE_CREATED="unknown"
ARG IMAGE_REVISION="unknown"
ARG IMAGE_SOURCE="https://github.com/ThibaudN35/devops-devcontainer"

LABEL org.opencontainers.image.title="devops-devcontainer" \
      org.opencontainers.image.description="Alpine-based DevOps devcontainer" \
      org.opencontainers.image.version="$IMAGE_VERSION" \
      org.opencontainers.image.created="$IMAGE_CREATED" \
      org.opencontainers.image.revision="$IMAGE_REVISION" \
      org.opencontainers.image.authors="Thibaud Naegele" \
      org.opencontainers.image.vendor="Thibaud Naegele" \
      org.opencontainers.image.licenses="MIT" \
      org.opencontainers.image.url="$IMAGE_SOURCE" \
      org.opencontainers.image.source="$IMAGE_SOURCE" \
      org.opencontainers.image.documentation="$IMAGE_SOURCE#readme" \
      org.opencontainers.image.base.name="python:3.12.13-alpine3.23"

ENV VIRTUAL_ENV=/opt/venv \
    PATH=/opt/venv/bin:$PATH \
    PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1 \
    PIP_DISABLE_PIP_VERSION_CHECK=1

WORKDIR /workspace

RUN apk add --no-cache \
    bash=5.2.26-r0 \
    git=2.45.4-r0 \
    openssh-client-default=9.7_p1-r4 \
    curl=8.9.1-r2 \
    jq=1.7.1-r0 \
    yq=4.44.3-r0 \
    shellcheck=0.10.0-r1 \
    make=4.4.1-r2 \
    ca-certificates=20241121-r1 \
 && update-ca-certificates

RUN python -m venv "$VIRTUAL_ENV"

COPY .devcontainer/requirements.txt /tmp/requirements.txt

RUN "$VIRTUAL_ENV/bin/pip" install --no-cache-dir --upgrade \
    pip==24.3.1 \
    setuptools==75.6.0 \
    wheel==0.45.1 \
 && "$VIRTUAL_ENV/bin/pip" install --no-cache-dir -r /tmp/requirements.txt \
 && rm -f /tmp/requirements.txt

RUN addgroup -g 1000 dev \
 && adduser -D -u 1000 -G dev -s /bin/bash vscode \
 && chown -R vscode:dev /workspace "$VIRTUAL_ENV"

USER vscode

CMD ["bash"]