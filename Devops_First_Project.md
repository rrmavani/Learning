# Linkedin Learning Course
## Devops Foundations: Your First Project
##### by 

* [Create Dockerfile](#create-dockerfile)
* [Create docker-compose](#create-docker-compose)

## Create Dockerfile
```Dockerfile
FROM nginx:alpine
MAINTAINER Rushabh Mavani

COPY website /website
COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
```
Some Commands for docker
```bash
ubuntu@desktop:~/Desktop/ex_files/ExFilesProject/ExerciseFiles/02_02_end$ docker build -t website .
[+] Building 3.5s (9/9) FINISHED                                                                                                                                                                         
 => [internal] load build definition from Dockerfile                                                                                                                                                     0.1s
 => => transferring dockerfile: 38B                                                                                                                                                                      0.0s
 => [internal] load .dockerignore                                                                                                                                                                        0.0s
 => => transferring context: 2B                                                                                                                                                                          0.0s
 => [internal] load metadata for docker.io/library/nginx:alpine                                                                                                                                          2.6s
 => [auth] library/nginx:pull token for registry-1.docker.io                                                                                                                                             0.0s
 => [internal] load build context                                                                                                                                                                        0.0s
 => => transferring context: 16.53kB                                                                                                                                                                     0.0s
 => [1/3] FROM docker.io/library/nginx:alpine@sha256:082f8c10bd47b6acc8ef15ae61ae45dd8fde0e9f389a8b5cb23c37408642bf5d                                                                                    0.0s
 => CACHED [2/3] COPY website /website                                                                                                                                                                   0.0s
 => CACHED [3/3] COPY nginx.conf /etc/nginx/nginx.conf                                                                                                                                                   0.0s
 => exporting to image                                                                                                                                                                                   0.1s
 => => exporting layers                                                                                                                                                                                  0.0s
 => => writing image sha256:46504fe737d0b1edba3edd6b76693699c311b30bbbd61dcd3c936fafbf3b4c11                                                                                                             0.0s
 => => naming to docker.io/library/website                                                                                                                                                               0.0s
```
Check Image created
```bash
ubuntu@desktop:~/Desktop/ex_files/ExFilesProject/ExerciseFiles/02_02_end$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
website       latest    46504fe737d0   3 hours ago     40.3MB
hello-world   latest    feb5d9fea6a5   11 months ago   13.3kB
```
Run Image
```bash
ubuntu@desktop:~/Desktop/ex_files/ExFilesProject/ExerciseFiles/02_02_end$ docker run -p 80:80 website
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
```

Visit http://localhost

![localhost](assets/localhost1.png)

***

# Create docker-compose
```docker
version: '3.7'
services:
  website:
   build:
    context: .
   ports:
    - 80:80
```
Docker compose start website
```bash
ubuntu@desktop:~/Desktop/ex_files/ExFilesProject/ExerciseFiles/02_03_end$ docker-compose up --build
Creating network "02_03_end_default" with the default driver
Building website
[+] Building 2.0s (8/8) FINISHED                                                                                                                                                                              
 => [internal] load build definition from Dockerfile                                                                                                                                                     0.1s
 => => transferring dockerfile: 38B                                                                                                                                                                      0.0s
 => [internal] load .dockerignore                                                                                                                                                                        0.0s
 => => transferring context: 2B                                                                                                                                                                          0.0s
 => [internal] load metadata for docker.io/library/nginx:alpine                                                                                                                                          1.1s
 => [1/3] FROM docker.io/library/nginx:alpine@sha256:082f8c10bd47b6acc8ef15ae61ae45dd8fde0e9f389a8b5cb23c37408642bf5d                                                                                    0.0s
 => [internal] load build context                                                                                                                                                                        0.0s
 => => transferring context: 16.53kB                                                                                                                                                                     0.0s
 => CACHED [2/3] COPY website /website                                                                                                                                                                   0.0s
 => CACHED [3/3] COPY nginx.conf /etc/nginx/nginx.conf                                                                                                                                                   0.0s
 => exporting to image                                                                                                                                                                                   0.1s
 => => exporting layers                                                                                                                                                                                  0.0s
 => => writing image sha256:46504fe737d0b1edba3edd6b76693699c311b30bbbd61dcd3c936fafbf3b4c11                                                                                                             0.0s
 => => naming to docker.io/library/02_03_end_website                                                                                                                                                     0.0s
Creating 02_03_end_website_1 ... done
Attaching to 02_03_end_website_1
website_1  | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
website_1  | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
website_1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
website_1  | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
website_1  | 10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
website_1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
website_1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
website_1  | /docker-entrypoint.sh: Configuration complete; ready for start up
```

Visit http://localhost

![localhost](assets/localhost1.png)
