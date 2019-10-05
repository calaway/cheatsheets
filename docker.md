# Docker CheatSheet


## Build
Help message
```bash
docker build --help
```

---

Build an image from ./Dockerfile with name `my_image` and tag `latest`.
```bash
docker build [--tag|-t my_image[:latest]] .
```

## Run
Help message
```bash
docker run --help
```

---

Base: `docker run image_name`
```bash
docker run [options] image_name[:tag] [/bin/sh]
```
Start up a container from image `image_name` with tag `tag`. If specified, run the command upon startup.

Options:
```bash
    -rm                   # Remove container automatically after it exits
-e, --env "foo=bar"       # Add env var `foo` with a value of `bar`
    --env-file .env.local # Run image with all env vars contained in `.env.local`
-p, --publish 5000:80     # Expose port 5000 externally and map to port 80 inside the container
-v, --volume ~/dev:/code  # Map volume `~/dev` locally to volume `/code` inside the container
```
