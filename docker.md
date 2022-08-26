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
    --rm                      # Remove container automatically after it exits
-e, --env foo1=bar1 foo2=bar2 # Add a list of env vars in key=value pairs
    --env-file .env.local     # Run image with all env vars contained in `.env.local`
-p, --publish 5000:80         # Expose port 5000 externally and map to port 80 inside the container, accepts a list
-v, --volume `pwd`:/code      # Map the local current directory to the directory `/code` inside the container, accepts a list
-d, --detach                  # Run container in background and print container ID
-it, --interactive --tty      # Connect container to terminal to execute commands interactively
```
