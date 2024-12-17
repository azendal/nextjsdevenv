# Base image
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:22

# Set Node.js version (you can change this as needed)
ENV NODE_VERSION=22

# Install additional dependencies
RUN apt-get update && apt-get install -y \
    curl \
    git \
    sudo \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /workspace

# Install global NPM tools for Next.js
RUN npm install -g create-next-app yarn

# Add a non-root user to avoid permissions issues
USER node

# Expose the Next.js default development port
EXPOSE 3000

CMD [ "bash" ]
