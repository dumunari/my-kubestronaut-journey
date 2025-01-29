# [CKS] Certified Kubernetes Security Specialist

## All exam tips
> [!NOTE] 
> Whenever you book your exam, you can already start it 30 minutes before the time you settled.

> USE THIS FEATURE, it can help you a lot in case something goes wrong during the exam preparation, as I said on my Medium post.

## CKA, CKAD and CKS tips
> Whenever you book your exam, you get an exam simulator from [Killer.sh](https://killer.sh/). 

>This  exam simulator is pretty similar, and sometimes even harder than the original exam, do it as many times as you can. It gets available for 36 hours after you first start it.

> During the real exam, If you are not sure about a question, flag it for later and go on, time is crucial for these exams.

## Exam introduction

Here comes the pain 🙂
And no, (unfortunately) it's not a Slipknot song, it's CKS.

CKS is one of the 3 HandsOn exams, the thoughest one. Here you will be asked to perform security tasks that will challenge you to mix your Kubernetes, OS and Networking skills. Also, there are a lot of additional tools that you will be required to use, like Falco, kube-bench, Trivy and so on. From Cluster Hardening to Minimizing footprints, you will be challenged through really cool tasks that will make you think out of the box. 

You can find the [Exam Topics here](https://training.linuxfoundation.org/certification/certified-kubernetes-security-specialist/).

## What course to take?
For CKS, I strongly recommend [Mumshad Mannambeth's](https://www.linkedin.com/in/mmumshad/) course [Certified Kubernetes Security Specialist (CKS)](https://learn.kodekloud.com/user/courses/certified-kubernetes-security-specialist-cks) course on [KodeKloud](https://learn.kodekloud.com/).

Mumshad Mannambeth and the KodeKloud Team are specialized on Kubernetes content, and go through all topics with lots of details.

Also, there are very well prepared HandsOn Labs after every topic.

In the end, you will also find some Practice Exams.

You will also find some [CKS Challenges](https://learn.kodekloud.com/user/courses/cks-challenges) on [KodeKloud](https://learn.kodekloud.com/). I recommend going through them, if you are able to. 

Also, I recommend going through all [KillerCoda Interactive Scenarios for Kubernetes Security](https://killercoda.com/killer-shell-cks).

## CKS tips
As you already know, CKS is a HandsOn exam, composed by around 16 challenges.

>Exam timebox: 120 minutes ⏳

>Score Needed: 67 🎯

>My Score: 74 ✅

Going through the exam topics, here are some tips from my own exam, based on the topics below. 

>Keep in mind that all these tips are very well detailed on [[CKS] Personal Notes:Anotações](./[CKS]%20Personal%20notes:Anotações.pdf).

Cluster Setup - 15%
* Here you will be asked to apply some security configurations to cluster components. You will be provided a kube-bench report to guide you on this task, so read it carefully;
* NetworkPolicies are here again. You will be asked to use them to secure cluster access.
* Remember Ingresses? They are also back. Here you will be asked to create/change an Ingress with the additional TLS configuration. Make sure you are sharp creating TLS Secrets.
* One task that seems easy but is very tricky is verifying binaries. DO NOT trust your eyes. Generate the hash for each binary and add it to a file, them compare both files contents. I don't know if it's the best way to do it, but that's how it worked for me.

Cluster Hardening - 15%
* ServiceAccounts will be explored here, but most in a way for you to make sure they don't have extra permissions. Also, automounting may also appear here. Remember how to configure it at Pod and ServiceAccount levels.
* Configuring acces to Kubernetes API will also appear;
* Kubelet configuration changes are also very often asked. There's detailed information about this on the Personal Notes file, read it carefully;
* Kubernetes Cluster Upgrade may also appear. Remember the lessons from CKA to go smoothly through it;
* Not sure if this is the right section, but make sure you understand how to retrieve secrets directly from etcd via etcdctl, and how to enable secret encryption at rest, I'm 90% sure that you will face a task like this.

System Hardening - 10%
* Reducing attack surface will be asked here. It may be explored in lots of ways;
* NetworkPolicies will also appear here;
* Applying Seccomp and AppArmor profiles will also be asked. Make sure you understand how to enable profiles on AppArmor and how to properly set Seccomp profiles to be used.

Minimize Microservice Vulnerabilities - 20%
* Here you will be asked to apply Pod Security Standards;
* Isolation techniques like soft and hard multi-tenancy and more isolation techniques will appear here;
* Remember NetworkPolicies? They can get worse. Here you will need to implement some CiliumNetWorkPolicies. To be truly honest, they are not much differente from conventional ones, so just keep calm, it's mostly a syntax difference. But there are 2 very important points to understand that differ from conventional NetworkPolicies. Take a close look at [ICMP/ICMPv6](https://docs.cilium.io/en/stable/security/policy/language/#example-icmp-icmpv6) and how to [Enforce Mutual Authentication](https://docs.cilium.io/en/v1.16/network/servicemesh/mutual-authentication/mutual-authentication-example/#enforce-mutual-authentication). Cilium NetworkPolicy has a very good [Documentation](https://docs.cilium.io/en/v1.16/security/policy/#network-policy) full of examples.

Supply Chain Security - 20%
* Here you will be asked to perform some image hardening. Make sure to look for too broad components versions, root user and bad use of the COPY command;
* Also, you may be asked to generate some SBOM using toolks like sbom an Trivy. Both are pretty straightforward. Take a look at the help command and you will be safe;
* You may be asked to perform some image scan using Trivy, too.

Monitoring, Logging and Runtime Security - 20%
* Here you will be asked to use toolks like Falco. Make sure you understand how Falco works, how to tweak rules and check for results;
* Container immutability will be also asked, so make sure you know to ensure it;
* You will be asked to enable Audit logs, make sure you know how to enable and configure them. Please, pay attention to Volume Mounting;
* Not sure if it will be prompted on this section, but configuring ImagePolicyWebhook admission plugin will surely be asked. Just saying it again, please, pay attention to Volume Mounting and configuring its specific kubeconfig file.

## Extra tips

> In case you don't have any Linux Admin skills, I strongly recommend looking for a course before taking on CKS. You will be asked to perform lots of System Administrator tasks like identifying a process PID, finding binaries and checking packages versions.