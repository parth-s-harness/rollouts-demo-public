# Use a modern, multi-arch supported base image like Ubuntu 22.04
FROM ubuntu:22.04

# Install the necessary tools directly from the package manager.
# These are pre-compiled and support multiple architectures.
# Also install ca-certificates to avoid any potential SSL issues.
RUN apt-get update && \
    apt-get install -y wrk jq curl ca-certificates && \
    rm -rf /var/lib/apt/lists/*

# Copy the lua script into the image
ADD report.lua .

# Set a working directory
WORKDIR /
