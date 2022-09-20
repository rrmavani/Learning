# Terraform in docker

- Create a `terraform.dockerfil`
```docker
FROM alpine
MAINTAINER RUSHABH MAVANI

RUN apk add --no-cache ca-certificates curl unzip 
RUN wget -O /tmp/terraform.zip https://releases.hashicorp.com/terraform/1.2.9/terraform_1.2.9_linux_amd64.zip
RUN unzip -u /tmp/terraform.zip -d /

USER nobody
ENTRYPOINT [ "/terraform" ]
```
<br>

- Update docker compose
```docker
  terraform:
    build:
      context: .
      dockerfile: terraform.dockerfile
```
<br>

- Build terraform Image
```bash
buntu@desktop:~/Desktop/ex_files/work$ docker-compose build terraform
Building terraform
[+] Building 15.2s (8/8) FINISHED                                                                                                             
 => [internal] load build definition from terraform.dockerfile                                                                           0.1s
 => => transferring dockerfile: 333B                                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                        0.1s
 => => transferring context: 2B                                                                                                          0.0s
 => [internal] load metadata for docker.io/library/alpine:latest                                                                         0.0s
 => [1/4] FROM docker.io/library/alpine                                                                                                  0.0s
 => CACHED [2/4] RUN apk add --no-cache ca-certificates curl unzip                                                                       0.0s
 => [3/4] RUN wget -O /tmp/terraform.zip https://releases.hashicorp.com/terraform/1.2.9/terraform_1.2.9_linux_amd64.zip                 11.1s
 => [4/4] RUN unzip -u /tmp/terraform.zip -d /                                                                                           2.5s 
 => exporting to image                                                                                                                   0.8s 
 => => exporting layers                                                                                                                  0.8s 
 => => writing image sha256:aebd986271cd5cfb6a2819a2b2a1dfeb4d7a3a629931ac4337b290ef10686961                                             0.0s 
 => => naming to docker.io/library/work_terraform               
```

- Run terraform command
```bash
buntu@desktop:~/Desktop/ex_files/work$ docker-compose run --rm terraform
Creating work_terraform_run ... done
Usage: terraform [global options] <subcommand> [args]

The available commands for execution are listed below.
The primary workflow commands are given first, followed by
less common or more advanced commands.
.....< snip >........
Global options (use these before the subcommand, if any):
  -chdir=DIR    Switch to a different working directory before executing the
                given subcommand.
  -help         Show this help output, or the help for a specified subcommand.
  -version      An alias for the "version" subcommand.
ERROR: 127
```