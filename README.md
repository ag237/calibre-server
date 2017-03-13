Docker build with Ubuntu 16.04 and Calibre.

The container exposes the volume /calibre-lib, port 8080 and allows you to set a prefix (for setting up calibre-server behind a proxy)

-v /path/to/calibre/library:/calibre-lib
-e USER=calibre
-e PASS=calibrepass
-e PREFIX=/calibre

Example:

docker run -d -p 8082:8080 -v /Calibre:/calibre-lib -e USER=calibre -e PASS=calibrepassword -e PREFIX=/calibre --name calibre-server agentgreen/calibre-server



---------------
Release: 2.81 [10 Mar, 2017]
