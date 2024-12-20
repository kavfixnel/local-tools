# Local Tools

Just a set of helpful tools with Web UIs all strung together with docker-compose
for ease of spinning this up

Corrently the following tools are included:
- [Homer](https://github.com/bastienwirtz/homer) to give a nice entrypoint
- [diff-text](https://github.com/andygock/diff-text) for compase text blobs
- [hound-search](https://github.com/hound-search/hound) for searching through git repos quickly

The project is structured simply:
- The configs/ folder contains all the configs for the tools
- Other folders have the build information for building and running that tool
- The contral docker-compose.yaml file ties everything together

## Running all tools

```shell
docker compose up -d
```

then, access http://localhost:80

