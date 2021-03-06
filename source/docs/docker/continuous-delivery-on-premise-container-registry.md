---
layout: post
title: Setting up continuous delivery with a custom or on-premise container registry
category: Docker
---

[Docker](https://www.docker.com/) brought many good things to the world of
distributed applications and containerization, and one of these things is the
ability to have **your own private container registries** for Docker images.

Setting up your **Custom Registry** with **Semaphore** is pretty straightforward
and quick.

If you haven't already enabled using Docker with your project, be sure to
consult our documentation page on
[setting up continuous integration for a Docker project on Semaphore](/docs/docker/setting-up-continuous-integration-for-docker-project.html),
and enable Docker integrations for your project.

Projects that are set up as **Docker** projects will have container registry
integrations available through project settings.

Configuring the Custom Registry project add-on will enable you to **push** and
**pull** your images without explicitly having to log into your Custom Registry
during builds and deployments. To achieve this, do the following:

  - visit your project on Semaphore and click on "Project settings" in the upper
      right corner of your screen
  - select "Docker Registry"
  - select the "Custom Container Registry" integration

Next, you will be prompted with three input fields:

  - `Username`,
  - `Password`, and
  - `Server` — your custom registry server.

After you have entered your credentials, click "Save". All of your credentials
will be encrypted and saved by Semaphore.

You can now push or pull images from your custom registry through Semaphore.

```
docker push your_registry_address/repository_name
```

Happy building!
