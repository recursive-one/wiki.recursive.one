# Docker

[Docker](https://www.docker.com) is a containerization tool for unix OSes. It implements many ideas of the [Open Container Initiative (OCI)](https://opencontainers.org/) but does that in a *rootful* manner. For the *rootless* containerization one can use the [/Podman]().

# Resources

- ["Docker Security Best Practices from the Dockerfile"](https://cloudberry.engineering/article/dockerfile-security-best-practices/)
- [lazydocker](https://github.com/jesseduffield/lazydocker), a nice TUI app for docker(-compose)
- [awesome-compose](https://github.com/docker/awesome-compose), "These samples provide a starting point for how to integrate different services using a Compose file and to manage their deployment with [Docker Compose](https://docs.docker.com/compose/)."

## hadolint

[hadolint](https://github.com/hadolint/hadolint) is a linter for Dockerfiles. Uses [/Haskell]() powered [shellcheck](https://github.com/koalaman/shellcheck/) under the hood.

Usually, I run hadolint using such script:

```bash
#!/bin/sh

FILE="$(pwd)/Dockerfile"
if [ ! -f "$FILE" ]; then
    echo "Dockerfile not found!"
else
    docker run --rm -i hadolint/hadolint < "$FILE"
fi
```

# Recipies

## Run as a script

Sometimes I need to run some dockerized app from shell having a couple of volumes mounted in "rw" mode. That's how I wrap such calls into shell scripts:

```bash
docker run --rm \
       -u $(id -u):$(id -g) \
       -v "$PWD":/data:rw \
       -e VAR="value" \
       image:latest \
       $*
```

The "`-u $(id -u):$(id -g)`" part keeps you away from problems with permissions.