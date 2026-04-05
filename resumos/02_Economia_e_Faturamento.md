# 02 - Economia e Faturamento

## Fudamentos da definição de preço

- Existem 3 fatores fundamentais:
    1. Computação: Cobrado por hora/segundo em que há variância pelo tipo da instância.
    2. Armazenamento: Cobrado, normalmente, por GB.
    3. Trânsferência de dados: A saída é agregada e cobrada, sem custo de entrada (há exceções) e normalmente cobrado por GB.
    
- Como é o pagamento na AWS?
    **1. Pague pelo que você usa.**
    **2. Pague menos ao fazer reserva.**
    **3. Pague menos quando você usar mais e conforme a AWS cresce.**
    
- Pague menos usando mais
    Alguns serviços na aws são estratificados, ou seja, serviços como o Amazon S3, quanto mais utilizar os GB, menos será o custo por GB.
    
- Questões sobre o Free tier
    O nível gratuito permite que você obtenha experiência prática gratuita com os produtos e os serviços da AWS. Gratuito por 1 ano para novos clientes.
    
- Serviços sem custo
    A AWS também oferece alguns serviços sem cobrança: VPC, Elastic Beanstalk, Auto Scaling, AWS CloudFormation, AWS IAM.
    Obs.: Pode haver cobrança associada a outros serviços utilizados por esses serviços.
    
## Custo total de propriedade

- Local x Nuvem
    Enquanto o local, existe um investimento inicial (como equipamento, otimização, segurança, etc) e fricção mental (contratos, adminitração, pessoas) demasiadamente grande, a utilização do serviços de nuvem da AWS permite que o cliente pague somente pelo que consumo (um custo inicial, muito menor), facilite a gestão (infraestrutura de  autoatendimento) e permitindo controlar a escala da empresa com mais facilidade.
    
- O que é o custo total de propriedade?
    O Custo total de propriedade (TCO) é a estimativa financeira para ajudar a identificar custos diretos e indiretos de um sistema. Serve para compactar os custos da execução de um **ambiente de infra inteiro** ou de uma determinada **carga de trabalho** no Local em comparação com AWS, o objetivo deve ser criar um orçamento e um caso de negócios para migrar para a nuvem.
    
## AWS Organizations
    
    É um serviço gratuito de gerenciamento de contas que permite consolidar várias contas da AWS em uma árvore organizacional com cada ramificação representando um departamento ou time.
    Além de poder centralizar os custos para o faturamento, você pode gerenciar as contas com base em políticas em grupo ou por conta. Contudo, ele não substitui o IAM que te dá o poder de controlar o acessos aos serviços da aws.
    
    Passo a passo:
    1. Criar organização
    2. Criar unidades organizacionais
    3. Criar políticas de controle de serviço
    4. Restrições de teste
    
Para acessar o AWS Organizations há 4 formas:
- Console de gereciamento
- CLI da Aws
- SDKs
- APIs

## AWS Billing and Cost Management

    É um serviço utilizado para pagar a fatura da AWS, monitorar o seu uso e controlar as depesas. Ele também permite prever e ter uma melhor noção de quais serão os custos e uso futuro. Na seção você pode utilizar algumas ferramentas:
    - Orçamento da AWS
    - Relatório de custos e uso da AWS
    - AWS Cost Explorer
    
## AWS Suport

    É fornecido para: experimentação com a AWS; uso da AWS na produção; processos de negócios crítivos que utilizam AWS.
    Para orientações proativas: TAM (gerente técnico de conta), eles são designados como o seu ponto de contato, fornecendo orientação, revisão da arquitetura e comunicação contínua. (Disponível somente no plano Enterprise)
    Para melhores práticas: AWS Trusted Advisor, atua como um especialista em nuvem personalizado, aponta erros e correções no que está fazendo com seus serviços.
    Para assistẽncia à conta: AWS Support Concierge, oferecendo análises de problemas de faturamento e conta.
    Existem 4 formas de suporte:
    1. Suporte básico: gratuíto e mais simples, porém limitado.
    2. Suporte ao desenvolvedor: possui acesso à orientação de melhores práticas e ferramentas de diagnóstico
    3. Suporte comercial: para clientes que executam cargas de trabalho de produção e é mais avançado nos recursos de suporte.
    4. Suporte empresarial: possui o acesso aos TAMs.
    
    Para suporte de casos, o plano utilizado tem uma relevância: o básico não possui suporte, o de desenvolvedor somente para casos de nível normal e baixo, o de comercial até casos altos e urgentes, e somente o enterprise possui suporte para o nível crítico.
