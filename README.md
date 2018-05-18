# Armut.com - .NET Core docker images

This repo contains the base Docker images for working with .NET Core and the .NET Core Tools based on Ubuntu images. Since the Armut.com developer team already uses these images, they will keep the images up to date and maintain it.

## Builds status
|       | Linux |
|-------|-------|
| Build | [![Build Status](https://travis-ci.com/armutcom/docker-dotnet-core-images.svg?branch=master)](https://travis-ci.com/armutcom/docker-dotnet-core-images)     | 

# Complete set of Tags

## Ubuntu Xenial (16.04) amd64 tags
- .NET Core Runtime Deps 2.0 : [`2.0.7-deps-xenial` (*2.0/ubuntu-16.04/dotnet-core/runtime-deps/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-16.04/dotnet-core/runtime-deps/Dockerfile)
- .NET Core Runtime 2.0 : [`2.0.7-xenial`, `xenial-latest` (*2.0/ubuntu-16.04/dotnet-core/runtime/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-16.04/dotnet-core/runtime/Dockerfile)
- .NET Core Sdk 2.0 : [`2.1.200-runtime-2.0.7-xenial` (*2.0/ubuntu-16.04/dotnet-core/sdk/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-16.04/dotnet-core/sdk/Dockerfile)
- ASP.NET Core 2.0 : [`2.0.8-xenial`, `xenial-latest` (*2.0/ubuntu-16.04/aspnet-core/runtime/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-16.04/aspnet-core/runtime/Dockerfile)
- ASP.NET Core Build 2.0 : [`2.0.8-sdk-2.1.200-build-xenial`, `build-xenial-latest` (*2.0/ubuntu-16.04/aspnet-core/build/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-16.04/aspnet-core/build/Dockerfile)

## Ubuntu Bionic (18.04) amd64 tags
- .NET Core Runtime Deps 2.0 : [`2.0.7-deps-bionic` (*2.0/ubuntu-18.04/dotnet-core/runtime-deps/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-18.04/dotnet-core/runtime-deps/Dockerfile) 
- .NET Core Runtime 2.0 : [`2.0.7-bionic`, `bionic-latest`, `latest` (*2.0/ubuntu-18.04/dotnet-core/runtime/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-18.04/dotnet-core/runtime/Dockerfile)
- .NET Core Sdk 2.0 : [`2.1.200-runtime-2.0.7-bionic`, `latest`(*2.0/ubuntu-18.04/dotnet-core/sdk/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-18.04/dotnet-core/sdk/Dockerfile)
- ASP.NET Core 2.0 : [`2.0.8-bionic`, `bionic-latest`, `latest` (*2.0/ubuntu-18.04/aspnet-core/runtime/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-18.04/aspnet-core/runtime/Dockerfile)
- ASP.NET Core Build 2.0 : [`2.0.8-sdk-2.1.200-build-bionic`, `build-bionic-latest`, `build-latest`, `build` (*2.0/ubuntu-18.04/aspnet-core/build/Dockerfile*)](https://github.com/armutcom/docker-dotnet-core-images/blob/master/2.0/ubuntu-18.04/aspnet-core/build/Dockerfile)

## Image variants

The `armutcom/dotnet-core-runtime/`, `armutcom/dotnet-core-sdk/`, `armutcom/aspnet-core/` images come in different flavors, each designed for a specific use case.

### `armutcom/aspnet-core:<version>-<os>`

This image contains the ASP.NET Core and .NET Core runtimes and libraries and is optimized for running ASP.NET Core apps in production

### `armutcom/dotnet-core-runtime:<version>-<os>`

This image contains the .NET Core runtimes and libraries and is optimized for running .NET Core apps in production.

### `armutcom/dotnet-core-sdk:<sdk-version>-runtime-<runtime-version>-<os>`

This is the defacto image. If you are unsure about what your needs are, you probably want to use this one. It is designed to be used both as a throw away container (mount your source code and start the container to start your app), as well as the base to build other images off of.

It contains the .NET Core SDK which is comprised of two parts:

1. .NET Core CLI
1. .NET Core
1. ASP.NET Core

Use this image for your development process (developing, building and testing applications).

### `armutcom/dotnet-core-runtime:<version>-deps-<os>`

This image contains the native dependencies needed by .NET Core. It does not include .NET Core. It is for  [self-contained](https://docs.microsoft.com/dotnet/articles/core/deploying/index) applications.

### `armutcom/aspnet-core:<aspnet-version>-sdk-<sdk-version>-build-<os>`

This is the build image. It is designed to be used both as a throw away container (mount your source code and start the container to start your app), as well as the base to build other images off of.

It contains the both .NET Core SDK which is comprised of two parts and Node.js:

1. .NET Core CLI
1. .NET Core
1. ASP.NET Core
1. Node.js 8.11.2

Use this image for your development process (developing, building and testing applications).

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/armutcom/docker-dotnet-core-images/issues).

## Licenses
Licensed under MIT, see [LICENSE](LICENSE) for the full text.

* [.NET Core license](https://github.com/dotnet/dotnet-docker/blob/master/LICENSE)

## Armut.com - .NET Core Docker Hub repos:

* [armutcom/aspnet-core](https://hub.docker.com/r/armutcom/aspnet-core/) for ASP.NET Core images.
* [armutcom/dotnet-core-runtime](https://hub.docker.com/r/armutcom/dotnet-core-runtime/) for .NET Core images.
* [armutcom/dotnet-core-sdk](https://hub.docker.com/r/armutcom/dotnet-core-sdk/) for .NET Core SDK images.

## Official Microsoft Hub repos :

.NET Core Docker Hub repos:

* [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) for ASP.NET Core images.
* [microsoft/dotnet-nightly](https://hub.docker.com/r/microsoft/dotnet-nightly/) for .NET Core preview images.
* [microsoft/dotnet-samples](https://hub.docker.com/r/microsoft/dotnet-samples/) for .NET Core sample images.

.NET Framework Docker Hub repos:

* [microsoft/aspnet](https://hub.docker.com/r/microsoft/aspnet/) for ASP.NET Web Forms and MVC images.
* [microsoft/dotnet-framework](https://hub.docker.com/r/microsoft/dotnet-framework/) for .NET Framework images.
* [microsoft/dotnet-framework-build](https://hub.docker.com/r/microsoft/dotnet-framework-build/) for building .NET Framework applications with Docker.
* [microsoft/dotnet-framework-samples](https://hub.docker.com/r/microsoft/dotnet-framework-samples/) for .NET Framework and ASP.NET sample images.