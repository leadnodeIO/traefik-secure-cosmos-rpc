# Traefik Secure Cosmos RPC

Traefik Secure Cosmos RPC is a middleware designed to publicly expose RPC endpoints for Cosmos-based blockchain networks, leveraging Traefik to add essential features like automatic SSL for secure communication and rate limiting to prevent abuse.

## Configuration

### Dynamic Configuration

The dynamic configuration for Traefik is defined in the `dynamic_conf.yml` file located at `config/traefik/dynamic_conf.yml`. This file specifies the routing rules, middlewares, and services for the Traefik instance.

### Docker Compose

The Docker Compose file (`docker-compose.yml`) defines the Traefik service configuration, including Docker provider settings and volumes.

### Environment Variables

Ensure to provide the necessary environment variables in the `.env` file to configure Traefik and the RPC endpoints.

## Usage

1. Ensure Docker and Docker Compose are installed on your system.
2. Customize the `.env` file with your configuration details, particularly `LE_EMAIL` and `DOMAIN`.
3. Optionally, modify `RPC_PORT` and the rate limit settings if necessary.
4. Run `docker-compose up -d` to start the Traefik service.
5. Traefik will automatically handle SSL termination and rate limiting for your Cosmos RPC endpoints.
6. Monitor Traefik logs and metrics to ensure smooth operation.

With Traefik Secure Cosmos RPC, you can securely expose your Cosmos RPC endpoints to the world while preventing abuse through rate limiting. Enjoy enhanced security and ease of configuration with Traefik.
