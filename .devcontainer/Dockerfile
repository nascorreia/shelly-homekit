# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.209.6/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version (use hirsuite or bionic on local arm64/Apple Silicon): hirsute, focal, bionic
ARG VARIANT="22.04"
FROM mcr.microsoft.com/devcontainers/base:ubuntu-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends clang-format make software-properties-common
RUN add-apt-repository ppa:mongoose-os/mos && apt-get update && apt-get -y install mos-latest libavahi-client3 avahi-daemon clang
