[[Docker]] images are the blueprint that are used to create the containers that your apps will live in.

Created from a `Dockerfile` which will specify the base image your image will be built off of. Many of you will probably most likely be using an [Alpine](https://github.com/mhart/alpine-node) version of Node which the barebones image of what exactly is needed to run a node instance (before installation of your node dependencies).

Within this dockerfile you will be creating the directory that houses your code, installing your dependencies from NPM, exposing the ports that will be needed to run your web application and the commands needed to kick off the application itself (`npm start`)

After the `Dockerfile` is complete, you will need docker to build your image proper. This will be some sort of `docker build` command.

It's always a good idea to try and run the docker image locally before sending it up to cloud. Once you're able to have it run locally, you have pretty good assurance that it will run anywhere.