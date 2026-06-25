# Comopassei: AWS-Cloud-practitioner

Resumo AWS Cloud Practitioner: Tudo o que Você Precisa Saber
Introdução à AWS e Modelos de Implantação
A AWS (Amazon Web Services) é a maior plataforma de computação em nuvem do mundo,
oferecendo uma vasta gama de serviços. Ela opera em um modelo cliente-servidor, onde seus
aplicativos e usuários fazem requisições a servidores na nuvem.
Existem três modelos de implantação em nuvem:
• Baseada na nuvem: Aplicações são criadas ou migradas diretamente para a nuvem da AWS.
On-premises (nuvem privada): Recursos são implantados e gerenciados localmente na sua
própria infraestrutura, usando tecnologias de virtualização.
•
Híbrida: Combina recursos da nuvem AWS com sua infraestrutura on-premises, ideal para
aplicações legadas ou requisitos regulatórios.
•
Benefícios da Computação em Nuvem:
Pague pelo uso (OpEx em vez de CapEx): Troque despesas iniciais (Capital Expenditure -
CapEx) por despesas variáveis (Operational Expenditure - OpEx), pagando apenas pelo que
usar.
•

Redução de custos com data centers: Não há necessidade de manter e operar infraestrutura
física própria.
•
Flexibilidade de capacidade: Adapte-se à demanda sem adivinhar a capacidade necessária,
escalando para cima ou para baixo.
•
Economias de escala: Beneficie-se de custos mais baixos devido ao grande volume de usuários
da AWS.
•
• Aumento de velocidade e agilidade: Implante e escale recursos rapidamente.
• Alcance global: Disponibilize seus serviços em minutos em múltiplas regiões geográficas.
Serviços Essenciais de Computação
A base de qualquer aplicação na AWS:
Amazon Elastic Compute Cloud (Amazon EC2): Fornece capacidade de computação segura e
redimensionável na nuvem através de instâncias virtuais. Você provisiona, inicia e paga
apenas pelo tempo de execução.
•

Tipos de Instâncias: Existem instâncias otimizadas para uso geral, computação, memória,
armazenamento e computação acelerada, cada uma para um caso de uso específico.
•
AMI (Amazon Machine Image): Um modelo que contém a configuração de software (SO,
servidor de aplicação, etc.) necessária para iniciar uma instância EC2.
•
• Modelos de Compra:
Sob Demanda: Pague pelo uso por hora, sem compromissos. Ideal para cargas de trabalho
imprevisíveis.
•
Savings Plans / Instâncias Reservadas (RIs): Oferecem economias significativas para
compromissos de 1 ou 3 anos, ideais para cargas de trabalho previsíveis.
•
Instâncias Spot: Oferecem os maiores descontos, mas são adequadas para cargas de trabalho
flexíveis que podem ser interrompidas, pois a AWS pode recuperá-las com pouco aviso (não
para aplicações contínuas).
•

Amazon Lightsail: Serviço simplificado para lançar aplicativos web e blogs de pequena escala,
fornecendo VMs pré-configuradas com tudo o que você precisa.
•
Amazon EC2 Auto Scaling: Adiciona ou remove automaticamente instâncias EC2 em resposta
à demanda, garantindo que seu aplicativo tenha a capacidade certa. Pode ser dinâmico (reage
a mudanças) ou preditivo (baseado na demanda prevista).
•

Elastic Load Balancing (ELB): Distribui automaticamente o tráfego de entrada de aplicações
entre várias instâncias EC2, garantindo alta disponibilidade e desempenho.
•
Computação sem Servidor e Contêineres
Foco em executar código sem gerenciar a infraestrutura subjacente.
RESUMO
domingo, 30 de novembro de 2025 00:41

Página 32 de AWS CLOUD PRACTITIONER

Foco em executar código sem gerenciar a infraestrutura subjacente.
Computação Sem Servidor: Você executa seu código sem provisionar ou gerenciar servidores,
focando apenas na lógica do negócio.
•
AWS Lambda: Executa código em resposta a eventos (ex: upload de arquivo, requisição HTTP),
sem necessidade de gerenciar servidores. Você paga apenas pelo tempo de computação
consumido.
•

Contêineres: Uma forma de empacotar código, configurações e dependências em um único
objeto para portabilidade e escalabilidade.
•
Amazon Elastic Container Service (Amazon ECS): Sistema de gerenciamento de contêineres
altamente escalável para executar aplicações Docker.
•
Amazon Elastic Kubernetes Service (Amazon EKS): Serviço totalmente gerenciado para
executar Kubernetes na AWS.
•
AWS Fargate: Mecanismo de computação sem servidor para contêineres, funcionando com
ECS e EKS, eliminando a necessidade de gerenciar servidores.
•
Amazon Elastic Container Registry (ECR): Registro de imagem de contêiner totalmente
gerenciado para armazenar, gerenciar e implantar imagens Docker.
•
Redes
Conectividade e isolamento de seus recursos na nuvem.
Amazon Virtual Private Cloud (Amazon VPC): Permite provisionar uma seção isolada da
nuvem AWS para executar seus recursos em uma rede virtual definida por você.
•
Sub-rede: Uma seção da VPC que pode conter recursos. Pode ser pública (acessível da
internet) ou privada (acessível apenas pela sua rede privada).
•
• Gateway de Internet: Conecta sua VPC à internet.

Gateway Privado Virtual: Permite uma conexão VPN entre sua VPC e uma rede privada (on-
premises).

•
AWS Direct Connect: Conexão privada dedicada de alta largura de banda entre seu data
center e uma VPC, bypassando a internet pública.
•
AWS Transit Gateway: Conecta várias VPCs e redes locais através de um único gateway,
simplificando a arquitetura de rede e permitindo controle centralizado.
•
Emparelhamento de VPC: Conecta duas VPCs para compartilhar recursos, mas não permite
emparelhamento transitivo (VPC A conectada a B não conecta B a C automaticamente).
•
VPC Endpoints: Conectam sua VPC a serviços AWS e serviços de endpoint PrivateLink de forma
privada, sem precisar de acesso público à internet.
•
• Segurança de Rede:
Lista de Controle de Acesso (ACL) de Rede: Firewall virtual no nível da sub-rede. É stateless
(não lembra decisões anteriores).
•
Grupos de Segurança: Firewall virtual no nível da instância EC2. É stateful (lembra decisões
anteriores).
•
Amazon Route 53: Serviço web de DNS (Sistema de Nomes de Domínio) que roteia usuários
para aplicações na AWS ou fora dela, convertendo nomes de domínio em endereços IP.
•
Amazon Elastic IP (EIP): Fornece um endereço IPv4 estático que você pode associar a uma
instância EC2, ideal para necessidades dinâmicas.
•
Armazenamento
Opções para guardar seus dados de forma segura e escalável.
Armazenamento de Instância: Armazenamento temporário, fisicamente anexado à instância
EC2. Os dados são perdidos quando a instância é encerrada.
•
Amazon Elastic Block Store (Amazon EBS): Fornece volumes de armazenamento em nível de
bloco que persistem independentemente da vida útil da instância EC2.
•
Snapshots do Amazon EBS: Backups incrementais de volumes EBS, onde apenas os blocos de
dados alterados são salvos após o primeiro backup completo.
•
Amazon Simple Storage Service (Amazon S3): Serviço de armazenamento de objetos
altamente escalável e durável que armazena dados em buckets. Oferece espaço de
armazenamento ilimitado e suporta arquivos de até 5 TB.
•

• Classes de Armazenamento S3: Escolha com base na frequência de acesso e disponibilidade:
• S3 Standard: Para dados acessados frequentemente, alta disponibilidade (mínimo 3 AZs).
• S3 Standard – Infrequent Access (S3 Standard-IA): Para dados acessados com pouca
Página 33 de AWS CLOUD PRACTITIONER

S3 Standard – Infrequent Access (S3 Standard-IA): Para dados acessados com pouca
frequência, mas que precisam de alta disponibilidade.
•
S3 One Zone-Infrequent Access (S3 One Zone – IA): Armazena dados em uma única AZ, ideal
para economizar custos onde os dados podem ser reproduzidos facilmente.
•
S3 Intelligent-Tiering: Monitora padrões de acesso e move objetos automaticamente entre os
níveis de acesso frequente e infrequente para otimizar custos.
•
S3 Glacier Instant Retrieval: Para dados arquivados que requerem acesso imediato
(milissegundos).
•
S3 Glacier Flexible Retrieval: Armazenamento de baixo custo para arquivamento de dados,
com recuperação em minutos a horas.
•
S3 Glacier Deep Archive: O menor custo de armazenamento para arquivamento de longo
prazo, com recuperação em 12 a 48 horas.
•
S3 Versioning: Permite manter múltiplas versões de um objeto em um único bucket,
preservando versões anteriores em caso de atualizações ou exclusões.
•
S3 Outposts: Cria buckets S3 em ambientes AWS Outposts on-premises, para dados que
precisam permanecer no local.
•
Amazon Elastic File System (Amazon EFS): Sistema de armazenamento de arquivos escalável
onde múltiplos clientes podem acessar os mesmos dados em pastas de arquivos
compartilhadas. É um serviço regional que armazena dados em múltiplas Zonas de
Disponibilidade.
•

Diferença EBS vs. EFS: EBS armazena dados em uma única Zona de Disponibilidade e precisa
estar na mesma AZ da instância EC2. EFS armazena dados em múltiplas Zonas de
Disponibilidade e é regional.
•

Bancos de Dados na AWS
Diversas opções para armazenar e gerenciar seus dados.
Bancos de Dados Relacionais (SQL): Usam SQL para armazenar e consultar dados em tabelas
com relações.
•
Amazon Relational Database Service (Amazon RDS): Serviço gerenciado para executar bancos
de dados relacionais populares (Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, SQL
Server). Automatiza tarefas como provisionamento, backups e patches.
•

Amazon Aurora: Banco de dados relacional de alto desempenho compatível com MySQL e
PostgreSQL, até 5x mais rápido que MySQL e 3x mais rápido que PostgreSQL. Replica 6 cópias
dos dados em 3 AZs.
•

Bancos de Dados Não Relacionais (NoSQL): Usam estruturas diferentes de linhas e colunas
(ex: chave-valor, documentos).
•
Amazon DynamoDB: Serviço de banco de dados de chave-valor e documento sem servidor,
oferecendo desempenho de milissegundos em qualquer escala.
•
• Amazon DocumentDB: Serviço de banco de dados de documentos compatível com MongoDB.
Amazon Neptune: Serviço de banco de dados de grafo para conjuntos de dados altamente
conectados (ex: mecanismos de recomendação, detecção de fraude).
•
Amazon Redshift: Serviço de data warehouse para análise de Big Data, coletando dados de
diversas fontes.
•
• Serviços de Cache:
Amazon ElastiCache: Serviço de cache em memória que melhora os tempos de leitura de
bancos de dados (suporta Redis e Memcached).
•
Amazon DynamoDB Accelerator (DAX): Cache em memória para o DynamoDB, melhorando
tempos de resposta de milissegundos para microssegundos.
•
• Serviços de Migração de Banco de Dados:
AWS Database Migration Service (AWS DMS): Permite migrar bancos de dados relacionais e
não relacionais, mantendo o banco de dados de origem operacional.
•
AWS Application Migration Service (MGN): Solução automatizada de "lift-and-shift" para
migrar servidores físicos, bancos de dados e aplicações para instâncias EC2.
•
Sistema de Mensagens e Enfileiramento
Para construir aplicações distribuídas e desacopladas.
Aplicações Monolíticas: Componentes fortemente acoplados; a falha de um pode afetar todo
o sistema.
•

Página 34 de AWS CLOUD PRACTITIONER

o sistema.
Microsserviços: Componentes fracamente acoplados; a falha de um não necessariamente
derruba o aplicativo.
•
• Serviços que facilitam a integração de aplicações:
Amazon Simple Notification Service (Amazon SNS): Serviço de publicação/assinatura, onde
um editor envia mensagens para múltiplos assinantes (ex: e-mails, funções Lambda).
•
Amazon Simple Queue Service (Amazon SQS): Serviço de enfileiramento de mensagens para
enviar, armazenar e receber mensagens entre componentes de software sem perda de dados.
•
Segurança, Identidade e Conformidade
Protegendo seus dados e recursos na nuvem.
Modelo de Responsabilidade Compartilhada da AWS: Define as responsabilidades de
segurança:
•
AWS (Segurança da nuvem): Responsável pela proteção da infraestrutura global (hardware,
software, rede, virtualização, segurança física dos datacenters).
•
Cliente (Segurança na nuvem): Responsável pela segurança de tudo que cria e coloca na
nuvem (seleção e configuração de sistemas operacionais, grupos de segurança, gerenciamento
de contas de usuário, dados).
•

AWS Identity and Access Management (IAM): Permite gerenciar o acesso a serviços e
recursos da AWS com segurança.
•
Usuário-raiz da conta AWS: Identidade inicial com acesso completo (use apenas para tarefas
de faturamento e configuração inicial).
•
• Usuários do IAM: Identidades para pessoas ou aplicações, com permissões específicas.
Grupos do IAM: Conjuntos de usuários do IAM; políticas anexadas ao grupo se aplicam a todos
os usuários nele.
•
Políticas do IAM: Documentos que concedem ou negam permissões a serviços e recursos
AWS.
•
Perfis do IAM: Identidades que você pode assumir para obter acesso temporário a
permissões.
•
• Autenticação Multifator (MFA): Camada extra de segurança para sua conta AWS.
• Gerenciamento de Contas e Conformidade:
• AWS Organizations: Consolida e gerencia múltiplas contas AWS em um local central.
Políticas de Controle de Serviço (SCPs): Permitem restringir serviços, recursos e ações de API
em contas e Unidades Organizacionais (UOs).
•
AWS Artifact: Concede acesso sob demanda a relatórios de segurança e conformidade da AWS
e a contratos online.
•
• Proteção Contra Ameaças:
• AWS Shield: Protege aplicações contra ataques DDoS (Negação de Serviço Distribuída).
• Standard: Proteção gratuita contra os ataques DDoS mais comuns.
Advanced: Serviço pago com diagnósticos detalhados e mitigação de ataques DDoS
sofisticados.
•
AWS WAF (Web Application Firewall): Firewall de aplicação web que monitora e controla
solicitações de rede para aplicações web, usando ACLs da web (listas de controle de acesso).
•
Amazon Inspector: Realiza avaliações de segurança automatizadas em aplicações para
identificar vulnerabilidades e desvios de práticas recomendadas (foca em vulnerabilidades na
infraestrutura).
•

Amazon GuardDuty: Serviço de detecção inteligente de ameaças que monitora
continuamente a atividade da rede e o comportamento da conta na AWS (foca em atividades
e comportamentos maliciosos).
•

AWS Key Management Service (AWS KMS): Permite executar operações de criptografia
usando chaves de criptografia.
•
• SSE-S3: Criptografia do lado do servidor com chaves gerenciadas pelo S3.
• SSE-KMS: Criptografia do lado do servidor usando AWS KMS para auditoria e controle.
• SSE-C: Criptografia do lado do servidor onde o cliente fornece as chaves.
Customer Managed Key (CMK): Uma chave gerada e gerenciada pelo cliente dentro do AWS
KMS.
•
AWS CloudHSM (Hardware Security Module): Fornece um dispositivo físico dedicado para
armazenar e proteger chaves criptográficas, oferecendo um nível mais alto de segurança de
•

Página 35 de AWS CLOUD PRACTITIONER

armazenar e proteger chaves criptográficas, oferecendo um nível mais alto de segurança de
hardware.
AWS Secrets Manager: Armazena e gerencia segredos (credenciais de banco de dados, chaves
de API) de forma segura e centralizada, com rotação automática.
•
Amazon Macie: Usa machine learning e IA para descobrir, classificar e proteger
automaticamente dados sensíveis em buckets S3.
•
AWS Security Hub: Agrega, organiza e prioriza alertas e descobertas de segurança de outros
serviços AWS (GuardDuty, Inspector, Macie) e parceiros.
•
Infraestrutura Global da AWS
A AWS opera em uma arquitetura global resiliente e escalável:
Regiões: Locais físicos geograficamente isolados com múltiplos datacenters. A escolha de uma
região considera conformidade, proximidade com clientes, serviços disponíveis e preços.
•
Zonas de Disponibilidade (AZs): Datacenters isolados dentro de uma Região, garantindo baixa
latência entre eles e resiliência a desastres.
•
Locais de Borda (Edge Locations): Sites usados pelo Amazon CloudFront (serviço de CDN -
Content Delivery Network) para armazenar cópias em cache de conteúdo, próximos aos
clientes para entrega mais rápida.
•

Gerenciamento, Monitoramento e Automação
Ferramentas para operar e otimizar seu ambiente AWS.
• Formas de Interagir com os Serviços AWS:
• Console de Gerenciamento da AWS: Interface web para acessar e gerenciar serviços.
AWS Console Mobile Application: Para monitoramento e tarefas rápidas em dispositivos
móveis.
•
AWS Command Line Interface (AWS CLI): Ferramenta de linha de comando para controlar
serviços AWS via scripts.
•
Kits de Desenvolvimento de Software (SDKs): Facilitam o uso de serviços AWS em diferentes
linguagens de programação.
•
AWS Elastic Beanstalk: Implanta automaticamente os recursos necessários para executar
código, ajustando capacidade, balanceando carga, fazendo auto scaling e monitorando a
saúde (PaaS - Platform as a Service).
•

AWS CloudFormation: Permite definir a infraestrutura como código (IaC), provisionando
recursos de forma segura e repetível.
•
• Amazon CloudWatch: Serviço web para monitorar e gerenciar métricas e configurar alarmes.
• Métricas: Pontos de dados para seus recursos.
Alarmes do CloudWatch: Executam ações automáticas quando as métricas ultrapassam
limites.
•
AWS CloudTrail: Registra as chamadas de API realizadas em sua conta, fornecendo um log de
ações para auditoria e governança.
•
• CloudTrail Insights: Detecta automaticamente atividades de API incomuns.
AWS Trusted Advisor: Inspeciona seu ambiente AWS e faz recomendações em tempo real com
base nas melhores práticas da AWS em cinco categorias: otimização de custos, desempenho,
segurança, tolerância a falhas e limites de serviço.
•

AWS Personal Health Dashboard: Fornece eventos recentes sobre a saúde dos serviços AWS
que afetam sua conta, ajudando a gerenciar eventos ativos e planejar atividades programadas.
•
AWS Config: Monitora e registra continuamente as alterações de configuração de seus
recursos da AWS, permitindo avaliar a conformidade.
•
AWS Compute Optimizer: Analisa a configuração e as métricas de utilização de seus recursos
AWS para recomendar otimizações de custos e desempenho.
•
AWS X-Ray: Permite analisar e depurar aplicações distribuídas, fornecendo visibilidade de
ponta a ponta do comportamento e desempenho.
•
AWS Cloud9: Ambiente de desenvolvimento integrado (IDE) baseado na nuvem que permite
escrever, executar e depurar código diretamente do navegador.
•
AWS Service Catalog: Permite que as organizações criem e gerenciem catálogos de serviços de
TI para uso na AWS, garantindo conformidade.
•
Preço e Suporte
Entendendo os custos e as opções de ajuda.
Página 36 de AWS CLOUD PRACTITIONER

Entendendo os custos e as opções de ajuda.
Nível Gratuito da AWS: Permite usar determinados serviços gratuitamente por um período
específico (sempre gratuito, 12 meses gratuitos e versões de teste).
•
• Como funciona a definição de preço da AWS:
• Pague somente pelo que usar: Flexibilidade e economia.
• Pague menos ao fazer reserva: Descontos para uso contínuo (ex: Savings Plans).
Pague menos com descontos baseados em volume: Quanto mais você usa, menor o preço por
unidade.
•
• Calculadora de Preços da AWS: Permite estimar os custos de seus casos de uso na AWS.
• Gerenciamento de Custos e Faturamento:
Painel de Cobrança (Faturamento e Gerenciamento de Custos da AWS): Para pagar faturas,
monitorar uso e analisar custos.
•
Cobrança Consolidada: No AWS Organizations, permite uma única fatura para todas as contas
AWS de uma organização.
•
• AWS Budgets: Crie orçamentos para planejar uso e custos, e defina alertas personalizados.
AWS Cost Explorer: Ferramenta para visualizar, interpretar e gerenciar seus custos e uso da
AWS ao longo do tempo.
•
• Planos de Suporte da AWS:
Basic (Gratuito): Acesso limitado a verificações do Trusted Advisor, Personal Health
Dashboard, documentação e comunidades.
•
Desenvolvedor (Pago): Acesso a orientação de práticas recomendadas e ferramentas de
diagnóstico.
•
Empresarial (Pago): Todas as verificações do Trusted Advisor, suporte limitado para software
de terceiros e orientação.
•
Enterprise On-Ramp / Enterprise (Pagos): Acesso a Technical Account Managers (TAMs),
otimização de custos, e tempos de resposta rápidos para problemas críticos.
•
Technical Account Manager (TAM): Ponto de contato principal com a AWS para orientação
especializada.
•
AWS Concierge Support Team: Suporte especializado para clientes com infraestrutura ou
gastos significativos na AWS.
•
Migração para a Nuvem
Ferramentas e estratégias para mover suas cargas de trabalho.
AWS Migration Hub: Um local central para acompanhar o progresso das migrações de
aplicativos em várias soluções AWS e de parceiros.
•
AWS Cloud Adoption Framework (AWS CAF): Um plano estratégico e organizacional para a
jornada da sua empresa para a nuvem. Organiza orientações em seis perspectivas: Negócio,
Pessoas, Governança, Plataforma, Segurança e Operações.
•

• Estratégias de Migração (6 Rs):
• Rehost (Redefinir Hospedagem): Mover aplicações sem alterações (lift-and-shift).
Replatform (Redefinir Plataforma): Fazer otimizações na nuvem sem alterar a arquitetura
central (lift, tinker and shift).
•
Refactor (Refatoração/Rearquitetura): Reimaginando a arquitetura da aplicação usando
recursos nativos da nuvem.
•
• Repurchase (Recomprar): Mudar de uma licença tradicional para um modelo SaaS.
• Retain (Reter): Manter aplicações essenciais no ambiente de origem.
• Retire (Retirar): Remover aplicações que não são mais necessários.
AWS Snow Family: Coleção de dispositivos físicos para transportar grandes volumes de dados
para dentro e para fora da AWS.
•
AWS Snowcone: Dispositivo pequeno e robusto para transferência de dados e computação de
borda.
•
AWS Snowball Edge: Dispositivos para migrações de dados em larga escala e computação local
(Storage Optimized para capacidade, Compute Optimized para poder computacional).
•
AWS Snowmobile: Serviço de transferência de dados em escala de exabytes, usando um
contêiner de transporte puxado por caminhão.
•
AWS DataSync: Serviço de transferência de dados projetado para mover grandes quantidades
de dados entre sistemas de armazenamento on-premise e serviços da AWS, com criptografia
em trânsito.
•

Página 37 de AWS CLOUD PRACTITIONER

em trânsito.
Inovação e Outros Serviços Relevantes
A AWS oferece muito mais do que infraestrutura básica:
• Machine Learning (ML) e Inteligência Artificial (IA):
• Amazon SageMaker: Para construir, treinar e implantar modelos de ML.
• Amazon Transcribe: Converte fala em texto.
• Amazon Comprehend: Descobre padrões e insights em texto.
• Amazon Fraud Detector: Identifica atividades online potencialmente fraudulentas.
• Amazon Lex: Cria chatbots de voz e texto.
• Amazon Polly: Converte texto em fala.
• Amazon Personalize: Cria recomendações individualizadas para clientes usando ML.
• Amazon Rekognition: Análise e detecção facial em imagens e vídeos.
• Streaming de Dados:
Amazon Kinesis: Plataforma para streaming de dados, facilitando o carregamento e análise de
dados em tempo real.
•
• Pesquisa e Análise:
• Amazon Kendra: Serviço de pesquisa inteligente baseado em machine learning.
Amazon Athena: Serviço de consulta interativo e sem servidor que facilita a análise de dados
no Amazon S3 usando SQL padrão.
•
AWS Glue: Serviço de ETL (Extração, Transformação e Carregamento) totalmente gerenciado
para preparar e carregar dados para análise.
•
Amazon EMR (Elastic MapReduce): Plataforma de big data na nuvem para processar grandes
quantidades de dados usando ferramentas de código aberto (Hadoop, Spark, etc.).
•
• Autenticação e Gerenciamento de Usuários:
Amazon Cognito: Serviço totalmente gerenciado que fornece autenticação, autorização e
gerenciamento de usuários para aplicativos web e móveis (suporta provedores de identidade
social).
•

• Desenvolvimento e DevOps:
AWS CodeCommit: Serviço de controle de versão totalmente gerenciado que hospeda
repositórios Git seguros.
•
AWS CodePipeline: Serviço de entrega contínua que automatiza pipelines de lançamento para
atualizações rápidas.
•
• Ambientes de Trabalho Virtual:
• Amazon WorkSpaces: Solução de infraestrutura de desktop virtual (VDI) baseada na nuvem.
• Gerenciamento de Conformidade:
AWS Audit Manager: Ajuda a automatizar o processo de avaliação, gerenciamento e geração
de relatórios sobre conformidade.
•
• AWS Compliance Center: Local central para pesquisar requisitos regulatórios.
• Outros Serviços:
Amazon Pinpoint: Serviço escalável para interagir com clientes via e-mail, SMS, notificações
push.
•
AWS Control Tower: Ajuda a configurar e controlar um ambiente seguro e com várias contas
da AWS, baseado nas melhores práticas.
•
AWS Managed Services (AMS): Ajuda empresas a operar sua infraestrutura da AWS com mais
eficiência e segurança.
•
AWS Quick Start Reference Deployments: Modelos automatizados do CloudFormation para
implantar e configurar soluções rapidamente.
•
AWS Marketplace: Catálogo digital com milhares de ofertas de software de provedores
independentes.
•
AWS Partner Network (APN): Programa global de parceiros da AWS para ajudar organizações
a construir negócios ou soluções baseados na AWS.
•
Otimização e Melhores Práticas
AWS Well-Architected Framework: Ajuda a projetar e operar sistemas confiáveis, seguros,
eficientes e econômicos na nuvem AWS, baseado em seis pilares:
•
• Excelência Operacional: Executar e monitorar sistemas, melhorando processos.
1. Segurança: Proteger informações e ativos.
2. Confiabilidade: Recuperar-se de interrupções, escalar dinamicamente.
Página 38 de AWS CLOUD PRACTITIONER

2. Confiabilidade: Recuperar-se de interrupções, escalar dinamicamente.
3. Eficiência de Desempenho: Usar recursos computacionais de forma eficiente.
4. Otimização de Custos: Executar sistemas com o menor preço.
5. Sustentabilidade: Melhorar impactos ambientais, reduzindo o consumo de energia.
AWS Well-Architected Tool: Ajuda os clientes a revisar e melhorar suas cargas de trabalho
com base nas melhores práticas do Framework.
6.

Resumo AWS Cloud Practitioner: Tudo o que Você Precisa Saber
Introdução à AWS e Modelos de Implantação
A AWS (Amazon Web Services) é a maior plataforma de computação em nuvem do mundo,
oferecendo uma vasta gama de serviços. Ela opera em um modelo cliente-servidor, onde seus
aplicativos e usuários fazem requisições a servidores na nuvem.
Existem três modelos de implantação em nuvem:
• Baseada na nuvem: Aplicações são criadas ou migradas diretamente para a nuvem da AWS.
On-premises (nuvem privada): Recursos são implantados e gerenciados localmente na sua
própria infraestrutura, usando tecnologias de virtualização.
•
Híbrida: Combina recursos da nuvem AWS com sua infraestrutura on-premises, ideal para
aplicações legadas ou requisitos regulatórios.
•
Benefícios da Computação em Nuvem:
Pague pelo uso (OpEx em vez de CapEx): Troque despesas iniciais (Capital Expenditure -
CapEx) por despesas variáveis (Operational Expenditure - OpEx), pagando apenas pelo que
usar.
•

Redução de custos com data centers: Não há necessidade de manter e operar infraestrutura
física própria.
•
Flexibilidade de capacidade: Adapte-se à demanda sem adivinhar a capacidade necessária,
escalando para cima ou para baixo.
•
Economias de escala: Beneficie-se de custos mais baixos devido ao grande volume de usuários
da AWS.
•
• Aumento de velocidade e agilidade: Implante e escale recursos rapidamente.
• Alcance global: Disponibilize seus serviços em minutos em múltiplas regiões geográficas.
Serviços Essenciais de Computação
A base de qualquer aplicação na AWS:
Amazon Elastic Compute Cloud (Amazon EC2): Fornece capacidade de computação segura e
redimensionável na nuvem através de instâncias virtuais. Você provisiona, inicia e paga
apenas pelo tempo de execução.
•

Tipos de Instâncias: Existem instâncias otimizadas para uso geral, computação, memória,
armazenamento e computação acelerada, cada uma para um caso de uso específico.
•
AMI (Amazon Machine Image): Um modelo que contém a configuração de software (SO,
servidor de aplicação, etc.) necessária para iniciar uma instância EC2.
•
• Modelos de Compra:
Sob Demanda: Pague pelo uso por hora, sem compromissos. Ideal para cargas de trabalho
imprevisíveis.
•
Savings Plans / Instâncias Reservadas (RIs): Oferecem economias significativas para
compromissos de 1 ou 3 anos, ideais para cargas de trabalho previsíveis.
•
Instâncias Spot: Oferecem os maiores descontos, mas são adequadas para cargas de trabalho
flexíveis que podem ser interrompidas, pois a AWS pode recuperá-las com pouco aviso (não
para aplicações contínuas).
•

Amazon Lightsail: Serviço simplificado para lançar aplicativos web e blogs de pequena escala,
fornecendo VMs pré-configuradas com tudo o que você precisa.
•
Amazon EC2 Auto Scaling: Adiciona ou remove automaticamente instâncias EC2 em resposta
à demanda, garantindo que seu aplicativo tenha a capacidade certa. Pode ser dinâmico (reage
a mudanças) ou preditivo (baseado na demanda prevista).
•

Elastic Load Balancing (ELB): Distribui automaticamente o tráfego de entrada de aplicações
entre várias instâncias EC2, garantindo alta disponibilidade e desempenho.
•

Página 39 de AWS CLOUD PRACTITIONER

entre várias instâncias EC2, garantindo alta disponibilidade e desempenho.
Computação sem Servidor e Contêineres
Foco em executar código sem gerenciar a infraestrutura subjacente.
Computação Sem Servidor: Você executa seu código sem provisionar ou gerenciar servidores,
focando apenas na lógica do negócio.
•
AWS Lambda: Executa código em resposta a eventos (ex: upload de arquivo, requisição HTTP),
sem necessidade de gerenciar servidores. Você paga apenas pelo tempo de computação
consumido.
•

Contêineres: Uma forma de empacotar código, configurações e dependências em um único
objeto para portabilidade e escalabilidade.
•
Amazon Elastic Container Service (Amazon ECS): Sistema de gerenciamento de contêineres
altamente escalável para executar aplicações Docker.
•
Amazon Elastic Kubernetes Service (Amazon EKS): Serviço totalmente gerenciado para
executar Kubernetes na AWS.
•
AWS Fargate: Mecanismo de computação sem servidor para contêineres, funcionando com
ECS e EKS, eliminando a necessidade de gerenciar servidores.
•
Amazon Elastic Container Registry (ECR): Registro de imagem de contêiner totalmente
gerenciado para armazenar, gerenciar e implantar imagens Docker.
•
Redes
Conectividade e isolamento de seus recursos na nuvem.
Amazon Virtual Private Cloud (Amazon VPC): Permite provisionar uma seção isolada da
nuvem AWS para executar seus recursos em uma rede virtual definida por você.
•
Sub-rede: Uma seção da VPC que pode conter recursos. Pode ser pública (acessível da
internet) ou privada (acessível apenas pela sua rede privada).
•
• Gateway de Internet: Conecta sua VPC à internet.

Gateway Privado Virtual: Permite uma conexão VPN entre sua VPC e uma rede privada (on-
premises).

•
AWS Direct Connect: Conexão privada dedicada de alta largura de banda entre seu data
center e uma VPC, bypassando a internet pública.
•
AWS Transit Gateway: Conecta várias VPCs e redes locais através de um único gateway,
simplificando a arquitetura de rede e permitindo controle centralizado.
•
Emparelhamento de VPC: Conecta duas VPCs para compartilhar recursos, mas não permite
emparelhamento transitivo (VPC A conectada a B não conecta B a C automaticamente).
•
VPC Endpoints: Conectam sua VPC a serviços AWS e serviços de endpoint PrivateLink de forma
privada, sem precisar de acesso público à internet.
•
• Segurança de Rede:
Lista de Controle de Acesso (ACL) de Rede: Firewall virtual no nível da sub-rede. É stateless
(não lembra decisões anteriores).
•
Grupos de Segurança: Firewall virtual no nível da instância EC2. É stateful (lembra decisões
anteriores).
•
Amazon Route 53: Serviço web de DNS (Sistema de Nomes de Domínio) que roteia usuários
para aplicações na AWS ou fora dela, convertendo nomes de domínio em endereços IP.
•
Amazon Elastic IP (EIP): Fornece um endereço IPv4 estático que você pode associar a uma
instância EC2, ideal para necessidades dinâmicas.
•
Armazenamento
Opções para guardar seus dados de forma segura e escalável.
Armazenamento de Instância: Armazenamento temporário, fisicamente anexado à instância
EC2. Os dados são perdidos quando a instância é encerrada.
•
Amazon Elastic Block Store (Amazon EBS): Fornece volumes de armazenamento em nível de
bloco que persistem independentemente da vida útil da instância EC2.
•
Snapshots do Amazon EBS: Backups incrementais de volumes EBS, onde apenas os blocos de
dados alterados são salvos após o primeiro backup completo.
•
Amazon Simple Storage Service (Amazon S3): Serviço de armazenamento de objetos
altamente escalável e durável que armazena dados em buckets. Oferece espaço de
armazenamento ilimitado e suporta arquivos de até 5 TB.
•

Página 40 de AWS CLOUD PRACTITIONER

armazenamento ilimitado e suporta arquivos de até 5 TB.
• Classes de Armazenamento S3: Escolha com base na frequência de acesso e disponibilidade:
• S3 Standard: Para dados acessados frequentemente, alta disponibilidade (mínimo 3 AZs).
S3 Standard – Infrequent Access (S3 Standard-IA): Para dados acessados com pouca
frequência, mas que precisam de alta disponibilidade.
•
S3 One Zone-Infrequent Access (S3 One Zone – IA): Armazena dados em uma única AZ, ideal
para economizar custos onde os dados podem ser reproduzidos facilmente.
•
S3 Intelligent-Tiering: Monitora padrões de acesso e move objetos automaticamente entre os
níveis de acesso frequente e infrequente para otimizar custos.
•
S3 Glacier Instant Retrieval: Para dados arquivados que requerem acesso imediato
(milissegundos).
•
S3 Glacier Flexible Retrieval: Armazenamento de baixo custo para arquivamento de dados,
com recuperação em minutos a horas.
•
S3 Glacier Deep Archive: O menor custo de armazenamento para arquivamento de longo
prazo, com recuperação em 12 a 48 horas.
•
S3 Versioning: Permite manter múltiplas versões de um objeto em um único bucket,
preservando versões anteriores em caso de atualizações ou exclusões.
•
S3 Outposts: Cria buckets S3 em ambientes AWS Outposts on-premises, para dados que
precisam permanecer no local.
•
Amazon Elastic File System (Amazon EFS): Sistema de armazenamento de arquivos escalável
onde múltiplos clientes podem acessar os mesmos dados em pastas de arquivos
compartilhadas. É um serviço regional que armazena dados em múltiplas Zonas de
Disponibilidade.
•

Diferença EBS vs. EFS: EBS armazena dados em uma única Zona de Disponibilidade e precisa
estar na mesma AZ da instância EC2. EFS armazena dados em múltiplas Zonas de
Disponibilidade e é regional.
•

Bancos de Dados na AWS
Diversas opções para armazenar e gerenciar seus dados.
Bancos de Dados Relacionais (SQL): Usam SQL para armazenar e consultar dados em tabelas
com relações.
•
Amazon Relational Database Service (Amazon RDS): Serviço gerenciado para executar bancos
de dados relacionais populares (Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, SQL
Server). Automatiza tarefas como provisionamento, backups e patches.
•

Amazon Aurora: Banco de dados relacional de alto desempenho compatível com MySQL e
PostgreSQL, até 5x mais rápido que MySQL e 3x mais rápido que PostgreSQL. Replica 6 cópias
dos dados em 3 AZs.
•

Bancos de Dados Não Relacionais (NoSQL): Usam estruturas diferentes de linhas e colunas
(ex: chave-valor, documentos).
•
Amazon DynamoDB: Serviço de banco de dados de chave-valor e documento sem servidor,
oferecendo desempenho de milissegundos em qualquer escala.
•
• Amazon DocumentDB: Serviço de banco de dados de documentos compatível com MongoDB.
Amazon Neptune: Serviço de banco de dados de grafo para conjuntos de dados altamente
conectados (ex: mecanismos de recomendação, detecção de fraude).
•
Amazon Redshift: Serviço de data warehouse para análise de Big Data, coletando dados de
diversas fontes.
•
• Serviços de Cache:
Amazon ElastiCache: Serviço de cache em memória que melhora os tempos de leitura de
bancos de dados (suporta Redis e Memcached).
•
Amazon DynamoDB Accelerator (DAX): Cache em memória para o DynamoDB, melhorando
tempos de resposta de milissegundos para microssegundos.
•
• Serviços de Migração de Banco de Dados:
AWS Database Migration Service (AWS DMS): Permite migrar bancos de dados relacionais e
não relacionais, mantendo o banco de dados de origem operacional.
•
AWS Application Migration Service (MGN): Solução automatizada de "lift-and-shift" para
migrar servidores físicos, bancos de dados e aplicações para instâncias EC2.
•
Sistema de Mensagens e Enfileiramento

Página 41 de AWS CLOUD PRACTITIONER

Para construir aplicações distribuídas e desacopladas.
Aplicações Monolíticas: Componentes fortemente acoplados; a falha de um pode afetar todo
o sistema.
•
Microsserviços: Componentes fracamente acoplados; a falha de um não necessariamente
derruba o aplicativo.
•
• Serviços que facilitam a integração de aplicações:
Amazon Simple Notification Service (Amazon SNS): Serviço de publicação/assinatura, onde
um editor envia mensagens para múltiplos assinantes (ex: e-mails, funções Lambda).
•
Amazon Simple Queue Service (Amazon SQS): Serviço de enfileiramento de mensagens para
enviar, armazenar e receber mensagens entre componentes de software sem perda de dados.
•
Segurança, Identidade e Conformidade
Protegendo seus dados e recursos na nuvem.
Modelo de Responsabilidade Compartilhada da AWS: Define as responsabilidades de
segurança:
•
AWS (Segurança da nuvem): Responsável pela proteção da infraestrutura global (hardware,
software, rede, virtualização, segurança física dos datacenters).
•
Cliente (Segurança na nuvem): Responsável pela segurança de tudo que cria e coloca na
nuvem (seleção e configuração de sistemas operacionais, grupos de segurança, gerenciamento
de contas de usuário, dados).
•

AWS Identity and Access Management (IAM): Permite gerenciar o acesso a serviços e
recursos da AWS com segurança.
•
Usuário-raiz da conta AWS: Identidade inicial com acesso completo (use apenas para tarefas
de faturamento e configuração inicial).
•
• Usuários do IAM: Identidades para pessoas ou aplicações, com permissões específicas.
Grupos do IAM: Conjuntos de usuários do IAM; políticas anexadas ao grupo se aplicam a todos
os usuários nele.
•
Políticas do IAM: Documentos que concedem ou negam permissões a serviços e recursos
AWS.
•
Perfis do IAM: Identidades que você pode assumir para obter acesso temporário a
permissões.
•
• Autenticação Multifator (MFA): Camada extra de segurança para sua conta AWS.
• Gerenciamento de Contas e Conformidade:
• AWS Organizations: Consolida e gerencia múltiplas contas AWS em um local central.
Políticas de Controle de Serviço (SCPs): Permitem restringir serviços, recursos e ações de API
em contas e Unidades Organizacionais (UOs).
•
AWS Artifact: Concede acesso sob demanda a relatórios de segurança e conformidade da AWS
e a contratos online.
•
• Proteção Contra Ameaças:
• AWS Shield: Protege aplicações contra ataques DDoS (Negação de Serviço Distribuída).
• Standard: Proteção gratuita contra os ataques DDoS mais comuns.
Advanced: Serviço pago com diagnósticos detalhados e mitigação de ataques DDoS
sofisticados.
•
AWS WAF (Web Application Firewall): Firewall de aplicação web que monitora e controla
solicitações de rede para aplicações web, usando ACLs da web (listas de controle de acesso).
•
Amazon Inspector: Realiza avaliações de segurança automatizadas em aplicações para
identificar vulnerabilidades e desvios de práticas recomendadas (foca em vulnerabilidades na
infraestrutura).
•

Amazon GuardDuty: Serviço de detecção inteligente de ameaças que monitora
continuamente a atividade da rede e o comportamento da conta na AWS (foca em atividades
e comportamentos maliciosos).
•

AWS Key Management Service (AWS KMS): Permite executar operações de criptografia
usando chaves de criptografia.
•
• SSE-S3: Criptografia do lado do servidor com chaves gerenciadas pelo S3.
• SSE-KMS: Criptografia do lado do servidor usando AWS KMS para auditoria e controle.
• SSE-C: Criptografia do lado do servidor onde o cliente fornece as chaves.
Customer Managed Key (CMK): Uma chave gerada e gerenciada pelo cliente dentro do AWS
KMS.
•

Página 42 de AWS CLOUD PRACTITIONER

KMS.
AWS CloudHSM (Hardware Security Module): Fornece um dispositivo físico dedicado para
armazenar e proteger chaves criptográficas, oferecendo um nível mais alto de segurança de
hardware.
•

AWS Secrets Manager: Armazena e gerencia segredos (credenciais de banco de dados, chaves
de API) de forma segura e centralizada, com rotação automática.
•
Amazon Macie: Usa machine learning e IA para descobrir, classificar e proteger
automaticamente dados sensíveis em buckets S3.
•
AWS Security Hub: Agrega, organiza e prioriza alertas e descobertas de segurança de outros
serviços AWS (GuardDuty, Inspector, Macie) e parceiros.
•
Infraestrutura Global da AWS
A AWS opera em uma arquitetura global resiliente e escalável:
Regiões: Locais físicos geograficamente isolados com múltiplos datacenters. A escolha de uma
região considera conformidade, proximidade com clientes, serviços disponíveis e preços.
•
Zonas de Disponibilidade (AZs): Datacenters isolados dentro de uma Região, garantindo baixa
latência entre eles e resiliência a desastres.
•
Locais de Borda (Edge Locations): Sites usados pelo Amazon CloudFront (serviço de CDN -
Content Delivery Network) para armazenar cópias em cache de conteúdo, próximos aos
clientes para entrega mais rápida.
•

Gerenciamento, Monitoramento e Automação
Ferramentas para operar e otimizar seu ambiente AWS.
• Formas de Interagir com os Serviços AWS:
• Console de Gerenciamento da AWS: Interface web para acessar e gerenciar serviços.
AWS Console Mobile Application: Para monitoramento e tarefas rápidas em dispositivos
móveis.
•
AWS Command Line Interface (AWS CLI): Ferramenta de linha de comando para controlar
serviços AWS via scripts.
•
Kits de Desenvolvimento de Software (SDKs): Facilitam o uso de serviços AWS em diferentes
linguagens de programação.
•
AWS Elastic Beanstalk: Implanta automaticamente os recursos necessários para executar
código, ajustando capacidade, balanceando carga, fazendo auto scaling e monitorando a
saúde (PaaS - Platform as a Service).
•

AWS CloudFormation: Permite definir a infraestrutura como código (IaC), provisionando
recursos de forma segura e repetível.
•
• Amazon CloudWatch: Serviço web para monitorar e gerenciar métricas e configurar alarmes.
• Métricas: Pontos de dados para seus recursos.
Alarmes do CloudWatch: Executam ações automáticas quando as métricas ultrapassam
limites.
•
AWS CloudTrail: Registra as chamadas de API realizadas em sua conta, fornecendo um log de
ações para auditoria e governança.
•
• CloudTrail Insights: Detecta automaticamente atividades de API incomuns.
AWS Trusted Advisor: Inspeciona seu ambiente AWS e faz recomendações em tempo real com
base nas melhores práticas da AWS em cinco categorias: otimização de custos, desempenho,
segurança, tolerância a falhas e limites de serviço.
•

AWS Personal Health Dashboard: Fornece eventos recentes sobre a saúde dos serviços AWS
que afetam sua conta, ajudando a gerenciar eventos ativos e planejar atividades programadas.
•
AWS Config: Monitora e registra continuamente as alterações de configuração de seus
recursos da AWS, permitindo avaliar a conformidade.
•
AWS Compute Optimizer: Analisa a configuração e as métricas de utilização de seus recursos
AWS para recomendar otimizações de custos e desempenho.
•
AWS X-Ray: Permite analisar e depurar aplicações distribuídas, fornecendo visibilidade de
ponta a ponta do comportamento e desempenho.
•
AWS Cloud9: Ambiente de desenvolvimento integrado (IDE) baseado na nuvem que permite
escrever, executar e depurar código diretamente do navegador.
•
AWS Service Catalog: Permite que as organizações criem e gerenciem catálogos de serviços de
TI para uso na AWS, garantindo conformidade.
•

Página 43 de AWS CLOUD PRACTITIONER

TI para uso na AWS, garantindo conformidade.
Preço e Suporte
Entendendo os custos e as opções de ajuda.
Nível Gratuito da AWS: Permite usar determinados serviços gratuitamente por um período
específico (sempre gratuito, 12 meses gratuitos e versões de teste).
•
• Como funciona a definição de preço da AWS:
• Pague somente pelo que usar: Flexibilidade e economia.
• Pague menos ao fazer reserva: Descontos para uso contínuo (ex: Savings Plans).
Pague menos com descontos baseados em volume: Quanto mais você usa, menor o preço por
unidade.
•
• Calculadora de Preços da AWS: Permite estimar os custos de seus casos de uso na AWS.
• Gerenciamento de Custos e Faturamento:
Painel de Cobrança (Faturamento e Gerenciamento de Custos da AWS): Para pagar faturas,
monitorar uso e analisar custos.
•
Cobrança Consolidada: No AWS Organizations, permite uma única fatura para todas as contas
AWS de uma organização.
•
• AWS Budgets: Crie orçamentos para planejar uso e custos, e defina alertas personalizados.
AWS Cost Explorer: Ferramenta para visualizar, interpretar e gerenciar seus custos e uso da
AWS ao longo do tempo.
•
• Planos de Suporte da AWS:
Basic (Gratuito): Acesso limitado a verificações do Trusted Advisor, Personal Health
Dashboard, documentação e comunidades.
•
Desenvolvedor (Pago): Acesso a orientação de práticas recomendadas e ferramentas de
diagnóstico.
•
Empresarial (Pago): Todas as verificações do Trusted Advisor, suporte limitado para software
de terceiros e orientação.
•
Enterprise On-Ramp / Enterprise (Pagos): Acesso a Technical Account Managers (TAMs),
otimização de custos, e tempos de resposta rápidos para problemas críticos.
•
Technical Account Manager (TAM): Ponto de contato principal com a AWS para orientação
especializada.
•
AWS Concierge Support Team: Suporte especializado para clientes com infraestrutura ou
gastos significativos na AWS.
•
Migração para a Nuvem
Ferramentas e estratégias para mover suas cargas de trabalho.
AWS Migration Hub: Um local central para acompanhar o progresso das migrações de
aplicativos em várias soluções AWS e de parceiros.
•
AWS Cloud Adoption Framework (AWS CAF): Um plano estratégico e organizacional para a
jornada da sua empresa para a nuvem. Organiza orientações em seis perspectivas: Negócio,
Pessoas, Governança, Plataforma, Segurança e Operações.
•

• Estratégias de Migração (6 Rs):
• Rehost (Redefinir Hospedagem): Mover aplicações sem alterações (lift-and-shift).
Replatform (Redefinir Plataforma): Fazer otimizações na nuvem sem alterar a arquitetura
central (lift, tinker and shift).
•
Refactor (Refatoração/Rearquitetura): Reimaginando a arquitetura da aplicação usando
recursos nativos da nuvem.
•
• Repurchase (Recomprar): Mudar de uma licença tradicional para um modelo SaaS.
• Retain (Reter): Manter aplicações essenciais no ambiente de origem.
• Retire (Retirar): Remover aplicações que não são mais necessários.
AWS Snow Family: Coleção de dispositivos físicos para transportar grandes volumes de dados
para dentro e para fora da AWS.
•
AWS Snowcone: Dispositivo pequeno e robusto para transferência de dados e computação de
borda.
•
AWS Snowball Edge: Dispositivos para migrações de dados em larga escala e computação local
(Storage Optimized para capacidade, Compute Optimized para poder computacional).
•
AWS Snowmobile: Serviço de transferência de dados em escala de exabytes, usando um
contêiner de transporte puxado por caminhão.
•

Página 44 de AWS CLOUD PRACTITIONER

contêiner de transporte puxado por caminhão.
AWS DataSync: Serviço de transferência de dados projetado para mover grandes quantidades
de dados entre sistemas de armazenamento on-premise e serviços da AWS, com criptografia
em trânsito.
•

Inovação e Outros Serviços Relevantes
A AWS oferece muito mais do que infraestrutura básica:
• Machine Learning (ML) e Inteligência Artificial (IA):
• Amazon SageMaker: Para construir, treinar e implantar modelos de ML.
• Amazon Transcribe: Converte fala em texto.
• Amazon Comprehend: Descobre padrões e insights em texto.
• Amazon Fraud Detector: Identifica atividades online potencialmente fraudulentas.
• Amazon Lex: Cria chatbots de voz e texto.
• Amazon Polly: Converte texto em fala.
• Amazon Personalize: Cria recomendações individualizadas para clientes usando ML.
• Amazon Rekognition: Análise e detecção facial em imagens e vídeos.
• Streaming de Dados:
Amazon Kinesis: Plataforma para streaming de dados, facilitando o carregamento e análise de
dados em tempo real.
•
• Pesquisa e Análise:
• Amazon Kendra: Serviço de pesquisa inteligente baseado em machine learning.
Amazon Athena: Serviço de consulta interativo e sem servidor que facilita a análise de dados
no Amazon S3 usando SQL padrão.
•
AWS Glue: Serviço de ETL (Extração, Transformação e Carregamento) totalmente gerenciado
para preparar e carregar dados para análise.
•
Amazon EMR (Elastic MapReduce): Plataforma de big data na nuvem para processar grandes
quantidades de dados usando ferramentas de código aberto (Hadoop, Spark, etc.).
•
• Autenticação e Gerenciamento de Usuários:
Amazon Cognito: Serviço totalmente gerenciado que fornece autenticação, autorização e
gerenciamento de usuários para aplicativos web e móveis (suporta provedores de identidade
social).
•

• Desenvolvimento e DevOps:
AWS CodeCommit: Serviço de controle de versão totalmente gerenciado que hospeda
repositórios Git seguros.
•
AWS CodePipeline: Serviço de entrega contínua que automatiza pipelines de lançamento para
atualizações rápidas.
•
• Ambientes de Trabalho Virtual:
• Amazon WorkSpaces: Solução de infraestrutura de desktop virtual (VDI) baseada na nuvem.
• Gerenciamento de Conformidade:
AWS Audit Manager: Ajuda a automatizar o processo de avaliação, gerenciamento e geração
de relatórios sobre conformidade.
•
• AWS Compliance Center: Local central para pesquisar requisitos regulatórios.
• Outros Serviços:
Amazon Pinpoint: Serviço escalável para interagir com clientes via e-mail, SMS, notificações
push.
•
AWS Control Tower: Ajuda a configurar e controlar um ambiente seguro e com várias contas
da AWS, baseado nas melhores práticas.
•
AWS Managed Services (AMS): Ajuda empresas a operar sua infraestrutura da AWS com mais
eficiência e segurança.
•
AWS Quick Start Reference Deployments: Modelos automatizados do CloudFormation para
implantar e configurar soluções rapidamente.
•
AWS Marketplace: Catálogo digital com milhares de ofertas de software de provedores
independentes.
•
AWS Partner Network (APN): Programa global de parceiros da AWS para ajudar organizações
a construir negócios ou soluções baseados na AWS.
•
Otimização e Melhores Práticas
AWS Well-Architected Framework: Ajuda a projetar e operar sistemas confiáveis, seguros,
eficientes e econômicos na nuvem AWS, baseado em seis pilares:
•

Página 45 de AWS CLOUD PRACTITIONER

eficientes e econômicos na nuvem AWS, baseado em seis pilares:
• Excelência Operacional: Executar e monitorar sistemas, melhorando processos.
1. Segurança: Proteger informações e ativos.
2. Confiabilidade: Recuperar-se de interrupções, escalar dinamicamente.
3. Eficiência de Desempenho: Usar recursos computacionais de forma eficiente.
4. Otimização de Custos: Executar sistemas com o menor preço.
5. Sustentabilidade: Melhorar impactos ambientais, reduzindo o consumo de energia.
AWS Well-Architected Tool: Ajuda os clientes a revisar e melhorar suas cargas de trabalho
com base nas melhores práticas do Framework.
