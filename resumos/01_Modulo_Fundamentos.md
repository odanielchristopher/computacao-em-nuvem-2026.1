# Módulo 01 - Fundamentos

## Básico

### O que é computação em nuvem?

    Entrega sob demanda de poder computacional, banco de dados, armazenamento e outros serviços via Internet com uma definição de preços conforme o uso.
    O Cloud permite que deixemos de pensar em infra como hardware e passemos a utilizá-la como um software.
    Além de um investimento inicial baixo, a sua flexibilidade e escalabilidade tornou o serviço de nuvem tentador.
    
### Modelos de Serviço em Nuvem

- IaaS: Infra como Serviço
    - São componentes básicos de TI em nuvem. Oferece acesso a recursos de rede, máquinas virtuais ou dedicadas, além de espaço de armazenamento. Te oferece um amplo controle sobre os recursos de TI.
- PaaS: Plataforma como Serviço
    - Elimina a forma de gerenciar diretamente a infraestrutura. Dá-lhe um controle por automação, permitindo o foco na implantação e gerenciamentos dos seus aplicativos do que nos recursos de hardware em si.
- SaaS: Software como Serviço
    - Refere-se ao app de usuários final. Sem se preocupar com infraestrutura e como ela é gerenciada, o usuário pode utilizar o sistema focando-se somente em como utilizar o item. Exemplos: Gmail, Instagram, etc.
    
### Modelos de Implantação

- Nuvem
    Aqui, todas as partes do sistema são implantadas usando Computação em Nuvem. Tanto o serviço em si, quanto a sua infraestrutura e gerenciamento é feito por meio da Nuvem.

- Híbrida
    Neste caso, parte do sistema é colocada na Nuvem, mas a sua infraestrutura e seus recursos estão localizados em instalações físicas. Conectando os serviços de Nuvem aos serviços internos da empresa.

- Local (nuvem privada)
    No geral, é parecida com a forma antiga de lidar com infraestrutura, mas mantendo uma conexão de Nuvem privada.
    
### AWS x TI tradicional

- Segurança
    - TI tradicional: Firewalls, ACLs , Administradores
    - AWS: Grupos de segurança, ACLs de Rede, IAM

- Redes
    - Tradicional: Roteador, Pipeline de rede, Switch
    - AWS: Elastic Load Balance, Amazon VPC
    
- Computação
    - Tradicional: Servidores locais
    - AWS: AMI -> Máquinas EC2s
    
- Armazenamento e DB
    - Tradicional: DAS, SAN, NAS, RDBMS
    - AWS: Amazon EBS, Amazon EFS, S3, Amazon RDS
    
## Vantagens da Nuvem

- 1° Despesas de Capital x Despesas Variáveis
    Ao utilizar datacenters comuns, o investimento é feito sob previsões de como o sistema pode funcionar. Por vezes, o investimento é maior ou menor do que realmente é de fato. Com a Nuvem, podemos pagar somente pelos recursos que foram utilizados e na medida em que foram utilizados.

- 2° Economia de escala: Com o uso da computação em nuvem, a AWS consegue ter uma grande economia de escala, resultando em descontos e menores preços nos serviços que a AWS oferece.

- 3° Sem adivinhação: Ao tentar adivinhar a capacidade que o servidor deve possuir, erros podem ocorrer e recursos podem ser desperdiçados ou o servidor não aguentar a demanda. Com a nuvem, a escalabilidade pode ser feito sob demanda.

- 4° Velocidade e agilidade: Para conseguir o acesso à novos recursos, basta somente alguns cliques.

- 5° Sem manutenção de Datacenters: A Nuvem permite que as empresas foquem nos investimentos com os clientes, ao invés de focar no provisionamento de recursos para as máquinas de infraestrutura (espaço, segurança, etc).

- 6° Alcance global: Hoje a nuvem está espalhada em todos o planeta praticamente. Com a utilização da Nuvem, a empresa consegue aumentar o alcance dos seus serviços a nível global em somente alguns minutos.

## AWS

### Maneiras de acesso à AWS

    Há 3 maneiras principais de acesso e comunicação com o ecossistema da AWS:
    - Console de Gerenciamento da AWS: Interface gráfica.
    - CLI: Acesso via comandos ou scripts pelo terminal.
    - SDKs: Acesso via clients diretamente do código (Java, JS, etc).

### Serviços

#### Serviços de Computação

- EC2
- Lambda
- Fargate
- Elastic Beanstalk
- ECS

####  Serviços de Armazenamento

- S3
- EFS
- EBS

#### Serviços de DB

- RDS
- DynamoDB
- Aurora
- Redshift

#### Serviços de Segurança

- IAM
- Cognito
- Shield
- Artifact
- KMS

#### Serviços de Rede

- VPX
- Route 53
- CloudFront

#### Serviços de Gerenciamento

- CloudWatch
- CloudTrail
- Console de gerenciamento da AWS
- AWS Config

## AWS CAF (Cloud Adoption Framework)

    É um guia de como as organizações podem ir migrando e adotando a utilização de recursos da AWS.
    Organizado em 6 perspectivas em que cada perspectiva consiste em alguns recursos.
    
1. Empresarial
    Stackholders: Gerentesde negócios e gerentesfinanceiros
    As partes interessadas devem garantir que as estratégias e metas de negócios de uma organização se alinhem às suas estratégias e objetivos de TI.
    
2. Pessoas
    Stackholders: Recursoshumanos, equipe e gerentes de pessoas.
    É necessário priorizar o treinamento, a equipe e as mudanças organizacionais para criar uma organização ágil.
    
3. Governança
    Stackholders: CIO, Analistas de negócio
    Énecessário garantir que as habilidades e os processos alinhem a estratégia e as metas de TI com a estratégia e as metas empresariais.
    
4. Plataforma:
    Stackholders: CTO, Gerentes de TI
    É necessário compreender e comunicar a natureza dos sistemas de TI e seus relacionamentos. Devemos ter a capacidade de descrever a arquitetura do ambiente do estado de destino em detalhes.
    
5. Segurança
    Stackholders: CISO, gerentes e analistas de segurança da TI.
    É necessário garantir que a organização atenda aos seus objetivos de segurança.
    
6. Operações
    Stackholders: Gerentes de operações e suporte de TI
    As partes interessadas da perspectiva de operações definem como as atividades diárias, trimestrais e anuais são realizadas.
