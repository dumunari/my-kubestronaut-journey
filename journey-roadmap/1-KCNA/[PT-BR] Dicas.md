# [KCNA] Kubernetes and Cloud Native Associate

## Dica para todos exames
> [!TIP] 
> Sempre que você marca uma prova, você pode começar com 30 minutos de antecedência do horário marcado.

> USE ESSA POSSIBILIDADE, esse tempo adicional ajuda muito caso você encontre algum problema, como comentei no meu post do Medium.

## Introdução

O KCNA é uma excelente introdução ao ecossistema Cloud Native e Kubernetes. Ele te leva desde as fundações do Cloud Native, Linux Foundation e CNCF até uma visão básica, mas sólida, de como o Kubernetes funciona, juntamente com outras ferramentas para Observabilidade, Stirage, Service Mesh, práticas de DevOps e GitOps.

Você pode encontrar os [Tópicos do Exame aqui](https://training.linuxfoundation.org/certification/kubernetes-cloud-native-associate/).

## Qual curso fazer?

Para a KCNA, recomendo fortemente o curso do [James Spurin](https://www.linkedin.com/in/jamesspurin/)  [Kubernetes Certified (KCNA) + Hands On Labs + Practice Exams](https://www.udemy.com/course/dive-into-cloud-native-containers-kubernetes-and-the-kcna/?srsltid=AfmBOooZb6PVZkBkO1fxFovRyuZQ3BZl8CuE6DOzCvkUy062yXyPlYfK&couponCode=KEEPLEARNINGBR) na Udemy.

James passa por todos os tópicos necessários para o exame KCNA de forma muito detalhada e com uma didática impressionante.

Além disso, os Labs HandsOn são muito bem preparados e ajudam a aplicar toda a teoria aprendi, enquanto fornece diversas ferramentas para os próximos exames. Esse curso me ajudou demais nas provas CKA e CKAD.

No final, ainda tem alguns Simulados que são bastante parecidos com o exame real.

## Dicas

Como você já sabe, a KCNA é um exame de múltipla escolha, com 60 questões.

>Tempo do exame: 120 minutos ⏳

>Pontuação necessária: 75 🎯

>Minha pontuação: 93 ✅

Ao revisar os tópicos do exame, aqui estão algumas dicas baseadas na minha experiência, de acordo com os tópicos abaixo.

>Todas essas dicas estão bem detalhadas no arquivo [[KCNA] Personal Notes:Anotações](./[KCNA]%20Personal%20notes:Anotações.pdf).

### Kubernetes Fundamentals - 46%
* As funções do Kubelet são bastante exploradas, então, tenha em mente suas responsabilidades;
* Você será questionado sobre os diferentes Container Runtimes (kata, gVisor). Lembre-se de suas vantagens, desvantagens e objetivos;
* Você também será questionado sobre os níveis de Container Runtime e suas responsabilidades. Certifique-se de entender os propósitos e responsabilidades dos Container Runtimes Low level e High level;
* Por fim, é importante conhecer a responsabilidade de cada componente do Kubernetes.

### Container Orchestration - 22%
* Aqui, você também será questionado sobre outras ferramentas de Orquestração de Containers, não apenas o Kubernetes. Claro, não será necessário entender todos os detalhes dessas ferramentas, pois isso não faz parte do exame, mas é importante conhecer o básico sobre outras ferramentas como Apache Mesos, OpenShift e Docker Compose.

### Cloud Native Architecture - 16%
* Aqui, você será questionado sobre o básico de Resiliência, Agilidade, Operabilidade e Observabilidade;
* Conheça as diferenças entre Microserviços e Monólitos;
* Entenda o ciclo de vida de uma aplicação junto com as práticas de pipelines automatizados e o propósito de cada etapa do CI/CD;
* Conceitos básicos de Service Discovery, velocidade/eficiência versus custo e os pilares principais da Arquitetura Cloud Native também são cobrados aqui.

### Cloud Native Observability - 8%
* Entenda a diferença entre Logs, Métricas e Tracing;
* Conheça o básico sobre Grafana e Prometheus;
* Aqui, você também será questionado sobre Gestão de Custos, então, conheça os diferentes tipos de Ofertas de Instâncias, Rightsizing, Autoscaling e Detecção de Anomalias.

### Cloud Native Application Delivery - 8%
* Aqui você terá seu primeiro contato com GitOps, então conheça o conceito;
* Entenda o básico sobre ArgoCD e Flux, juntamente com suas diferenças e objetivos.
