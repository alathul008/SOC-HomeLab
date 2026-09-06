# Docker Lab

The home-server layer uses Docker Compose to run multiple services inside WSL. The original infrastructure contains services for management, networking, monitoring, media, automation, security tooling, and AI workloads.

For the public portfolio, only sanitized configuration belongs here.

## Security Rules

- Never commit `.env` files containing real values.
- Replace passwords, tokens, private addresses, and host-specific paths with variables/placeholders.
- Do not expose Docker socket access without understanding its privilege implications.
- Keep management interfaces restricted to the trusted lab network.

See [`docker-compose.example.yml`](./docker-compose.example.yml) for the sanitized portfolio configuration.
