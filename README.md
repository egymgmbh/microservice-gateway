# microservice-gateway

## Context
Imagine you're developing a Software that makes use of the Microservice architecture pattern. You might end up having several front end microservices. You might also want to provide a single point of entry for your user, to hide the microservice architecture for the user and avoid having the user to deal with several addresses.

## Problem
How to combine multiple front-end web services on one web page.

## Solution
This Project shows three possible solutions to the problem of combining front end microservices. 

The Project consists of three nginx Server, a `App` and a three `Compoments`. 

The `Component` are included in the `App` using three different approaches
* Server Side Includes
* HTML Imports from Web Components
* HTML Imports with [Polymer](https://www.polymer-project.org/)

The Project also includes YAML-Files to run everything on a Kubernetes Cluster.

The Project was created in September 2016 as part of the eGym 10 % Week.

The Presentation can be found here: https://docs.google.com/presentation/d/1_mTztIQ7WKVt4SlIcKsTWOAIIoL5cMMg308dBDrxvqY/edit#slide=id.p

