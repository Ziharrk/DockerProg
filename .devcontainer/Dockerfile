FROM ubuntu:latest

# Install needed libraries
RUN apt update && apt upgrade -y
RUN apt install make gcc g++ curl -y
RUN apt install libgmp-dev -y

# Set environment variables for non-interactive GHCup installation
ENV BOOTSTRAP_HASKELL_NONINTERACTIVE=1
ENV BOOTSTRAP_HASKELL_INSTALL_HLS=1

# Install GHCup
RUN curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh

# Set the PATH
RUN echo "source /root/.ghcup/env" >> ./root/.bashrc