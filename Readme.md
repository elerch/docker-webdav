# Docker:webdav-alpine

This [Dockerfile](Dockerfile) compiles to an image that

* is based on a [alpine:3.6](https://hub.docker.com/_/alpine/)
* has the latest [Apache webserver](http://httpd.apache.org/) installed
* has the [Apache WebDAV modules](https://httpd.apache.org/docs/2.2/mod/mod_dav.html) enabled

It is available through the Docker Hub at [elerch/webdav-alpine](https://hub.docker.com/r/elerch/webdav-alpine/).

## Running

To run the images you still need to provide a username, password and
host name.

Thus, a commandline may look like this:

    docker run -d                           \
        -e USERNAME=user                    \
        -e PASSWORD=pass                    \
        -e VIRTUAL_HOST=myhost.example.com  \
        -v /path/to/dav-files:/dav          \
        -p 8888:80

