# Meta-ouroboros

meta-ouroboros is a conference demonstration of Yocto Project and
OpenEmbedded tooling. It builds a minimal firmware image with the Podman
runtime and a container image that provides a build environment.

At runtime, the firmware downloads and starts the container. The container
sets up the build environment, runs BitBake to produce the next firmware
image, and makes that image available to SWUpdate. After the system updates
and boots the new firmware, the cycle repeats.

# Dependencies

This layer depends on:
* openembedded-core
* meta-openembedded
* meta-swupdate

This layer is intended to only support the latest LTS, `wrynose`.
