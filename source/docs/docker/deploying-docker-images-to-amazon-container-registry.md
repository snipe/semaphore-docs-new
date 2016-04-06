---
layout: post
title: Deploying Docker images to Amazon EC2 Container Registry
category: Docker
---

[Amazon EC2 Container Registry](https://aws.amazon.com/ecr/) is Docker
container registry for easily managing, storing and deploying Docker images.
It comes from a family of [Amazon Web Services (AWS)](https://aws.amazon.com/)
which sole purpose is on simplifying services you use on the web.
If you don't have AWS account, you can [sign up](https://console.aws.amazon.com/console/home).

Integrating your **Semaphore account** with **Amazon EC2 Container Registry
(ACR)** is very easy and it will take a couple of minutes of your time.

If you haven't set up your project as a **Docker project**, you should consult
[Setting up a continuous integration for a Docker project on Semaphore](/docs/docker/setting-up-continuous-integration-for-docker-project.html)
page in our documentation in order to have Docker integrations available for
your project.

You should definitely set up Amazon EC2 Container Registry (ACR) integration if you
are planning on:

  - **pulling Docker images** from ACR repository,
  - **pushing Docker images** to ACR repository.

This can be done by visiting your project on Semaphore and clicking "Add-ons"
at the upper right corner of your screen.

<img src="" class="img-responsive img-bordered" alt="Click Project Add-ons">

Next, click "Docker integrations".

<img src="" class="img-responsive img-bordered" alt="Click Docker integrations">

Choose "Amazon EC2 Container Registry (ACR)" integration.

<img src="" class="img-responsive img-bordered" alt="Click Amazon Container Registry (ACR)">

Then you will be prompted with three input fields requiring
your:

  - `AWS Access Key ID`,
  - `AWS Secret Access Key`,
  - `AWS Region` - region where your repository resides.

You can find instructions for managing AWS credentials at
[their documentation](http://docs.aws.amazon.com/general/latest/gr/managing-aws-access-keys.html).
You should also consider making an
[IAM user](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html)
for Semaphore.

After you have copied contents, you can click "Test" to see if everything is
OK. If the test is successful you can click "Save".

<img src="" class="img-responsive img-bordered" alt="Successful connection test and Save">

If the credentials you provided are valid, your ACR integration will be saved.
You can now push or pull images on Amazon Container Registry through Semaphore.

Happy building!