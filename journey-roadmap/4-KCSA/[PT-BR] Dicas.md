# [KCSA] Kubernetes and Cloud Native Security Associate

## Dica para todos exames
> [!TIP] 
> Sempre que você marca uma prova, você pode começar com 30 minutos de antecedência do horário marcado.

> USE ESSA POSSIBILIDADE, esse tempo adicional ajuda muito caso você encontre algum problema, como comentei no meu post do Medium.

## Introdução

KCSA é uma introdução desafiadora ao ecossistema de Segurança Cloud Native. Quando digo desafiadora, digo isso de forma positiva. A KCSA pode parecer fácil de passar, mas ela tem algumas perguntas realmente boas que vão fazer você pensar, então venha preparado, não será de graça. Além disso, ela vai te levar de uma visão geral de Segurança Cloud Native, passando por Segurança de Componentes do Cluster, Modelagem de Ameaças, Segurança da Plataforma e Frameworks de Segurança e Compliance. Você conhecerá muitas ferramentas que irão te ajudar na sua jornada de segurança.

Você pode encontrar os [Tópicos do Exame aqui](https://training.linuxfoundation.org/certification/kubernetes-and-cloud-native-security-associate-kcsa/).

## Qual curso fazer?

Para a KCSA, recomendo fortemente o curso [Kubernetes and Cloud Native Security Associate (KCSA)](https://learn.kodekloud.com/user/courses/kubernetes-and-cloud-native-security-associate-kcsa) do [Mumshad Mannambeth's](https://www.linkedin.com/in/mmumshad/) na [KodeKloud](https://learn.kodekloud.com/).

Mumshad Mannambeth e a equipe da KodeKloud são especializados em conteúdo de Kubernetes e abordam todos os tópicos com muitos detalhes.

Além disso, há HandsOn Labs muito bem preparados após cada tópico.

No final, você também encontrará alguns Simulados.

> [!IMPORTANT] 
> Aqui vai uma Dica de OURO para a KCSA. Use o [Kubernetes Security KCSA Mock Exam](https://kubernetes-security-kcsa-mock.vercel.app/) do [Thiago](https://www.linkedin.com/in/thiago4go/). As questões são muito parecidas com as questões da prova de verdade, então se você tirar uma bota nota aqui, você tirará uma bota nota na prova de verdade. Inclusive, quem quiser, pode accesar o [GitHub do Projeto](https://github.com/thiago4go/kubernetes-security-kcsa-mock).

## Dicas

Como você já sabe, a KCSA é um exame de múltipla escolha, com 60 questões.

>Tempo do exame: 120 minutos ⏳

>Pontuação necessária: 75 🎯

>Minha pontuação: 87 ✅

Ao revisar os tópicos do exame, aqui estão algumas dicas baseadas na minha experiência, de acordo com os tópicos abaixo.

>Todas essas dicas estão bem detalhadas no arquivo [[KCSA] Personal Notes:Anotações](./[KCSA]%20Personal%20notes:Anotações.pdf).

Overview of Cloud Native Security - 14%
* Lembre-se dos 4Cs, responsabilidades compartilhadas entre o Provedor de Nuvem e a segurança da Infraestrutura, além das técnicas de isolamento;
* Repositórios de Artefatos e Segurança de Imagens também são tópicos importantes;
* A Segurança do Código da Aplicação também será cobrada.

Kubernetes Cluster Component Security - 22%
* Aqui você precisará fornecer maneiras de configurar todos os componentes do Kubernetes de forma segura, então entenda como mantê-los seguros;
* As questões irão desde os próprios Componentes até objetos do Kubernetes como Pods, Volumes, etc.

Kubernetes Security Fundamentals - 22%
* Aqui você precisará responder sobre osPod Security Standards e Pod Security Admissions;
* AuthN e AuthZ entre os componentes também serão abordadas;
* Como isolar workloads de maneira soft ou hard também será solicitado;
* A configuração de Audit Logs será exigida, então lembre-se dos passos para ativá-la;
* E, claro, as queridas(?) NetworkPolicies.

Kubernetes Threat Model - 16%
* Threat Modelling é uma área ampla, mas você será questionado sobre boundaries, como os dados fluem em seu ecossistema e de quantas maneiras um atacante pode explorar seu ambiente;
* Entenda como código ou acesso malicioso podem afetar seu ambiente;
* Além disso, manter dados sensíveis seguros e evitar escalonamento de privilégios são pontos importantes a serem observados aqui.

Platform Security - 16%
* Preste atenção à Segurança de Supply Chain e à segurança dos Repositórios de Artefatos;
* A Infraestrutura de Chave Pública (PKI) é um ponto importante a ser observado aqui;
* Admission controllers são frequentemente abordados, então conheça os mais utilizados.

Compliance and Security Frameworks - 10%
* Aqui você será questionado sobre os focos e objetivos de cada um dos Frameworks de Compliance;
* Ferramentas para automatizar esses processos também serão exigidas, então certifique-se de entendê-las (são muitas) e saber quando usar cada uma.