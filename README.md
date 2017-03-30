# microservice-gateway

## Context
Imagine you're developing a Software that makes use of the Microservice architecture pattern. You might end up having several front end microservices with their respective addresses. This is is bad from a UX perspective. How can you hide the microservice architecture for the user and provide a single point of entry to your services?


## Problem
How to combine multiple front-end web services on one web page.


## Project
This Project provides a solution to the to the problem of combining front end microservices. 

![solution](https://cloud.githubusercontent.com/assets/15627894/24502586/ba45dc18-154e-11e7-8afb-eb18158ae55f.png)

*A user accessing multiple front end microservices via a single webpage*

The Project consists of four microservices, a `App` and a three `Compoments`. 

The `Components` are included in the `App` using three different approaches
* Server Side Includes
* HTML Imports from Web Components
* HTML Imports with [Polymer](https://www.polymer-project.org/)


## Used Technologies
The Project makes use of the these technologies:
* nginx
* Kubernetes
* Docker
* YAML
* HTML
* Bootstrap
* JavaScript, JQuery
* Server Side Includes
* PHP

## How to Start up the Services locally

Build the Docker Files:

`docker build -t app:latest ./app/`

`docker build -t ssi:latest ./components/ssi/`

`docker build -t polymer:latest ./components/polymer/`

`docker build -t htmlimport:latest ./components/html-import/`

Run the Docker Files:

`docker run -d --name ssi ssi:latest`

`docker run -d --name polymer polymer:latest`

`docker run -d --name htmlimport htmlimport:latest`

`docker run -d --name app --link ssi:ssi --link htmlimport:htmlimport --link polymer:polymer -p 8080:80 app:latest`

Open in Chrome: [localhost:8080](http://localhost:8080)

Every Component has a little form which performs a post to the microservice in the back and displays the result.

## How to Start up the Services on Kubernetes

The Project also includes YAML-Files to run everything on a Kubernetes Cluster.

## Credits
The Project was created in September 2016 as part of [eGym's 10 % Week](https://github.com/egymgmbh).