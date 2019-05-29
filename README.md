# Getting started with Jenkins React & Node App

This repository is for helping you get started quickly with [Building Jenkins for React & Node JS](https://jenkins.io/doc/tutorials/build-a-node-js-and-react-app-with-npm/) tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/). Materials from that instructions are already provided in this repository.

The repository contains a simple Node.js and React application which generates a web page with the content "Welcome to React" and is accompanied by a test to check that the application renders satisfactorily.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline) you'll be creating yourself during the tutorial and the `scripts` subdirectory contains shell scripts with commands that are executed when Jenkins processes the "Test" and "Deliver" stages of your Pipeline.

## Get Started

Run the jenkinsci/blueocean image as a container in Docker using the following docker run command (bearing in mind that this command automatically downloads the image if this hasn’t been done):
```
docker run -d \
  --rm \
  -u root \
  -p 8080:8080 \
  -v jenkins-data:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v "$HOME":/home \
  --name simple-jenkins-react-app \
  jenkinsci/blueocean
```
or if you have docker compose, then you can run: 
```
docker-compose -f docker-compose-setup.yml up -d
```
When that's done, then you can just go and follow the tutorial [Building Jenkins for React & Node JS](https://jenkins.io/doc/tutorials/build-a-node-js-and-react-app-with-npm/).

## Thank You

Get love and give love! Clone the project and happy coding!
