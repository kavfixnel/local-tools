FROM node:23.3.0-slim AS builder

# Set the working directory inside the container
WORKDIR /build

# Install git and pnpm
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/* && npm install -g pnpm

RUN git clone https://github.com/andygock/diff-text.git .

# Install dependencies
RUN pnpm install && pnpm build

FROM nginx

COPY --from=builder /build/dist /usr/share/nginx/html

