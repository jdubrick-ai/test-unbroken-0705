# Deploying Locally

This document is intended for users who wish to deploy their application locally. This was generated from a software template and information regarding building and pushing container images can be found below. 

## Prerequisite

You have chosen `quay.io` as your desired image registry. Please ensure you are logged in and can read/write images from that repository. For example using `quay.io` you can run this command to prompt the entering of credentials:
```
podman login quay.io
```

## Building and Pushing Image

To rebuild images you can run the following command from the root of the repository:
```
bash deployment/build_and_push.sh <absolute path to docker/containerfile>
```

This script requries you to provide the absolute path to your docker/containerfile as an argument. The script will perform both the building of the image as well as pushing it to the registry location you specified as part of the developer hub setup for this application. You can view the templated values in `build_and_push.sh`.