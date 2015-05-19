# gitless-nodejs-bower-grunt-runtime
A Dockerfile for an automated build that includes bower and grunt without using git://

Basically exactly the same image as [digitallyseamless/nodejs-bower-grunt](https://registry.hub.docker.com/u/digitallyseamless/nodejs-bower-grunt-runtime/), but with the addition of `ONBUILD RUN git config --global url.https://.insteadOf git://` which means that it will allow the bower (and any other step that requires accessing git) to work with https:// rather than git://. This is useful if, for reasons that no-one seems willing to explain, access to git is blocked by your network connection.

For all other information, please check [digitallyseamless/nodejs-bower-grunt](https://registry.hub.docker.com/u/digitallyseamless/nodejs-bower-grunt-runtime/)
