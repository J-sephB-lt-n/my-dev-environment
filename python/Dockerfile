# Use the official lightweight Python image #
# https://hub.docker.com/_/python #
FROM python:3.12

# Copy local code to the container image #
WORKDIR /src/
COPY . ./

# Install linux packages #
RUN apt update
RUN apt install neovim tree -y
RUN sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.1.5/zsh-in-docker.sh)"

# Install python dependencies #
RUN pip install --no-cache-dir -r requirements.txt
