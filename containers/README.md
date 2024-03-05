# Containers

## Development tools

- [Rancher Desktop](https://rancherdesktop.io/)
  - Easy to use desktop container mangement and Kubernetes for
    macOS, Linux and Windows. Kubernetes can be disabled and it just used
    as a container-development environment that provides `docker` etc out of the
    box.
- [Podman Desktop](https://podman-desktop.io/)
  - [Podman](https://podman.io/) based desktop-container development.
- [Lima](https://lima-vm.io/) with [Nerdctl](https://github.com/containerd/nerdctl)
  - Lima offers Linux VMs. Used by Rancher Desktop
  - Nerdctl offers a docker-compatible CLI for containerd and works well with
    Lima.

## Container registries

- [Quay.io](https://quay.io/search)
  - Public container repository provided by RedHat.
  - Alternative to [Docker Hub](https://hub.docker.com/) that introduced rate
    limits in [November 2020](https://www.docker.com/blog/what-you-need-to-know-about-upcoming-docker-hub-rate-limiting/).
  - Quay can self-hosted for [internal registries](https://docs.projectquay.io/welcome.html).
  - Pull from quay.io by prefixing the `organization/image` name with the domain:
    `docker pull quay.io/organization/image`.
- [GitHub](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)
  provides support for uploading Docker and OCI containeer images.
