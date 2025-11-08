# Base image: Node 22 on Alpine
FROM node:22-alpine

# Add metadata
LABEL maintainer="abdallaheeid@icloud.com"
LABEL description="Custom Node 22 Alpine image for GitLab CI with Netlify CLI and Playwright support"

# Install system dependencies
# - bash (optional, for debugging)
# - curl and jq (used in deploy steps)
# - git (useful for CI environments)
# - chromium (optional if you run e2e locally)
RUN apk add --no-cache bash curl jq git

# Install global NPM tools
# Netlify CLI for deployment
RUN npm install -g netlify-cli@20.1.1

# Optional: Playwright dependencies (for e2e tests)
# Uncomment if you want one single image for everything
# RUN npx playwright install --with-deps

# Verify installations
# RUN node --version && npm --version && netlify --version && curl --version && jq --version

# Default working directory
# WORKDIR /app

# Copy your code (optional, if you want to test locally)
# COPY . .

# Default command (will be overridden in CI)
# CMD ["node", "--version"]
