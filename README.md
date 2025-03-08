# Lilypad Nomic Embed Text

Run [Nomic Embed Text](https://ollama.com/library/nomic-embed-text) on Lilypad Network.

## Getting Started

> Make sure that you Base64 encode your request.

```sh
export WEB3_PRIVATE_KEY=WEB3_PRIVATE_KEY

lilypad run github.com/DevlinRocha/lilypad-nomic-embed-text:baa4a13752fdeb4608de11676aecf13007b15581 \
-i request="$(echo -n '{
  "model": "nomic-embed-text",
  "input": "The sky is blue because of Rayleigh scattering",
  "stream": false,
}' | base64 -w 0)"
```

## Available Scripts

In the project directory, you can run:

### [`scripts/configure`](scripts/configure)

Configures your module.
Sets the following values in the [`.env` file](.env)

```
MODEL_NAME
MODEL_VERSION
DOCKER_HUB_USERNAME
DOCKER_IMAGE
GITHUB_REPO
```

### [`scripts/build [--major] [--minor] [--patch] [--local]`](scripts/build)

Builds the Docker image and pushes it to Docker Hub.

### `--major`, `--minor`, and `--patch` Flags

Increments the specified version before building the Docker image.

#### `--local` Flag

Loads the built Docker image into the local Docker daemon.

### [`scripts/run`](scripts/run)

Runs your module.

## Learn More

To learn more about Lilypad, check out the [Lilypad documentation](https://docs.lilypad.tech/lilypad).
