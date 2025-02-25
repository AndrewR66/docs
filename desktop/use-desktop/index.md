---
description: Understand what you can do with Docker Dashboard
keywords: Docker Dashboard, manage, containers, gui, dashboard, images, user manual, whale menu
title: Explore Docker Desktop
redirect_from:
- /desktop/dashboard/
---

When you open Docker Desktop, the Docker Dashboard displays.

![Docker Dashboard on Containers view](../images/dashboard.PNG){:width="750px"}

The **Containers** view provides a runtime view of all your containers and applications. It allows you to interact with containers and applications, and manage the lifecycle of your applications directly from your machine. This view also provides an intuitive interface to perform common actions to inspect, interact with, and manage your Docker objects including containers and Docker Compose-based applications. For more information, see [Explore running containers and applications](container.md).

The **Images** view displays a list of your Docker images and allows you to run an image as a container, pull the latest version of an image from Docker Hub, and inspect images. It also displays a summary of image vulnerabilities. In addition, the **Images** view contains clean-up options to remove unwanted images from the disk to reclaim space. If you are logged in, you can also see the images you and your organization have shared on Docker Hub. For more information, see [Explore your images](images.md).

The **Volumes** view displays a list of volumes and allows you to easily create and delete volumes and see which ones are being used. For more information, see [Explore volumes](volumes.md).

The **Learning center** view helps you get started with quick in-app walkthroughs and other resources for learning about Docker. 

For a more detailed guide about getting started, see
[Get started](../../get-started/index.md).

The **Builds** view, currently in beta, lets you inspect your build history and manage builders. By default, it displays a list of all your ongoing and completed builds. [Explore builds](builds.md).

In addition, the Docker Dashboard allows you to:

- Navigate to the **Settings** menu to configure your Docker Desktop settings. Select the **Settings** icon in the Dashboard header.
- Access the **Troubleshoot** menu to debug and perform restart operations. Select the **Troubleshoot** icon in the Dashboard header.

## Quick search

From the Docker Dashboard you can use Quick Search, which is located in the Dashboard header, to search for:

- Any container or Compose application on your local system. You can see an overview of associated environment variables or perform quick actions, such as start, stop, or delete.

- Public Docker Hub images, local images, and images from remote repositories. Depending on the type of image you select, you can either pull the image by tag, view documentation, go to Docker Hub for more details, or run a new container using the image.

- Extensions. From here, you can learn more about the extension and install it with a single click. Or, if you already have an extension installed, you can open it straight from the search results.

- Any volume. From here you can view the associated container.

- Docs. Find help from Docker's official documentation straight from Docker Desktop. 

## The Docker menu

Docker Desktop also provides an easy-access tray icon that appears in the taskbar and is referred to as the Docker menu ![whale menu](../../assets/images/whale-x.svg){: .inline}.

To display the Docker menu, select the ![whale menu](../../assets/images/whale-x.svg){: .inline} icon. It displays the following options:

- **Dashboard**. This takes you to the Docker Dashboard.
- **Sign in/Create Docker ID**
- **Settings**
- **Check for updates**
- **Troubleshoot**
- **Give feedback**
- **Switch to Windows containers** (if you're on Windows)
- **About Docker Desktop**. Contains information on the versions you are running, and links to the Subscription Service Agreement for example.
- **Learning center**
- **Docker Hub**
- **Documentation**
- **Extensions**
- **Kubernetes**
- **Pause**
- **Restart**
- **Quit Docker Desktop**
