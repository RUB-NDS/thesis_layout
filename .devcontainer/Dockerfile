FROM mcr.microsoft.com/vscode/devcontainers/java:17-bullseye

# [Optional] Uncomment this section to install additional packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends biber curl git git-lfs latexmk lmodern locales make neovim pandoc procps python3-pip texlive texlive-bibtex-extra texlive-extra-utils texlive-fonts-extra texlive-lang-german texlive-latex-extra texlive-science texlive-xetex && \
    pip3 install Pygments && \
    rm -rf /var/lib/apt/lists/*