FROM mcr.microsoft.com/devcontainers/base:bookworm

USER vscode

# Create tmp dir
RUN mkdir -p /home/vscode/tmp-workspace
WORKDIR /home/vscode/tmp-workspace

# Install Scala with cs setup
# See https://get-coursier.io/docs/cli-installation#linux
RUN curl -fL "https://github.com/VirtusLab/coursier-m1/releases/latest/download/cs-aarch64-pc-linux.gz" | gzip -d > cs && \
  chmod +x cs && \
  # See https://get-coursier.io/docs/cli-setup
  ./cs setup --user-home /home/vscode --jvm 17 --yes

RUN rm -R /home/vscode/tmp-workspace
