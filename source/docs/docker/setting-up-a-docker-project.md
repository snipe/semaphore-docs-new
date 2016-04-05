---
layout: post
title: Setting up a Docker project on Semaphore
category: Docker
---

Setting up continuous integration for your Docker project and running your
first build on Semaphore is easy and intuitive.

If you don't already have a Semaphore account, you can [sign_up](/users/sign_up)
and confirm your email address. The free account gives you unlimited CI
service for open-source projects and up to 100 private builds per month.

After you have signed in on Semaphore for time, a welcome screen will prompt
you to add your first project. Click "Build a new Project" button to get
started.

<img src="/docs/assets/img/adding-new-project/build-new-project.png" class="img-responsive img-bordered">

If you already have some projects on Semaphore, you can easily add new project
by clicking "Add new project" button.

#### "Add new project" screenshot

If the next step prompts you to connect your Semaphore account with your
GitHub/Bitbucker account, please consult
[adding your GitHub or Bitbucket project to Semaphore](/adding-github-bitbucket-project-to-semaphore.html)
page in docs which explains it in details.

After you have connected your version control account with your Semaphore
account, Semaphore will list all the project you can add. You can select one
from the list.

<img src="/docs/assets/img/adding-new-project/select-project.png" class="img-responsive img-bordered">

Next, select a branch you would like to build. Semaphore will automatically
test every new branch you create, and remove the ones you delete in origin.
Additional preexisting branches can be easily added from your project page
later on.

<img src="/docs/assets/img/adding-new-project/select-branch.png" class="img-responsive img-bordered">

After that, Semaphore will perform a quick analysis of the source code and
it will recognize presence of your `Dockerfile` or `docker-compose.yml`. This
will generate a set of working build commands depending on your project's
programming language which you will see later on.

#### "Analysis results" screenshot

Next, Semaphore will prompt you to choose a platform for you project based on
the project analysis. If you have `Dockerfile` or `docker-compose.yml` in your
project, Semaphore will recommend you a "Docker" option. Click on "Docker"
option. You can change the platform later in the project's settings page.

#### "Docker platform" sceenshot

Once you have chosen a platform, you can add your container registry host.
We support:
 - Docker Hub
 - Amazon EC2 Container Registry (ECR)
 - Google Container Registry (GCR)
 - Quay.io
 - Any private registry you use

This step is optional, so if you don't use any of the above you can click
"Skip this step" link and proceed.

#### "Container registry hosts" screenshot

If your project needs to run commands that are different from what Semaphore has
suggested, just use the commands editor to customize them to your needs.

At this point, you'll be ready to launch your first Docker build. Click on
"Build With These Settings" to do so. If all goes well, you should see your
first successful build on Semaphore.

<img src="/docs/assets/img/adding-new-project/green-build.png" class="img-responsive img-bordered">