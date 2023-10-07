FROM mcr.microsoft.com/vscode/devcontainers/base:debian-11

# [Optional] Uncomment this section to install additional packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends openjdk-17-jdk biber curl git git-lfs latexmk lmodern locales make neovim pandoc procps python3-pip texlive texlive-bibtex-extra texlive-extra-utils texlive-fonts-extra texlive-lang-german texlive-latex-extra texlive-science texlive-xetex && \
    pip3 install Pygments && \
    rm -rf /var/lib/apt/lists/*

RUN sudo mv /usr/lib/jvm/java-17-openjdk-* /usr/lib/jvm/java-17-openjdk