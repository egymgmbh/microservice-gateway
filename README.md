# microservice-gateway

## Context
Imagine you're developing a Software that makes use of the Microservice architecture pattern. You might end up having several front end microservices with their respective addresses. This is is bad from a UX perspective. How can you hide the microservice architecture for the user and provide a single point of entry to your services?


## Problem
How to combine multiple front-end web services on one web page.


## Solution
This Project provides a solution to the to the problem of combining front end microservices. 

![solution](https://cloud.githubusercontent.com/assets/15627894/24502586/ba45dc18-154e-11e7-8afb-eb18158ae55f.png)

*A user accessing multiple front end microservices via a single webpage*

The Project consists of three nginx Server, a `App` and a three `Compoments`. 

The `Component` are included in the `App` using three different approaches
* Server Side Includes
* HTML Imports from Web Components
* HTML Imports with [Polymer](https://www.polymer-project.org/)

The Project also includes YAML-Files to run everything on a Kubernetes Cluster.


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


## Credits
The Project was created in September 2016 as part of [eGym's 10 % Week](https://github.com/egymgmbh).