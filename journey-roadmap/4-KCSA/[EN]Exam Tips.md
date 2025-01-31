# [KCSA] Kubernetes and Cloud Native Security Associate

## All exam tips
> [!TIP] 
> Whenever you book your exam, you can already start it 30 minutes before the time you settled.

> USE THIS FEATURE, it can help you a lot in case something goes wrong during the exam preparation, as I said on my Medium post.

## Exam introduction

KCSA is a tricky introduction to Cloud Native Security ecosystem. When I say tricky, I say it in a good way. KCSA may seen easy to ace, but it has some really good questions to make you think, so come prepared, it won't be free. KCSA will take you from and Cloud Native Seucrity Overview, going through Cluster Component Security, Threat Modelling, Platform Security and Securtity & Compliance Frameworks. You will get to know a lot of tools to aid you on your security journey.

You can find the [Exam Topics here](https://training.linuxfoundation.org/certification/kubernetes-and-cloud-native-security-associate-kcsa/).

## What course to take?
For KCSA, I strongly recommend [Mumshad Mannambeth's](https://www.linkedin.com/in/mmumshad/) course [Kubernetes and Cloud Native Security Associate (KCSA)](https://learn.kodekloud.com/user/courses/kubernetes-and-cloud-native-security-associate-kcsa) course on [KodeKloud](https://learn.kodekloud.com/).

Mumshad Mannambeth and the KodeKloud Team are specialized on Kubernetes content, and go through all topics with lots of details.

Also, there are very well prepared HandsOn Labs after every topic.

In the end, you will also find some Practice Exams.

> [!IMPORTANT] 
> One AMAZING resource to help you on KCSA is [Thiago's](https://www.linkedin.com/in/thiago4go/) [Kubernetes Security KCSA Mock Exam](https://kubernetes-security-kcsa-mock.vercel.app/). It has questions that are pretty alligned with the real exam. Make sure you get a good grade on this Mock Exam and you will surely get a good grade on the real KCSA Exam. You can also take a look at the [Project's GitHub Repo](https://github.com/thiago4go/kubernetes-security-kcsa-mock).

## KCNA tips
As you already know, KCSA is a 60 questions multiple choice exam.

>Exam timebox: 120 minutes ⏳

>Score Needed: 75 🎯

>My Score: 87 ✅

Going through the exam topics, here are some tips from my own exam, based on the topics below. 

>Keep in mind that all these tips are very well detailed on [[KCSA] Personal Notes:Anotações](./[KCSA]%20Personal%20notes:Anotações.pdf).

Overview of Cloud Native Security - 14%
* Remember about the 4Cs, shared responsibilities between Cloud Provider and Infra security and isolation techniques;
* Artifact Repository and Image Security are also a thing;
* Application Code Security will also be asked.

Kubernetes Cluster Component Security - 22%
* Here you will be asked to provide ways to configure all Kubernetes compenentes securely, so understand how to keep them safe;
* You will be asked from Components itself to Kubernetes objects like Pods, Volumes and etc.

Kubernetes Security Fundamentals - 22%
* Here you will get to know Pod Security Standards and Admissions;
* AuthN and AuthZ between components will also be asked;
* How to isolate workloads in soft and hard ways will also be requested;
* Audit logging configuration will be asked, so remember the steps to enable it;
* And, of course, NetworkPolicies.

Kubernetes Threat Model - 16%
* Threat Modelling is a wide area, but you will be asked about Boundaries, how data flows on your ecosystem and in how many ways an attacker can explore your environment;
* Understand how malicious code or access can affect your environment;
* Also, keep sensitive data safe and avoiding privilege escalation is important noting here.

Platform Security - 16%
* Pay attention to Supply Chain Security and securing Arfifact Repos;
* Public Key Infrastrucutre is an important point to be aware here;
* Admission controllers are often explored, so get to know the most used ones.

Compliance and Security Frameworks - 10%
* Here you will be asked about Compliace Frameworks focus and objectives;
* Tools for automating these processes will be asked, so make sure to understand them (they are a lot) and when to use each one.