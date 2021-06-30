---
categories: TODO
...
# Podman

[Podman](https://opencontainers.org/)

# Tooling

- [podman-compose](https://github.com/containers/podman-compose), "An implementation of `docker-compose` with Podman backend. The main objective of this project is to be able to run `docker-compose.yml` unmodified and **rootless**."

# Resources

- ["Transitioning from Docker to Podman"](https://developers.redhat.com/blog/2020/11/19/transitioning-from-docker-to-podman/)

# Cookbook

## Kernel namespaces feature

```bash
echo 'kernel.unprivileged_userns_clone=1' | sudo tee /etc/sysctl.d/userns.conf
```

## Registries

- `~/.config/containers/policy.json`

    ```json
    {
        "default": [
            {
                "type": "insecureAcceptAnything"
            }
        ],
        "transports":
            {
                "docker-daemon":
                    {
                        "": [{"type":"insecureAcceptAnything"}]
                    }
            }
    }
    ```
- `~/.config/containers/registries.conf`

    ```ini
    unqualified-search-registries = ['docker.io']
    ```