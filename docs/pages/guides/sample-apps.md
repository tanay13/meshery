---
layout: default
title: Deploying Sample Applications
description: This guide is to help users get a better understanding of sample apps
permalink: guides/sample-apps
type: Guides
---

## Sample Applications

Sample Applications are used to interact and exemplify the features of your service mesh. They are often a collection of microservices which you can be used by the user as a sandbox playground to experiment and learn about the service mesh and it's exhaustive set of features.
Before deploying a sample app on top of your service mesh, the application needs to be exposed and allowed external access to the available services in a cluster. There are a myriad of ways to do this, specific to the service mesh you are using. 

A popular way of exposing your cluster is by using [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/), an API object that defines rules which allow external access to services in a cluster. 

- [Set up Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/#the-ingress-resource)
- [Set up Ingress on Minikube](https://kubernetes.io/docs/tasks/access-application-cluster/ingress-minikube/)

To deploy a sample app on Meshery:

1. Go to the management page of any [service mesh](/docs/service-meshes) and install any of its stable versions
<img alt="Consul-install" style="width:500px;height:auto;" src="/docs/assets/img/adapters/consul/consul-install.png" />
2. Click (+) on `Manage Sample Application Lifecycle`. You will now be able to see a drop down menu with the available sample applications
<img alt="ImageHub sample app" style="width:500px;height:auto;" src="/docs/assets/img/adapters/consul/consul-sample-app.png" />
3. Click on the sample application you want to deploy. This might take up to a minute. You will be notified when the sample application has been deployed
<img alt="ImageHub deployed" style="width:500px;height:auto;" src="/docs/assets/img/adapters/consul/consul-imagehub-success.png" />

#### [BookInfo](https://github.com/layer5io/istio-service-mesh-workshop/blob/master/lab-2/README.md#what-is-the-bookinfo-application)

Originally built by Istio, BookInfo is a sample application which on deployment displays information about a book, similar to a single catalog entry of an online book store. Displayed on the page is a description of the book, book details (ISBN, number of pages, and so on), and a few book reviews. The application comprises of four microservices:

   - `productpage`: The productpage microservice calls the details and reviews microservices to populate the page.
   - `details`: The details microservice contains book information.
   - `reviews`: The reviews microservice contains book reviews. It also calls the ratings microservice.
   - `ratings`: The ratings microservice contains book ranking information that accompanies a book review.

Once BookInfo is deployed, you can use Meshery to apply custom configurations to control traffic, inject latency, perform context-based routing, and so on. 

<img alt="BookInfo sample app" style="width:500px;height:auto;" src="/docs/assets/img/adapters/sample-apps/bookinfo.png" />

#### [Emojivoto](https://github.com/BuoyantIO/emojivoto)

Emojivoto is a microservice application, originally built by Linkerd that allows users to vote for their favorite emoji, and tracks votes received on a leaderboard. The application is composed of three microservices:

   - `emojivoto-web`: Web frontend and REST API
   - `emojivoto-emoji-svc`: gRPC API for finding and listing emoji
   - `emojivoto-voting-svc`: gRPC API for voting and leaderboard

<img alt="Emojivoto" style="width:500px;height:auto;" src="/docs/assets/img/adapters/sample-apps/emojivoto.png" />

#### [ImageHub](https://layer5.io/projects/image-hub)

Image Hub is a sample application for exploring WebAssembly modules used as Envoy filters. The application was originally written to run on Consul. However, it doesn't have any dependency on Consul and can be deployed on any service mesh. These modules can be used to implement multi-tenancy or to implement per user rate limiting in your application’s endpoints, without messing with your application infrastructure. 
Follow this tutorial to set up [ImageHub with Ingress](https://github.com/layer5io/image-hub#use-image-hub)

<img alt="Imagehub-on-Consul" style="width:500px;height:auto;" src="/docs/assets/img/adapters/sample-apps/imagehub-on-consul.png" />

#### [HTTPBin](https://httpbin.org)

HttpBin is a simple HTTP request and response service that responds to many kinds of http/https requests including the standaard http request methods (or verbs) used by REST.

<img alt="httpbin" style="width:500px;height:auto;" src="/docs/assets/img/adapters/sample-apps/httpbin.png" />

#### [Linkerd Books](https://github.com/BuoyantIO/booksapp)

Linkerd Books is a sample Ruby based application. It is designed to demonstrate the various value propositions, including debugging, observability, and monitoring of your service mesh. It can be used to scope out your mesh's efficiency and for debugging.

<img alt="Linkerd Books" style="width:500px;height:auto;" src="/docs/assets/img/adapters/sample-apps/linkerd-books.png" />

#### [Hipster](https://github.com/GoogleCloudPlatform/microservices-demo)

Hipster is a sample cloud-native application, originally built by Google. It comprises of 10 microservices and can be used to showcase and work with Kubernetes, Istio, gRPC and OpenCensus. On deployment, it runs a web-based e-commerce demo application, an example of which can be seen below:

<img alt="Hipster" style="width:500px;height:auto;" src="/docs/assets/img/adapters/sample-apps/hipster-shop.png" />

<!--Sample apps specific to NSM can be found on /docs/service-meshesadapters/nsm/nsm-->