FROM node:18.16.0-alpine
# See https://docs.aws.amazon.com/amplify/latest/userguide/custom-build-image.html
# to find required dependencies for amplify to run
RUN apk add --no-cache \
    # libc6 is needed to build turbo https://github.com/vercel/turbo/blob/main/examples/with-docker/apps/api/Dockerfile
    libc6-compat \
    gcompat \
    git \
    git-lfs \
    curl \
    openssh

RUN npm install -g @aws-amplify/cli@12.0.3 --unsafe-perm=true
