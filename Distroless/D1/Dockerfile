FROM ubuntu AS build
# image includes a minimal Ubuntu OS, dont have development tools
# "AS build" is something like label for later use

RUN apt-get update && apt-get install -y golang-go
# updates everything and install go in container.

ENV GO111MODULE=off
# disable Go modules

COPY . .
# copy from current DIR to the container

RUN CGO_ENABLED=0 go build -o /app .
# compile the go application, specifies location, use files in the current DIR

ENTRYPOINT ["/app"]
# /app will execute when container is launched
