# [KCNA] Kubernetes and Cloud Native Associate

## All exam tips
> [!NOTE] 
> Whenever you book your exam, you can already start it 30 minutes before the time you settled.

> USE THIS FEATURE, it can help you a lot in case something goes wrong during the exam preparation, as I said on my Medium post.

## Exam introduction

KCNA is a very nice introduction to Cloud Native and Kubernetes ecosystem. It takes you from Cloud Native, Linux Foundation and CNCF foundations to a solid basic vision of how Kubernetes works alongside other tools for Observability, Storage, Service Mesh, DevOps and GitOps practices.

You can find the [Exam Topics here](https://training.linuxfoundation.org/certification/kubernetes-cloud-native-associate/).

## What course to take?
For KCNA, I strongly recommend [James Spurin's](https://medium.com/r/?url=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fjamesspurin%2F)  [Kubernetes Certified (KCNA) + Hands On Labs + Practice Exams](https://www.udemy.com/course/dive-into-cloud-native-containers-kubernetes-and-the-kcna/?srsltid=AfmBOooZb6PVZkBkO1fxFovRyuZQ3BZl8CuE6DOzCvkUy062yXyPlYfK&couponCode=KEEPLEARNINGBR) course on Udemy.

James goes through all required topics for KCNA exam with amazing detail.

Also, there are very well prepared HandsOn Labs that helps you applying the theory, while giving you lots of tools to use on the next exams. I truly believe my CKA and CKAD exams.

In the end, you will find some Practice Exams that are pretty aligned with the real exam.

## KCNA tips
As you already know, KCNA is a 60 questions multiple choice exam.

>Exam timebox: 120 minutes ⏳

>Score Needed: 75 🎯

>My Score: 93 ✅

Going through the exam topics, here are some tips from my own exam, based on the topics below. 

>Keep in mind that all these tips are very well detailed on [[KCNA] Personal Notes:Anotações]([KCNA]%20Personal%20notes:Anotações.pdf).

Kubernetes Fundamentals - 46%
* Kubelet functions are often explored, so keep in my its responsabilities;
* You will be asked about the different Container Runtimes (kata, gVisor). Remember their advantages, disadvantages and purposes;
* You will also be asked about Container Runtime levels and their responsabilities, make sure you understand about Low level and High level Container Runtimes purposes and responsabilities;
* Last but not least, get to know every Kubernetes Component responsability.

Container Orchestration - 22%
* Here you will also be asked about other Container Orchestration tools, not only Kubernetes. Of course you wont be asked about their inside outs cause its not part of the exam, but get to know the basics about other tools like Apache Mesos and OpenShift.

Cloud Native Architecture - 16%
* Here you will be asked the basics about Resilience, Agility, Operability and Observability;
* Get to know about Microservices vs Monoliths;
* Understand Application lifecycle alongside with automated pipeline practices and the purpose of each step/stage of CI/CD;
* Service Discovery basics, speed/efficiency vs cost and the key pillars of CN Architecture are also asked here.


Cloud Native Observability - 8%
* Understand the difference between Logs, Metrics and Tracing;
* Get to know the basics about Grafana and Prometheus;
* Here you will also be asked about Cost Management, so get to know about different types of Instance Offerings, Rightizing, Autoscaling and Anomaly detection.


Cloud Native Application Delivery - 8%
* Here you will get your first glimpse of GitOps;
* Get to know the GitOps concept;
* Understand the basics of ArgoCD and Flux, along with their differences and objectives.