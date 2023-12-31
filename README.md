Original tutorial here: https://www.youtube.com/watch?v=X48VuDVv0do

![Alt text](/images/image.png)

Now, with Services:
![Alt text](/images/image-1.png)

Now, with Ingress, request first goes to Ingress then Service:
![Alt text](/images/image-2.png)

ConfigMap and Secret:
![Alt text](/images/image-3.png)

But, for credentials put it in a Secret and not a ConfigMap. You can use data from ConfigMap/Secret inside of your app pod using environment variables or as a properties file:
![Alt text](/images/image-4.png)

Summary of components so far:
![Alt text](/images/image-5.png)

Next, is Data storage using Volumes. K8s doesn't manage data persistance. Think of data storage as a separate "hard drive"
![Alt text](/images/image-6.png)

Next, let's talk about Deployment and Stateful Set. Deployment is the blueprint for my-app pods. But, in practice you will not be working with pods, you will create Deployments.
Pods are a layer of abstraction on top of containers. Deployments are an abstraction on top of pods. 
![Alt text](/images/image-7.png)

We ccan't replicated DB via Deployments because it has a state, which is it's data. They would need to access the same data storage and you would need 
some sort mechanism to figure out which pods are reading/writing to the storage. This is where StatefulSet comes in.
![Alt text](/images/image-8.png)

![Alt text](/images/image-9.png)

Summary so far:
![Alt text](/images/image-10.png)

Now, let's talk about K8s architecture:
![Alt text](/images/image-11.png)

![Alt text](/images/image-12.png)

![Alt text](/images/image-13.png)

![Alt text](/images/image-14.png)

One entry point into the cluster:
![Alt text](/images/image-15.png)

![Alt text](/images/image-17.png)

![Alt text](/images/image-18.png)

![Alt text](/images/image-19.png)

![Alt text](/images/image-20.png)

In practice, K8's is usually made up of multiple master nodes.
![Alt text](/images/image-21.png)

![Alt text](/images/image-22.png)

![Alt text](/images/image-23.png)

![Alt text](/images/image-24.png)

You in practice will never have to manage/delete/create ReplicateSets
![Alt text](/images/image-25.png)

Everything below Deployment is managed by K8s
![Alt text](/images/image-26.png)


![Alt text](/images/image-27.png)

![Alt text](/images/image-28.png)

![Alt text](/images/image-29.png)

![Alt text](/images/image-30.png)

![Alt text](/images/image-31.png)









