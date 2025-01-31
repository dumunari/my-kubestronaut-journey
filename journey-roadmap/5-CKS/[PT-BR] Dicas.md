# [CKS] Certified Kubernetes Security Specialist

## Dica para todos exames
> [!TIP] 
> Sempre que você agendar seu exame, poderá começar a fazê-lo 30 minutos antes do horário marcado.

> USE ESSA POSSIBILIDADE, esse tempo adicional ajuda muito caso você encontre algum problema, como comentei no meu post do Medium.

## Dicas para CKA, CKAD e CKS
> Sempre que você agendar seu exame, você receberá um simulado da [Killer.sh](https://killer.sh/). 

> Este simulado é bem similar e, às vezes, até mais difícil do que o exame original, faça-o o máximo de vezes possível. Ele ficará disponível por 36 horas após o primeiro acesso.

> Durante o exame real, se você não tiver certeza sobre uma pergunta, marque-a para revisar depois e continue. O tempo é crucial nesses exames.

## Dica para CKS
> [!CAUTION] 
> Principalmente nessa prova você precisará tomar MUITO cuidado com o tempo. Análise a questão e faça até onde você consegue. Se acabar travando, marque-a e siga pra próxima, essa prova é bastante extensa.

## Introdução

Here comes the pain 🙂
E não, (infelizmente) não é a música do Slipknot, é a CKS.

CKS é um dos 3 exames HandsOn, e o mais difícil. Aqui, você será desafiado a realizar tarefas de segurança que vão testar suas habilidades em Kubernetes, Sistemas Operacionais e Redes. Além disso, há muitas ferramentas adicionais que você precisará usar, como Falco, kube-bench, Trivy e assim por diante. De Hardening de Cluster a Minimização de footprints, você será desafiado com tarefas bem interessantes que farão você pensar fora da caixa.

Você pode encontrar os [Tópicos do Exame aqui](https://training.linuxfoundation.org/certification/certified-kubernetes-security-specialist/).

## Qual curso fazer?
Para a CKS, recomendo fortemente o curso [Certified Kubernetes Security Specialist (CKS)](https://learn.kodekloud.com/user/courses/certified-kubernetes-security-specialist-cks) do [Mumshad Mannambeth](https://www.linkedin.com/in/mmumshad/) na [KodeKloud](https://learn.kodekloud.com/).

Mumshad Mannambeth e a equipe da KodeKloud são especializados em conteúdo de Kubernetes e abordam todos os tópicos com muitos detalhes.

Além disso, há HandsOn Labs muito bem preparados após cada tópico.

No final, você também encontrará alguns Simulados.

Você também encontrará alguns [CKS Challenges](https://learn.kodekloud.com/user/courses/cks-challenges) na [KodeKloud](https://learn.kodekloud.com/). Eu recomendo que você os faça, se puder.

Além disso, recomendo passar por todos os [KillerCoda Interactive Scenarios for Kubernetes Security](https://killercoda.com/killer-shell-cks).

## Dicas
Como você já sabe, o CKS é um exame HandsOn, composto por cerca de 16 desafios.

>Tempo de prova: 120 minutos ⏳

>Pontuação Necessária: 67 🎯

>Minha pontuação: 74 ✅ 😰

Passando pelos tópicos do exame, aqui estão algumas dicas baseadas na minha própria experiência, com base nos tópicos abaixo. 

>Todas essas dicas estão bem detalhadas no arquivo [[CKS] Personal Notes:Anotações](./[CKS]%20Personal%20notes:Anotações.pdf)

Cluster Setup - 15%
* Aqui, você precisará aplicar algumas configurações de segurança nos componentes do cluster. Você receberá um relatório do kube-bench para orientá-lo nesta tarefa, então leia-o com atenção;
* NetworkPolicies estão aqui novamente. Você precisará usá-las para proteger o acesso ao cluster.
* Lembra dos Ingresses? Eles também voltaram. Aqui, você precisará criar/alterar um Ingress com a configuração adicional de TLS. Certifique-se de estar afiado na criação de Secrets do tipo TLS.
* Uma tarefa que parece fácil, mas é bem complicada, é verificar os binários. NÃO confie nos seus olhos. Gere o hash de cada binário e adicione-o em um arquivo, depois compare o conteúdo dos dois arquivos usando o comando diff. Eu não sei se é a melhor forma de fazer isso, mas foi assim que funcionou para mim.

Cluster Hardening - 15%
* ServiceAccounts serão explorados aqui, mas principalmente para garantir que eles não tenham permissões desnecessárias. Além disso, o automounting também aparecerá. Lembre-se de como configurá-lo nos níveis de Pod e ServiceAccount.
* A configuração de acesso à API do Kubernetes também será abordada;
* Alterações na configuração do Kubelet também são frequentemente solicitadas. Há informações detalhadas sobre isso no arquivo de Anotações, leia-o com atenção;
* A atualização do Cluster Kubernetes também pode aparecer. Lembre-se das lições da CKA para passar por isso com facilidade;
* Não tenho certeza se esta é a seção certa, mas certifique-se de entender como recuperar segredos diretamente do etcd via etcdctl e como habilitar a criptografia de segredos em repouso. Tenho 90% de certeza de que você enfrentará uma tarefa como essa.

System Hardening - 10%
* A redução da superfície de ataque será abordada aqui. Isso pode ser explorado de várias formas;
* NetworkPolicies também aparecerão aqui;
* A aplicação de profiles Seccomp e AppArmor também será solicitada. Certifique-se de entender como habilitar os profiles no AppArmor e como configurar corretamente esses perfis Seccomp para serem utilizados.

Minimize Microservice Vulnerabilities - 20%
* Aqui, você precisará aplicar os Pod Security Standards;
* Técnicas de isolamento, como multi-tenancy soft e hard, e outras técnicas de isolamento aparecerão aqui;
* Lembra das NetworkPolicies? Elas podem ficar mais complexas. Aqui, você precisará implementar algumas CiliumNetworkPolicies. Para ser bem sincero, elas não são muito diferentes das convencionais, então, fique tranquilo, é basicamente uma diferença de sintaxe. Mas há 2 pontos muito importantes a entender que diferem das NetworkPolicies convencionais. Preste atenção em [ICMP/ICMPv6](https://docs.cilium.io/en/stable/security/policy/language/#example-icmp-icmpv6) e como aplicar [Mutual Authentication](https://docs.cilium.io/en/v1.16/network/servicemesh/mutual-authentication/mutual-authentication-example/). A parte boa é que Cilium NetworkPolicies têm uma excelente [Documentação](https://docs.cilium.io/en/v1.16/security/policy/#network-policy), cheia de exemplos.

Supply Chain Security - 20%
* Aqui, você precisará realizar o hardening de imagens. Certifique-se de procurar por versões de componentes muito amplas, usuário root e uso inadequado do comando COPY;
* Além disso, você pode ser solicitado a gerar alguns SBOM usando ferramentas como sbom e Trivy. Ambas são bem simples. Dê uma olhada no comando help do cli e você estará tranquilo;
* Você também precisará realizar verificações de imagem usando o Trivy.

Monitoring, Logging and Runtime Security - 20%
* Aqui, você precisará usar ferramentas como o Falco. Certifique-se de entender como o Falco funciona, como ajustar regras e verificar os resultados;
* A imutabilidade de containers também será cobrada, então certifique-se de saber como garantir isso;
* Você será precisará habilitar os Audit logs, certifique-se de saber como ativá-los e configurá-los. Por favor, preste atenção no Volume Mounting;
* Não tenho certeza se isso será abordado nesta seção, mas a configuração de admission plugins como ImagePolicyWebhook certamente será solicitada. Só para reforçar, por favor, preste atenção no Volume Mounting e na configuração do arquivo kubeconfig específico.

## Dicas extras

> [!WARNING]
> Caso você não tenha a skill de administração Linux, recomendo fortemente procurar um curso antes de encarar a CKS. Você precisará realizar várias tarefas de administrador de sistemas, como identificar o PID de um processo, encontrar binários e verificar versões de pacotes.