Current working Goal:

Nginx proxy to node setup in compose

---
Let's just get a basic nginx container running.

Start by pulling the image. I like to queue up pulling images when I know I'm on
a fast network.

Also, we'll pull the alpine linux image, since it's much smaller, and we aren't
going to do anything too crazy, yet.

```bash
docker pull nginx:alpine
```

Next, you can run the image with:

```bash
docker run --name webserver -p 80:80 --rm -it nginx:alpine
```

Now you will have a working nginx server at localhost

**Note**: This is ephemeral. You can get into the container to poke around with the
following run in a new terminal:

```bash
docker exec -it webserver /bin/bash
```

Once you kill that first terminal, the container will stop, and will be destroyed.

Any changes made while inside the container will be lost. Containers are ephemeral, unless
explicit data persistence is defined using volumes.
