# [CKAD] Certified Kubernetes Application Developer

## Dica para todos exames
> [!TIP] 
> Sempre que você agendar seu exame, poderá começar a fazê-lo 30 minutos antes do horário marcado.

> USE ESSA POSSIBILIDADE, esse tempo adicional ajuda muito caso você encontre algum problema, como comentei no meu post do Medium.

## Dicas para CKA, CKAD e CKS
> Sempre que você agendar seu exame, você receberá um simulado da [Killer.sh](https://killer.sh/). 

> Este simulado é bem similar e, às vezes, até mais difícil do que o exame original, faça-o o máximo de vezes possível. Ele ficará disponível por 36 horas após o primeiro acesso.

> Durante o exame real, se você não tiver certeza sobre uma pergunta, marque-a para revisar depois e continue. O tempo é crucial nesses exames.

## Introdução

CKAD é um dos 3 exames HandsOn. Neste exame, você será solicitado a realizar tarefas sob a perspectiva de um Desenvolvedor de Aplicações, passando por Design e Construção de Apps, Implantação de Apps, Observabilidade e Manutenção, Services, Networking, além de configuração de Variáveis de Ambiente, Secrets, ConfigMaps e Volumes. Além disso, terá troubleshooting, mas sob a ótica de um Desenvolvedor.

Você pode encontrar os [Tópicos do Exame aqui](https://training.linuxfoundation.org/certification/certified-kubernetes-application-developer-ckad/).


## Qual curso fazer?
Para a CKAD, recomendo fortemente o curso [Certified Kubernetes Application Developer (CKAD)](https://learn.kodekloud.com/user/courses/certified-kubernetes-application-developer-ckad) do [Mumshad Mannambeth](https://www.linkedin.com/in/mmumshad/) na [KodeKloud](https://learn.kodekloud.com/).

O mesmo curso [também está disponível na Udemy](https://www.udemy.com/course/certified-kubernetes-application-developer).

Mumshad Mannambeth e a equipe da KodeKloud são especializados em conteúdo de Kubernetes e abordam todos os tópicos com muitos detalhes.

Além disso, há HandsOn Labs muito bem preparados após cada tópico.

No final, você também encontrará alguns Simulados.

## Dicas
Como você já sabe, o CKAD é um exame HandsOn, composto por cerca de 16 desafios.

>Tempo de prova: 120 minutos ⏳

>Pontuação Necessária: 66 🎯

>Minha pontuação: 98 ✅

Passando pelos tópicos do exame, aqui estão algumas dicas baseadas na minha própria experiência, com base nos tópicos abaixo. 

>Todas essas dicas estão bem detalhadas no arquivo [[CKAD] Personal Notes:Anotações](./[CKAD]%20Personal%20notes:Anotações.pdf)

Application Design and Build - 20%
* Aqui, você precisará criar Deployments, DaemonSets e Cronjobs. Cronjobs são os mais complicados, então tente ser rápido ao trabalhar com eles. Além disso, certifique-se de saber como rodar um job a partir de um cronjob;
* Pods com múltiplos containers serão abordados, então, certifique-se de entender como eles funcionam juntos, desde initContainers até múltiplos containeres de fato;
* Volumes também aparecerão aqui, mas de uma forma mais voltada para o Desenvolvedor, então configurações e solução de problemas podem não ser abordadas aqui, mas mantenha esses conhecimentos afiados.

Application Deployment - 20%
* Esta seção vai pedir para você implementar algumas estratégias de deploy diferentes, usando componentes nativos do Kubernetes. Aprenda a implementar "Canary gambiarra" e a lidar com estratégias de Rollout de Deployments.
* Além disso, você precisará realizar algumas tarefas com Helm. Certifique-se de entender quando usar o values.yaml e o Chart.yaml. Uma coisa que ajuda muito é saber usar o Helm CLI, pois você precisará identificar instalações de releases com falha, também sobrescrever valores de Charts específicos já prontos. Não se esqueça de aprender o básico sobre como baixar charts e adicionar novos repositórios.

Application Observability and Maintenance - 15%
* Aqui, você precisará realizar alguns tipos de tarefas de Observabilidade/Troubleshooting;
* Todos os tipos de probes serão abordados aqui, então, certifique-se de entender como elas funcionam e como configurá-las corretamente. Além disso, as probes podem ser usadas para várias coisas, mantenha a mente aberta. No meu caso, um dos desafios foi utilizar uma probe para removers todos os terminais shell do containers;
* Entenda como gerar logs úteis e analisá-los.

Application Environment, Configuration and Security - 25%
* Requests, limits e quotas também aparecerão aqui, então certifique-se de entender como eles podem impactar suas aplicações, como as classificações de Quality of Service;
* ConfigMaps e Secrets também aparecerão, então certifique-se de entender como montá-los de diferentes formas;
* ServiceAccounts também serão abordados, então certifique-se de entender como adicioná-los às suas aplicações e como evitar o automounting tanto no nível da aplicação quanto no nível do ServiceAccount;
* SecurityContext será frequentemente abordado nesta seção, então certifique-se de entender todas as diferentes possibilidades e quais são aplicadas no nível do pod ou do container.

Services and Networking - 20%
* Você precisará solucionar problemas, criar e modificar todos os tipos de Services, então lembre-se de manter suas habilidades no kubectl afiadas, isso vai te economizar muito tempo;
* Ingresses serão abordados aqui, mas principalmente na parte de configuração de regras, então lembre-se de usar o kubectl para criar seus Ingresses, quando solicitado. Há dicas detalhadas sobre Ingress nos Personal Notes, mas gostaria de destacar aqui a minha favorita: usar kubectl create ingress --help e copiar o exemplo de ingress "anotado". Isso vai te economizar MUITO tempo.
* Não sei com qual frequência esse tipo de questão aparece, mas tenho quase certeza de que perdi meus 2 pontos no CKAD por causa de um desafio com Ingress que estava usando Traefik em vez de NGINX, então sugiro que você se prepare para desafios com Traefik, também. Eu não estava preparado e perdi 2 pontos.
* NetworkPolicies são sempre complicadas, e elas também vão te assombrar aqui. Dedique um bom tempo para estudar e entender como elas funcionam, como permitir, como bloquear e tudo o que suas aplicações precisam para funcionar corretamente. Certifique-se de ler essas questões com atenção e saiba como acessar rapidamente os exemplos de NetworkPolicy na documentação.

## Dicas extras

> Lembre-se de que este exame pede para você analisar todos esses tópicos sob a perspectiva de um Desenvolvedor.

> Na minha CKAD, jsonpath não foi tão exigido quanto na CKA, mas tenha em mente que jsonpath será muito útil para você aqui, pois você precisará adicionar suas descobertas a um arquivo.