* [Create Basic Unit Test File](#create-basic-unit-test-file)
* [Create Dockerfile](#create-dockerfile)
* [Modify Docker compose](#modify-docker-compose)


## Create Basic Unit Test File
Go to your code and create test folder structure
```bash
$ mkdir spec
$ cd spec
/spec$ mkdir unit
/spec$ cd unit/
/spec/unit$ vim page_spec.rb
```
Write test
```ruby
require 'capybara'
require 'capybara./dsl'

describe "Example page render unit tests" do
  it "Shows the Explore California logo" do
  end
end
```

## Create Dockerfile

```docker
FROM ruby:alpine
MAINTAINER Carlos Nunez <dev@carlosnunez.me>

RUN apk add --no-cache build-base ruby-nokogiri
RUN gem install rspec capybara selenium-webdriver
ENTRYPOINT [ "rspec" ]
```

## Modify Docker compose
```docker
  unit-tests:
    volumes:
      - "$pwd:/app"
    build:
      context: .
      dockerfile: rspec.dockerfile
    command:
      - --pattern
      - /app/spec/unit/*_spec.rb
```
<details>
  <summary>Full File</summary>
  docker-compose.yml

  ```docker
  version: '3.7'
  services:
    website:
      build:
        context: .
      ports:
        - 80:80
    unit-tests:
      volumes:
        - "$pwd:/app"
      build:
        context: .
        dockerfile: rspec.dockerfile
    command:
      - --pattern
      - /app/spec/unit/*_spec.rb

  ```
</details>


## Start first test

Make website up

```bash
ubuntu@desktop:~/Desktop/ex_files/work$ docker-compose up -d --build website
Building website
[+] Building 4.3s (9/9) FINISHED                                                                                                              
 => [internal] load build definition from Dockerfile                                                                                     0.1s
 => => transferring dockerfile: 180B                                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                        0.1s
 => => transferring context: 2B                                                                                                          0.0s
 => [internal] load metadata for docker.io/library/nginx:alpine                                                                          2.7s
 => [auth] library/nginx:pull token for registry-1.docker.io                                                                             0.0s
 => [1/3] FROM docker.io/library/nginx:alpine@sha256:082f8c10bd47b6acc8ef15ae61ae45dd8fde0e9f389a8b5cb23c37408642bf5d                    0.0s
 => [internal] load build context                                                                                                        0.8s
 => => transferring context: 16.82MB                                                                                                     0.7s
 => CACHED [2/3] COPY website /website                                                                                                   0.0s
 => CACHED [3/3] COPY nginx.conf /etc/nginx/nginx.conf                                                                                   0.0s
 => exporting to image                                                                                                                   0.0s
 => => exporting layers                                                                                                                  0.0s
 => => writing image sha256:46504fe737d0b1edba3edd6b76693699c311b30bbbd61dcd3c936fafbf3b4c11                                             0.0s
 => => naming to docker.io/library/work_website                                                                                          0.0s
Creating work_website_1 ... done

ubuntu@desktop:~/Desktop/ex_files/work$ docker images
REPOSITORY     TAG       IMAGE ID       CREATED         SIZE
work_website   latest    46504fe737d0   2 days ago      40.3MB
hello-world    latest    feb5d9fea6a5   11 months ago   13.3kB

```
Visit http://localhost

![localhost](assets/localhost1.png)

## Run Basic Test
Now run unit test with `-rm` option. It will remove container once execution completed.

```bash
ubuntu@desktop:~/Desktop/ex_files/work$ docker-compose run --rm unit-tests
Building unit-tests
Step 1/5 : From ruby:alpine
alpine: Pulling from library/ruby
213ec9aee27d: Already exists
20b722058550: Pull complete
4e4edad8fe58: Pull complete
05c438b754fc: Pull complete
e543eab4b71b: Pull complete
Digest: sha256:499a310e8fab835ad47ab6251302aba1fd6ba91ebdfa22d621f495a5d0ded170
Status: Downloaded newer image for ruby:alpine
 ---> 6c65fdec191f
Step 2/5 : MAINTAINER Rushabh Mavani <rrmavani@gmail.com>
 ---> Running in 17a33e32ad45
Removing intermediate container 17a33e32ad45
 ---> 138929e5baa1
Step 3/5 : RUN apk add --no-cache build-base ruby-nokogiri
 ---> Running in 48218a584c4b
fetch https://dl-cdn.alpinelinux.org/alpine/v3.16/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.16/community/x86_64/APKINDEX.tar.gz
(1/25) Installing binutils (2.38-r3)
(2/25) Installing libmagic (5.41-r0)
(3/25) Installing file (5.41-r0)
(4/25) Installing libgomp (11.2.1_git20220219-r2)
(5/25) Installing libatomic (11.2.1_git20220219-r2)
(6/25) Installing isl22 (0.22-r0)
(7/25) Installing mpfr4 (4.1.0-r0)
(8/25) Installing mpc1 (1.2.1-r0)
(9/25) Installing gcc (11.2.1_git20220219-r2)
(10/25) Installing musl-dev (1.2.3-r0)
(11/25) Installing libc-dev (0.7.2-r3)
(12/25) Installing g++ (11.2.1_git20220219-r2)
(13/25) Installing make (4.3-r0)
(14/25) Installing fortify-headers (1.1-r1)
(15/25) Installing patch (2.7.6-r7)
(16/25) Installing build-base (0.5-r3)
(17/25) Installing libucontext (1.2-r0)
(18/25) Installing ruby-libs (3.1.2-r0)
(19/25) Installing ruby (3.1.2-r0)
(20/25) Installing libgpg-error (1.45-r0)
(21/25) Installing libgcrypt (1.10.1-r0)
(22/25) Installing xz-libs (5.2.5-r1)
(23/25) Installing libxml2 (2.9.14-r1)
(24/25) Installing libxslt (1.1.35-r0)
(25/25) Installing ruby-nokogiri (1.13.8-r0)
Executing busybox-1.35.0-r17.trigger
OK: 219 MiB in 60 packages
Removing intermediate container 48218a584c4b
 ---> b2ff640c5c99
Step 4/5 : RUN gem install rspec capybara selenium-webdriver
 ---> Running in 860f50c7d1f5
Successfully installed rspec-support-3.11.1
Successfully installed diff-lcs-1.5.0
Successfully installed rspec-mocks-3.11.1
Successfully installed rspec-expectations-3.11.1
Successfully installed rspec-core-3.11.0
Successfully installed rspec-3.11.0
Successfully installed nokogiri-1.13.8-x86_64-linux
Successfully installed xpath-3.2.0
Successfully installed regexp_parser-2.5.0
Successfully installed rack-3.0.0
Successfully installed rack-test-2.0.2
Successfully installed mini_mime-1.1.2
Successfully installed public_suffix-5.0.0
Successfully installed addressable-2.8.1
Successfully installed capybara-3.37.1
Successfully installed websocket-1.2.9
RubyZip 3.0 is coming!
**********************

The public API of some Rubyzip classes has been modernized to use named
parameters for optional arguments. Please check your usage of the
following classes:
  * `Zip::File`
  * `Zip::Entry`
  * `Zip::InputStream`
  * `Zip::OutputStream`

Please ensure that your Gemfiles and .gemspecs are suitably restrictive
to avoid an unexpected breakage when 3.0 is released (e.g. ~> 2.3.0).
See https://github.com/rubyzip/rubyzip for details. The Changelog also
lists other enhancements and bugfixes that have been implemented since
version 2.3.0.
Successfully installed rubyzip-2.3.2
Successfully installed childprocess-4.1.0
Successfully installed selenium-webdriver-4.4.0
19 gems installed
Removing intermediate container 860f50c7d1f5
 ---> 6cc5f223c8c3
Step 5/5 : ENTRYPOINT [ "rspec" ]
 ---> Running in 8cb05680b7ff
Removing intermediate container 8cb05680b7ff
 ---> e364c43a4bd8

Successfully built e364c43a4bd8
Successfully tagged work_unit-tests:latest
WARNING: Image for service unit-tests was built because it did not already exist. To rebuild this image you must use `docker-compose build` or `docker-compose up --build`.
Creating work_unit-tests_run ... done
.

Finished in 0.00314 seconds (files took 1.13 seconds to load)
1 example, 0 failures

```

Notice the last line `1 example, 0failures`.

