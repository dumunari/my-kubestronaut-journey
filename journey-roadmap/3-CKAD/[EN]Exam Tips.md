# [CKAD] Certified Kubernetes Application Developer

## All exam tips
> [!TIP] 
> Whenever you book your exam, you can already start it 30 minutes before the time you settled.

> USE THIS FEATURE, it can help you a lot in case something goes wrong during the exam preparation, as I said on my Medium post.

## CKA, CKAD and CKS tips
> Whenever you book your exam, you get an exam simulator from [Killer.sh](https://killer.sh/). 

>This  exam simulator is pretty similar, and sometimes even harder than the original exam, do it as many times as you can. It gets available for 36 hours after you first start it.

> During the real exam, If you are not sure about a question, flag it for later and go on, time is crucial for these exams.

## Exam introduction

CKAD is one of the 3 HandsOn exams. Here you will be asked to perform tasks from an Application Developer view, goingr through App Design & Build, App Deployment, Observability & Maintenance, Services & Networking and Configuring Env Vars, Secrets, ConfigMaps and Volume Mountings. Also all sorts of Troubleshooting will be asked, always from an Developers view.

You can find the [Exam Topics here](https://training.linuxfoundation.org/certification/certified-kubernetes-application-developer-ckad/).

## What course to take?
For CKAD, I strongly recommend [Mumshad Mannambeth's](https://www.linkedin.com/in/mmumshad/) course  [Certified Kubernetes Application Developer (CKAD)](https://learn.kodekloud.com/user/courses/certified-kubernetes-application-developer-ckad) course on [KodeKloud](https://learn.kodekloud.com/).

The same course [is also available at Udemy](https://www.udemy.com/course/certified-kubernetes-application-developer).

Mumshad Mannambeth and the KodeKloud Team are specialized on Kubernetes content, and go through all topics with lots of details.

Also, there are very well prepared HandsOn Labs after every topic.

In the end, you will also find some Practice Exams.

## CKAD tips
As you already know, CKAD is a HandsOn exam, composed by around 16 challenges.

>Exam timebox: 120 minutes ⏳

>Score Needed: 66 🎯

>My Score: 98 ✅

Going through the exam topics, here are some tips from my own exam, based on the topics below. 

>Keep in mind that all these tips are very well detailed on [[CKAD] Personal Notes:Anotações](./[CKAD]%20Personal%20notes:Anotações.pdf).

Application Design and Build - 20%
* Here you will be asked to create Deployments, DaemonSets and Cronjobs. Cronjobs are tricky, so try to be fast when working with them. Also, make sure you know how to run a job from a cronjob;
* Multi-container pods will be asked, make sure you know how they work together, from initContainers to multiple containers purely.
* Volumes will also appear here, but more in a Developer way, so configurations and troubleshooting may not appear here, but keep them sharp.

Application Deployment - 20%
* This section will ask you to implement some different deployment strategies using raw Kubernetes components. Learn how to implement "bodge Canary" and dealing with Deployment Rollout Strategies.
* Also, you will be asked to perform some Helm taks. Make sure you understand when to use values.yaml and Chart.yaml. One thing to be aware here is how to manage helm cli, you will be asked to identify failed release installations and also to override values from specific Charts. Don't forget to learn the basics about downloading charts and adding new repos.

Application Observability and Maintenance - 15%
* Here you will be asked to do some sorts of Observability/Troubleshooting tasks;
* All sorts of probes will be asked here, so make sure you understand how they work and how to configure them properly. Also, probes can be used to lots of things, keep your mind open;
* Understand how to generate useful logs and analyze them;

Application Environment, Configuration and Security - 25%
* Here you will be asked to create and apply some CRDs;
* Requests, limits and quotas will also appear here, make sure you understand how they can impact your applications, like Quality of Service ratings;
* ConfigMaps and Secrets will also appear, so make sure you understand how to mount them in their differentes ways;
* ServiceAccounts will also come out here, make sure you understand how to add them to your applications and how to avoid automounting at application and at ServiceAccount level;
* SecurityContext is going to be frequently asked on this section, so make sure you understand all the different possibilities and which ones are applied at pod or container level.

Services and Networking - 20%
* You will be asked to troubleshoot, create and modify all sorts of services, so remember to keep them sharp on your kubectl skills, it will save you a lot of time;
* Ingresses will be asked here, but mostly on a rules configuration way, so remember to leverage kubectl to create your Ingresses, when requested. There is detailed Ingress tips on the Personal Notes, but I'd like to point here my favorite one: using kubectl create ingress --help and copying the "annotated" ingress example. It will save you A LOT of time.
* I don't know how often it happens, but I'm pretty sure I lost my 2 points on CKAD to a Ingress challenge that was using Traefik instead of Nginx, so I suggest you to prepare for Traefik challenges. I wasn't prepared, lost 2 points.
* NetworkPolicies are always tricky, and they will also haunt you here. Take a good time to study and understand how they work, how to allow, how to block and everything your apps need to function properly. Make sure you read these questions carefully, and know how to get to the Documentation NetworkPolicy examples fast.

## Extra tips

> Remember this exam asks you to look at all these topics as an Application Developer view.

> I'm my own CKAD exam, jsonpath wasnt as required as on CKA, but keep it in mind that jsonpath will be a handful for you here, as you will be asked to add your findings to a file.