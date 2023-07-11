# Deprecated. Use [squashfs-container](https://github.com/queeup/squashfs-container) instead.

## mksquashfs in a container

## Pull

```bash
podman pull docker.io/queeup/mksquashfs-container

# OR

podman pull ghcr.io/queeup/mksquashfs-container
```

## Use

```bash
podman run \
    --rm \
    --volume `pwd`:/build \
    --workdir /build \
    --interactive \
    --tty \
    mksquashfs-container \
    system.new SYSTEM.new -noappend -comp zstd -Xcompression-level 19 -b 1048576
```

## Build

```bash
podman build -t mksquashfs-container --file Containerfile
```
