Docker build with Ubuntu 16.04 and Calibre.

The container exposes the volume /calibre-lib, port 8080 and allows you to set a prefix (for setting up calibre-server behind a proxy)

-v /path/to/calibre/library:/calibre-lib
-e PREFIX=/calibre

Example:

docker run -d -p 8082:8080 -v /Calibre:/calibre-lib -e PREFIX=/calibre --name calibre-server agentgreen/calibre-server



---------------
20170707 - As of Calibre-server 3.0 they drastically changed how authentication is done, and the old method of putting user/pass on command line is deprecated. I have removed auth for now until I can work out the proper method for adding it back in.
