# 03 - Visão Geral AWS

## Infraestrutura Global

    Foi projetada e criada para oferecer um ambiente em nuvem **flexível**, **confiável**, **escalável** e **seguro**, com desempenho global de alta qualidade.
    
    Atualmente, existem 22 regiões (regions) da AWS espalhadas pelo mundo inteiro. Uma região é uma área geográfica física com uma ou mais zonas de disponibilidade (Availability Zone - AZ) que, por sua vez, consiste em um ou mais datacenters.
    
## Sobre as regiões

    Para estabilidade e tolerâncias a falhas, os recursos de cada região são isolados, de modo que esses recursos não são replicados automaticamente para outra. Cabe ao usuário replicar os dados entre regiões se necessário.
    
    Algumas regiões vem desabilitadas por padrão, o usuário deve, caso haja necessidade, habilitá-las via console de gerenciamento da AWS. Além disso, algumas regiões têm acesso restrito.
    
### Seleção de regiões

    Existem algumas questões importantes ao escolher a região que você irá subir os dados:
    - Gvernança de dados e os requisitos legais da região, afinal, os datacenters estão em países diferentes com leis e restrições diferentes.
    - A proximidade da região dos dados em relação as usuários finais, isso influência grandemente na latência das requisições. Você pode testar o tempo de resposta no site: https://www.cloudping.info/
    - A disponibilidade dos serviços em determinada região também é um fator a ser considerado.
    - E por último, e mais importante, os custos de tráfego de dados variam conforme a região. Isso se deve aos custos de manter a região naquele local do globo.
    
## Sobre as Availability Zones (AZ)

    Cada região têm, pelo menos, 3 zonas de disponibilidade, com cada zona sendo uma partição isolada da infraestrutura da AWS.
    As zonas são datacenters distintos, projetados para isolamento de falhas e interconectadas a outras zonas usando redes privadas de alta velocidade.
    O usuário pode escolher a zona de disponibilidade que os dados dele ficarão. Porém, a AWS recomenda que haja uma replicação de dados e recursos entre as zonas da região.
    
## Sobre os datacenters

    Eles são a base da estrutura da AWS, projetados para segurança, os clientes não especificam um datacenter para a implantação de um recurso, sendo uma AZ o nível mais granular de especificação disponível para os usuários.

### Segurança nos datacenters

    Contudo, um datacenter é o verdadeiro local onde os dados reais residem. Para evitar que haja perda de dados que afetem as aplicações dos clientes, a AWS faz backups dos dados em diferentes datacenters, além de monitorar o uso do serviço, a AWS disponibiliza suporte para casos de falhas. Os locais reais dos datacenters não são divulgados e há alta segurança no local com acesso restrito. Em caso de falha, a AWS move os dados para longe das áreas afetadas.
    
## Pontos de presença

    A AWS fornece **pontos de presença** que consitem em 176 pontos e 11 pontos de cache regionais.
    O CloudFront é uma rede de entrega de conteúdo usada para a distribuição de dados para usuários finais a fim de reduzir a latência.
    Já o Route 53 é um sistema de nome de domínio, um serviço de DNS, em que a solicitação enviada para um desses serviços será roteada automaticamente para o ponto de presença mais próximo, diminuindo a latência.
    Esses pontos de presença medem, continuamente, a conectividade, desempenho e computação com internet. Eles são usados internamente por diversos serviços da AWS: CloudFront, Route 53, AWS Shield, AWS Web Application Firewall.
    
## Benefícios da infraestrutura

    1. Elasticidade e Escalabilidade
        Os recursos podem se ajustar, aumentando ou diminuindo dinamicamente, os requisitos de capacidade.
    2. Tolerância a falhas
        Há uma redundância de componentes integrada na infraestrutura, permitindo a continuidade das operações mesmo que um componente se encontre com falha.
    3. Alta disponibilidade
        A AWS fornece um alto nível de disponibilidade com tempo inativo mínimo.
        
## Visão dos serviços e categorias

    AWS fornece um amplo conjunto de produtos globais na nuvem para uso como componente básico de arquiteturas de nuvem comuns.
    Os serviços fundamentais estão dispostas desta forma:
    - Infraestrutura: Regiões, AZs e pontos de presença.
    - Serviços base: Computação, Redes, Armazenamento.
    - Serviços de Plataforma: Bando de Dados, Análise, Serviços para Apps, Implementação e gerência, serviços mobile.
    - Aplicações: Desktops virtuais, colaboração e compartilhamento.
    
### Categorias

    Existem 23 categorias diferentes de produtos ou serviços e, cada categoria, consistem em um ou mais serviços.
    
#### Serviços mais usados

    **Armazenamento**
        - Amazon S3: Armazenamento mais comum, organização em buckets.
        - Amazon Elastic Block Store: armazenamento em bloco de alto desempenho projetado para uso com EC2.
        - Amazon Elastic File Sistem: Oferece sistemas de arquivos de rede escalável e gerenciado.
        - Amazon S3 Glacier: uma classe de armazenamento com foco em segurança, durabilidade e baixo custo para dados de backup.
        
    **Computação**
        - Amazon EC2: Fornece máquinas virtuais na nuvem
        - Amazon EC2 Auto Scaling: Permite que o usuário adicione ou remova instâncias automaticamente de acordo com a demanda de requisições.
        - Amazon ECS: Foco em alta escalabilidade e alta performance com suporte do Docker.
        - Amazon EC2 Container Registry: Registro de containers gerenciado do Docker, facilitando o armazenamento, gerenciamento e implantagem de imagens Docker.
        - AWS Elastic Beanstalk: Serviço de implantação/escalabilidade de aplicativos.
        - AWS Lambda: FaaS
        - Amazon Elastic Kubernetes Service: Simplifica a implantação/gerenciamento e escalabilidade de apps containerizados com Kubernetes.
        - AWS Fargate: Um macanismo de computação para o Amazon ECS, permitindo executar containers e gerenciar servidores/clusters.
        
    **Banco de dados**
        - Amazon RDS: Serviço de gerenciamento de banco de dados relacionais (postgres, sqlite, etc).
        - Amazon Aurora: Um banco de dados relacional compatível com Postgres e MySQL.
        - Amazon Redshift: permite execultar consutlas analíticas em petabytes.
        - Amazon DynamoDB: Um banco de dados NoSQL de documentos e chave-valor.
        
    **Rede AWS**
        - Amazon VPC: Provisiona seções da Nuvem AWS isoladas logicamente para a execução de recursos da AWS em rede definida pelo usuário.
        - Elastic Load Balancing: Distribui automaticamente o tráfego de entrada de aplicativos entre diversos destinos, como instâncias EC2, containers, endereços IP e Lambda function.
        - CloudFront: é uma rede de entrega de conteúdo, uma CDN.
        - AWS Transit Gateway: serviço de conexão entre clientes amazon e VPCs e redes locais com um único gateway centralizado.
        - Amazon Route 53: serviço web de sistema de nome de domínio em nuvem.
        - AWS Direct Connect: fornece formas de conexão de rede privada dedicada do datacenter ou escritório para a AWS.
        - AWS VPN: VPN da aws.
        
    **Segurança, Identidade e Conformidade**
        - IAM: serviço de gerenciamento de acesso os serviços ou recursos da AWS.
        - AWS Organizations: permite registrir quais serviços são permitidos nas contas, podendo ser criado grupos de contas.
        - Amazon Cognito: serviço de autenticação e controle de acesso de usuário aos aplicativos web e mobile.
        - AWS Artifact: oferece acesso sob demanda aos relatórios de segurança e conformidade da AWS e também à contratos on-line selecionados.
        - AWS Key Management: permite criar e gereciar chaves de criptografia.
        - AWS Shield: fornece proteção contra negação de serviço distribuida, protegendo aplicativos executados na AWS.
        
    **Gerenciamento de Custos**
        -  Custo da AWS e Relatório de uso
        - Orçamentos da AWS
        - Custo da AWS Explorer
        
    **Gerenciamento da AWS e Governança**
        - Console de Gerenciamento da AWS
        - AWS Config
        - Amazon CloudWatch
        - AWS Auto Scaling
        - CLI da AWS
        - AWS Trusted Advisor: Ajuda a aplicar boas práticas nos serviços da AWS
        - AWS Well-Architected Tool: Ajuda na revisão e melhorias de cargas de trabalho 
        - AWS CloudTrail: 
