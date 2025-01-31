# [CKA] Certified Kubernetes Administrator

## Dica para todos exames
> [!TIP] 
> Sempre que você agendar seu exame, poderá começar a fazê-lo 30 minutos antes do horário marcado.

> USE ESSA POSSIBILIDADE, esse tempo adicional ajuda muito caso você encontre algum problema, como comentei no meu post do Medium.

## Dicas para CKA, CKAD e CKS
> Sempre que você agendar seu exame, você receberá um simulado da [Killer.sh](https://killer.sh/). 

> Este simulado é bem similar e, às vezes, até mais difícil do que o exame original, faça-o o máximo de vezes possível. Ele ficará disponível por 36 horas após o primeiro acesso.

> Durante o exame real, se você não tiver certeza sobre uma pergunta, marque-a para revisar depois e continue. O tempo é crucial nesses exames.

## Introdução

CKA é um dos 3 exames HandsOn. Neste exame, você será solicitado a realizar tarefas de Administração de Cluster, como Storage, Scheduling, Atualizações de Cluster, Services, Networking, Backups e diversos tipos de Troubleshooting.

Você pode encontrar os [Tópicos do Exame aqui](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/).


## Qual curso fazer?
Para a CKA, recomendo fortemente o curso [CKA Certification Course - Certified Kubernetes Administrator](https://learn.kodekloud.com/user/courses/cka-certification-course-certified-kubernetes-administrator) do [Mumshad Mannambeth](https://www.linkedin.com/in/mmumshad/) na [KodeKloud](https://learn.kodekloud.com/).

O mesmo curso [também está disponível na Udemy](https://www.udemy.com/course/certified-kubernetes-administrator-with-practice-tests).

Mumshad Mannambeth e a equipe da KodeKloud são especializados em conteúdo de Kubernetes e abordam todos os tópicos com muitos detalhes.

Além disso, há HandsOn Labs muito bem preparados após cada tópico.

No final, você também encontrará alguns Simulados.

## Dicas
Como você já sabe, o CKA é um exame HandsOn, composto por cerca de 16 desafios.

>Tempo de prova: 120 minutos ⏳

>Pontuação Necessária: 66 🎯

>Minha pontuação: 99 ✅

Passando pelos tópicos do exame, aqui estão algumas dicas baseadas na minha própria experiência, com base nos tópicos abaixo. 

>Todas essas dicas estão bem detalhadas no arquivo [[CKA] Personal Notes:Anotações](./[CKA]%20Personal%20notes:Anotações.pdf)

Storage - 10%
* Aqui você precisará adicionar todos os tipos de Volumes às suas aplicações, como criar PVs, PVCs e Storage Classes;
* Preste atenção ao mountPath, tipos de Volume, Access Modes e diferentes tipos de Secrets e ConfigMaps;
* Certifique-se de saber como acessar a Documentação sobre PVs e PVCs e encontrar exemplos rapidamente.

Troubleshooting - 30%
* Aqui você será solicitado a entender por que as aplicações não estão funcionando ou estão com problemas;
* Preste atenção nos logs e eventos;
* Estamos falando de todos os tipos de troubleshooting aqui, como apps, nós, componentes do cluster, volumes, etcd e certificados.

Workloads & Scheduling - 15%
* Entenda como escalar, fazer rollout e lidar com Deployments e ReplicaSets. Lembre-se de que os comandos kubectl são bem mais rápidos e podem te ajudar a ganhar tempo aqui. Domine os comandos kubectl scale, kubectl set image e kubectl rollout;
* Você também precisará montar Secrets e Volumes nos pods, assim como criar esses objetos. Use kubectl para criá-los rapidamente e certifique-se de conseguir encontrar os exemplos de como montá-los usando as diferentes formas na Documentação;
* Lembre-se da finalidade de usar Taints, Tolerations e NodeSelectors e como fazer esses elementos funcionarem juntos.

Cluster Architecture, Installation & Configuration - 25%
* Nesta seção, você precisará atualizar completamente os masters e worker nodes do cluster, além de solucionar e corrigir atualizações que falharam. Domine os comandos de atualização, seus caminhos alternativos e sempre lembre-se de verificar a lista de fontes do apt para Kubernetes 🙂;
* Você também será solicitado a fazer backup e restaurar o etcd. Domine os comandos etcdctl para tornar essas questões mais rápidas. Além disso, preste atenção nas pastas e volumes ao restaurar o etcd;
* E, por último, mas não menos importante, você precisará criar e gerenciar Roles, RoleBindings, ClusterRoles, ClusterRoleBindings e ServiceAccounts. Certifique-se de conseguir manipulá-los facilmente via kubectl e dê atenção especial ao cenário de vincular ServiceAccounts a Roles ou ClusterRoles, lembrando que você pode vincular um ClusterRole a um RoleBinding.

Services & Networking - 20%
* Esta é provavelmente a parte mais difícil do exame;
* Aqui você vai precisar criar alguns tipos de Services para expor suas aplicações. Domine o comando kubectl expose, pois ele pode te economizar muito tempo;
* Uma parte importante aqui é a criação de Ingresses. Ingresses podem parecer difíceis de lidar, mas são bem simples e você pode aproveitar o kubectl para criar seu Ingress quando solicitado. Existem dicas detalhadas sobre Ingress no arquivo de Anotações, mas queria deixar aqui a minha favorita: use o comando kubectl create ingress --help e copie o exemplo de ingress "annotated". Isso vai te economizar MUITO tempo;
* Agora, o componente mais difícil desse exame, as NetworkPolicies. Dedique um bom tempo para estudar e entender NetworkPolicies. Como elas funcionam, como permitir, como bloquear e tudo o que suas aplicações precisam para funcionar corretamente. Tenho quase certeza de que o 1 ponto que perdi na CKA foi por conta de NetworkPolicies, provavelmente ao permitir conexões DNS. Certifique-se de ler essas questões com cuidado e saber como acessar rapidamente o exemplo de NetworkPolicy na Documentação;
* Você também encontrar alguma questão sobre instalar ou configurar um plugin de CNI, então mantenha esse conhecimento na manga.

## Dicas extras

> Lembre-se de que este exame pede para você analisar todos esses tópicos sob a perspectiva de um Administrador.

> Além disso, tenha em mente que o jsonpath será muito útil pra você aqui, pois na maioria das vezes será pedido para que você salve suas análises em arquivos.