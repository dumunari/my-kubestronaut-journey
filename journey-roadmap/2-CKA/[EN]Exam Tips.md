# [CKA] Certified Kubernetes Administrator

## All exam tips
> [!TIP] 
> Whenever you book your exam, you can already start it 30 minutes before the time you settled.

> USE THIS FEATURE, it can help you a lot in case something goes wrong during the exam preparation, as I said on my Medium post.

## CKA, CKAD and CKS tips
> Whenever you book your exam, you get an exam simulator from [Killer.sh](https://killer.sh/). 

>This  exam simulator is pretty similar, and sometimes even harder than the original exam, do it as many times as you can. It gets available for 36 hours after you first start it.

> During the real exam, If you are not sure about a question, flag it for later and go on, time is crucial for these exams.

## Exam introduction

CKA is one of the 3 HandsOn exams. Here you will be asked to perform some Cluster Administrator tasks about Storage, Scheduling, Cluster upgrades, Services, Networking, Backups and all sorts of Troubleshootings.

You can find the [Exam Topics here](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/).

## What course to take?
For CKA, I strongly recommend [Mumshad Mannambeth's](https://www.linkedin.com/in/mmumshad/) course  [CKA Certification Course - Certified Kubernetes Administrator](https://learn.kodekloud.com/user/courses/cka-certification-course-certified-kubernetes-administrator) course on [KodeKloud](https://learn.kodekloud.com/).

The same course [is also available at Udemy](https://www.udemy.com/course/certified-kubernetes-administrator-with-practice-tests).

Mumshad Mannambeth and the KodeKloud Team are specialized on Kubernetes content, and go through all topics with lots of details.

Also, there are very well prepared HandsOn Labs after every topic.

In the end, you will also find some Practice Exams.

## CKA tips
As you already know, CKA is a HandsOn exam, composed by around 16 challenges.

>Exam timebox: 120 minutes ⏳

>Score Needed: 66 🎯

>My Score: 99 ✅

Going through the exam topics, here are some tips from my own exam, based on the topics below. 

>Keep in mind that all these tips are very well detailed on [[CKA] Personal Notes:Anotações](./[CKA]%20Personal%20notes:Anotações.pdf)

Storage - 10%
* Here you will be asked to add all kinds of Volumes to your apps, as long as creating PVs, PVCs and Storage Classes;
* Pay attention to mountPath, Volume types, Access Modes and different kinds of Secrets and ConfigMaps mounting;
* Make sure you know how to get to the Documentation about PVs and PVCs and find the examples fast.

Troubleshooting - 30%
* Here you will be asked to understand why applications are not working or malfunctioning;
* Pay attention to logs and events;
* We are talking about all kinds of troubleshootings here, like apps, nodes, cluster components, volumes, etcd and certificates.

Workloads & Scheduling - 15%
* Understand how to scale, rollout and deal with Deployments and ReplicaSets. Remember that kubectl commands are way faster and can help you gaining some time here. Master kubectl scale, kubectl set image and kubectl rollout commands;
* You will be also asked to mount Secrets and Volumes to the pods, as long as creating these objects. Use kubectl to create them fast, and make sure you can find the examples on how to mount them using the different ways on Documentation;
* Remember the purpose of using Taints, Tolerations and NodeSelectors, and how to make them work together.

Cluster Architecture, Installation & Configuration - 25%
* On this section you will be asked to fully Upgrade a cluster masters and worker nodes, and also to troubleshoot and fix ongoing failed upgrades. Master the upgrade commands, their alternative paths and always remember to check apt source list for Kubernetes 🙂
* You will also be asked to backup and restore etcd. Master the etcdctl commands to make these questions faster. Also, pay attention to the folders and volumes when restoring etcd;
* And last, but not least, you will be asked to create and handle Roles, Rolebindings, ClusterRoles, ClusterRoleBindings and ServiceAccounts. Make sure you can handle them easily via kubectl, and give an special attention to binding ServiceAccounts to Roles or ClusterRoles, and remember you can bind a ClusterRole to a Rolebinding.

Services & Networking - 20%
* This is probably the trickiest part of the exam;
* Here you will be asked to create some sort of services to expose your applications. Master the kubectl expose command, as it will save you a lot of time;
* One importat part here is creating Ingresses. Ingresses may seem hard to deal with, but they are pretty straightforward and you can leverage kubectl to create your Ingress, when requested. There is detailed Ingress tips on the Personal Notes, but I'd like to point here my favorite one: using kubectl create ingress --help and copying the "annotated" ingress example. It will save you A LOT of time.
* Now, the trickiest component of this exam, NetworkPolicies. Take a good time to study and understand NetworkPolicies. How they work, how to allow, how to block and everything your apps need to function properly. I'm pretty sure the 1 point I lost at CKA was at NetworkPolicies, probably on allowing DNS connections. Make sure you read these questions carefully, and know how to get to the Documentation NetworkPolicy examples fast;
* You also may be asked to install or configure a CNI plugin, so keep this knowledge sharp.

## Extra tips

> Remember this exam asks you to look at all these topics as an Administrators view.

> Also, keep in mind that jsonpath will be a handful for you here, as you will be asked to add your findings to a file most of the time.