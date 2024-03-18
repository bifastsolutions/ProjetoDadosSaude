# Desafio

Uma empresa, líder na distribuição de material hospitalar, enfrenta um desafio crucial para
direcionar suas estratégias de vendas de forma eficiente em meio à pandemia de COVID-19.
A falta de dados precisos sobre casos, internações, mortes e a taxa de ocupação de hospitais em diferentes
regiões do Brasil tem impactado significativamente a capacidade da empresa de prever demandas e atender às necessidades de forma precisa e oportuna.

Atualmente, a empresa enfrenta dificuldades em entender a real demanda por material hospitalar em várias regiões do país, 
resultando em imprecisões na fabricação e distribuição. A falta de dados confiáveis sobre a situação da COVID-19
em diferentes estados prejudica a capacidade da empresa de responder eficazmente às necessidades dos hospitais e clínicas, levando a um suprimento inadequado ou excessivo em certas regiões.

# Quais a principais perguntas que devem ser respondidas (qual é a dor?)

## Indicadores

- Qual é o total de casos de Covid por estado?
- Qual é a taxa de ocupação  por estado e tipo de leito?
- Qual é a taxa de suspeitos e confirmados?
- Qual a quantidade e taxa de obitos de suspeitos e confirmados?
- Qual é a cidade e o estado mais e menos afetada?

## Benefícios(valor) esperado pelo cliente

- Serei capaz de tomar decisões mais rápidas e em tempo hábil?
  
  R: Sim, ao ter acesso a dados precisos e atualizados, você será capaz de tomar decisões mais rápidas e eficazes, permitindo uma resposta ágil às necessidades do mercado.
- Essa solução irá automatizar o processo evitando a intervenção humano para coletar, tratar e visualisar esses dados?
  
  R: Sim, essa solução foi projetada para automatizar o processo, eliminando a necessidade de intervenção humana na coleta, tratamento e visualização dos dados, garantindo eficiência e precisão.
- Os meus dados ficaram seguros e disponíveis com qualidade?
  
  R: Absolutamente, os dados serão protegidos, mantidos com qualidade e disponíveis para análise, proporcionando segurança e confiabilidade na tomada de decisões.
- Irei economizar em relação a custos com infraestrutura?
  
  R: Sim, ao automatizar o processo, você poderá economizar significativamente em custos de infraestrutura, reduzindo a dependência de recursos humanos e aumentando a eficiência operacional.
- Irei conseguir alcançar meus objetivos comerciais?
  
  R: Definitivamente, a solução visa aprimorar suas estratégias comerciais, oferecendo insights valiosos baseados em dados confiáveis para alcançar e superar seus objetivos de negócio.
- Essa solução irá me ajudar a melhorar a experiência do meu cliente?
  
  R: Sim, ao melhorar a precisão das decisões e estratégias, a solução contribuirá para aprimorar a experiência do cliente, atendendo melhor às necessidades do mercado e oferecendo um serviço mais alinhado e eficiente.


# Resumo Arquitetura e pipeline de dados

![Arquitetura Projeto Databricks - Saúde](https://github.com/bifastsolutions/ProjetoConcessionaria/assets/134235178/590a4afe-66c7-42fb-91bb-e9210339b6c1)

# Git e Gitlab

## Git

O git possui comandos que você usa para interagir com seus arquivos, é um sistema de controle de versão muito útil para acompanhar as mudanças em seus arquivos ao longo do tempo, ele mantém o controle das diferentes versões dos seus documentos, permitindo que você veja o que mudou, quando mudou e até mesmo voltar no tempo, se necessário.

Os principais comandos que utilizo nesse projeto são:

- git init: Este comando é usado para iniciar um repositório Git em um diretório. Ele cria um novo repositório Git ou transforma um diretório existente em um repositório Git.
- git add: Este comando adiciona arquivos ao "staging area", que é onde você prepara os arquivos para serem confirmados (ou "commitados") no Git.
  Por exemplo, se você alterou um arquivo chamado "script.py", você usaria git add script.py para adicionar essa mudança ao staging area.
- git commit: Este comando é usado para confirmar as mudanças feitas nos arquivos que estão no staging area. Cada commit cria um ponto na linha do tempo do seu projeto, permitindo que você acompanhe as alterações.
- git push: Quando você está trabalhando com um repositório remoto (como no GitHub, GitLab, etc.), o git push é usado para enviar suas alterações confirmadas para o repositório remoto.
- git branch: O Git permite que você trabalhe em diferentes "ramificações" do seu projeto. O git branch é usado para listar, criar ou excluir ramificações.
- git merge: Após trabalhar em ramificações separadas, o git merge é usado para combinar as alterações de uma ramificação em outra.
- git status: Este comando mostra o estado atual do seu repositório Git. Ele exibe informações sobre quais arquivos estão no staging area, quais foram modificados e ainda não foram adicionados, entre outros detalhes.
- git remote: Esse comando é como uma ponte entre o seu repositório local e um repositório remoto (como GitHub, GitLab, etc.). O repositório remoto é como uma versão online do seu projeto, onde você pode compartilhar seu 
  trabalho com outras pessoas.
- git checkout> Esse comando é como trocar de canal na TV. É uma forma de mudar para uma ramificação diferente do seu projeto, permitindo que você trabalhe em áreas separadas sem bagunçar uma com a outra.

   
  ![Funcionamento GIT e suas camadas](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/d4cfb18a-a018-4760-a918-d7fe7a6e21cd)


## Gitlab

O GitLab desempenha um papel crucial no gerenciamento de projetos de dados, oferecendo um repositório centralizado para controle de versionamento. Ele permite armazenar scripts essenciais, como os do Terraform para configuração na AWS e do Databricks para manipulação de dados. Com o GitLab, equipes podem colaborar, rastrear e revisar alterações de código, garantindo consistência e permitindo a implementação ágil de novas funcionalidades, mantendo um registro detalhado de todas as mudanças e facilitando a colaboração entre os membros do time.

![Gitlab](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/9039cbcd-38ca-4b72-bba9-a719fa6db14e)

Nesse projeto em específico foi utulizado o VS code para trabalhar com a criação de scripts em pyspark e terraform para ser utilizado dentro do projeto, após a construção do código através do Git,
os códigos eram enviados para uma branch Dev, enviados para o gitlab e após ter sua versão final era feito um merge para a branch de produção (como trabalho sozinho no projeto, 2 branchs foram suficientes
para a organização).

![Exemplo de comandos Git no projeto](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/fcfeeab0-7dfe-4f7b-a0f2-aedefe4aeb57)

# Terraform

![1-0XID8x0ak2xAqA3vt68BHg](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/b19f19a7-07b8-4ef1-8246-441e08bcd0a8)


O Terraform é uma ferramenta poderosa para orquestrar infraestrutura como código(IaC). Na AWS, ele será utilizado para automatizar a criação e gerenciamento de recursos, permitindo uma abordagem eficiente e consistente para provisionar serviços na nuvem. Estou usando ele para criar dois tipos de usuários na AWS: um que vai ter o controle como governança de dados, mexendo com várias coisas como IAM, SQS, SNS, criando e fazendo backup de buckets no S3, entre outras coisas. O outro usuário é mais limitado, só consegue ler os arquivos dos Buckets no S3 e executar containers específicos no ECS, onde usamos o Airflow e o Airbyte separados. Com isso,conseguimos ter um usuário para cada função não deixando acesso FULL para nenhum deles, usando um dos conceitos mais importantes em cloud do princípio do menor previlégio. E o terraform facilita esse controle de criação de serviços via código, onde eu não dependo da interface gráfica, podendo fazer manitenção de tudo que acontece na AWS de forma simples e prática por exemplo alterando, excluindo ou adicionando linhas no código.

## Principais Scripts terraform

#Irei listar apenas alguns códigos para que o projeto aqui não fique grande demais#

Todos os scripts utilizam 3 comandos básicos no terraform atravbés do vscode:

- Terraform init. Isso inicializa o Terraform e baixa os plugins necessários.
  
![WhatsApp Image 2023-12-18 at 19 57 49](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/6048613f-1505-471e-8c0a-0efaefc63606)

-  Terraform plan para verificar quais recursos serão criados, modificados ou removidos. (É opcional, mas interessante utilizar para ter certeza do que será executado, e você também será capaz de ver se os recursos
já existem na AWS e caso sejam alterações o codigo terraform informa essas modificações)

![WhatsApp Image 2023-12-18 at 19 59 51](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/2d3abee7-db73-40b1-bc7d-d8ecfbb73ecb)

- Terraform apply para aplicar as mudanças definidas no código Terraform.

![WhatsApp Image 2023-12-18 at 20 02 22](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/8b1863a8-3aca-4304-b7fa-abf1a650b77d)

!Importante: Para não haver conflitos entre os scripts terraform ao executar os comandos, como boas práticas é interessante separar os arquivos terraform em pastas, para que não haja tentativa do terraform de executar tudo novamente se estiver no mesmo diretório.


## Criação de usuário user_aws_governance

```terraform

provider "aws" {
  region = "us-east-1" 
}

resource "aws_iam_user" "user_aws_governance" {
  name = "user_aws_governance"
}

resource "aws_iam_policy" "policy_aws_governance" {
  name        = "policy_aws_governance"
  description = "Policy for AWS governance user"
  
  policy = jsonencode({
    Version = "2012-10-17",
    Statement = [
      {
        Effect   = "Allow",
        Action   = [
          "s3:CreateBucket",
          "s3:DeleteBucket",
          "s3:ListBucket",
          "s3:GetBucketLocation",
          "s3:GetBucketPolicy",
          "s3:GetObject",
          "s3:PutObject",
          "s3:DeleteObject",
          "s3:GetObjectVersion",
          "s3:PutObjectAcl"
        ],
        Resource = ["arn:aws:s3:::*", "arn:aws:s3:::*/*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "ecs:ListTasks",
          "ecs:DescribeTasks",
          "ecs:DescribeTaskDefinition",
          "ecs:DescribeContainerInstances",
          "ecs:RunTask",
          "ecs:DeleteTask"
        ],
        Resource = ["*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "sqs:ListQueues",
          "sqs:GetQueueAttributes",
          "sqs:ReceiveMessage",
          "sqs:CreateQueue",
          "sqs:DeleteQueue"
        ],
        Resource = ["*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "sns:ListTopics",
          "sns:GetTopicAttributes",
          "sns:Publish",
          "sns:CreateTopic",
          "sns:DeleteTopic"
        ],
        Resource = ["*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "logs:CreateLogGroup",
          "logs:CreateLogStream",
          "logs:PutLogEvents"
        ],
        Resource = ["arn:aws:logs:*:*:*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "lambda:ListFunctions",
          "lambda:GetFunction",
          "lambda:InvokeFunction",
          "lambda:CreateFunction",
          "lambda:DeleteFunction"
        ],
        Resource = ["*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "ce:GetCostAndUsage"
        ],
        Resource = ["*"]
      },
      {
        Effect   = "Allow",
        Action   = [
          "budgets:ViewBudget",
          "budgets:ModifyBudget"
        ],
        Resource = ["*"]
      }
    ]
  })
}

resource "aws_iam_user_policy_attachment" "attachment_aws_governance" {
  user       = aws_iam_user.user_aws_governance.name
  policy_arn = aws_iam_policy.policy_aws_governance.arn

}
```

### Detalhes

provider "aws" { region = "us-east-1" }: Esta linha define o provedor que o Terraform usará para interagir com a AWS, indicando a região onde os recursos serão criados.

resource "aws_iam_user" "user_aws_governance" { name = "user_aws_governance" }: Aqui, um recurso do tipo aws_iam_user é criado. Ele representa um usuário no IAM (Identity and Access Management) da AWS, com o nome "user_aws_governance".

resource "aws_iam_policy" "policy_aws_governance" { ... }: Este trecho define uma política no IAM chamada "policy_aws_governance". Essa política contém as permissões que serão associadas ao usuário criado anteriormente.

Dentro do bloco da política (policy = jsonencode({ ... })), cada seção Statement define uma permissão específica:

S3: Permite operações relacionadas aos Buckets do S3, como criação, exclusão, leitura e gravação de objetos. No caso, são permitidas ações em todos os Buckets (arn:aws:s3:::*) e seus objetos (arn:aws:s3:::*/*).

ECS: Concede permissões para listar, descrever, criar e excluir tarefas e containers no ECS.

SQS: Permite listar, obter atributos, receber mensagens, criar e excluir filas no SQS.

SNS: Fornece autorização para listar tópicos, obter atributos, publicar mensagens, criar e excluir tópicos no SNS.

Logs: Permite a criação de grupos de logs, streams de logs e a inserção de eventos de log.

Lambda: Concede permissões para listar, obter, invocar, criar e excluir funções do Lambda.

Cost Explorer e Budgets: Oferece permissões para visualizar e modificar orçamentos no AWS Budgets e acessar informações de custos no Cost Explorer.

resource "aws_iam_user_policy_attachment" "attachment_aws_governance" { ... }: Por fim, esta seção associa a política criada ao usuário previamente definido. Isso efetivamente concede ao usuário as permissões especificadas na política

![Usuario](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/382f581b-4d6c-43ad-b9b4-9110ee25c354)

![Politica](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/0912bc32-d984-4bf4-bf7b-a35a2130abc5)

![Permissões da política](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/4dfb9854-010b-41ee-8878-e72fc1f5e813)

## Criação dos buckets

```terraform

provider "aws" {
  region = "us-east-1"
}

# Bucket SAUDE_PROJECT_RAW
resource "aws_s3_bucket" "saude_project_raw" {
  bucket = "saude-project-raw"

  tags = {
    Name           = "SAUDE_PROJECT_RAW"
    SAUDE_PROJECT  = "true"
  }
}

resource "aws_s3_bucket_versioning" "saude_project_raw_versioning" {
  bucket = aws_s3_bucket.saude_project_raw.id

  versioning_configuration {
    status = "Enabled"
  }
}

# Bucket SAUDE_PROJECT_BRONZE
resource "aws_s3_bucket" "saude_project_bronze" {
  bucket = "saude-project-bronze"

  tags = {
    Name           = "SAUDE_PROJECT_BRONZE"
    SAUDE_PROJECT  = "true"
  }
}

resource "aws_s3_bucket_versioning" "saude_project_bronze_versioning" {
  bucket = aws_s3_bucket.saude_project_bronze.id

  versioning_configuration {
    status = "Enabled"
  }
}

# Bucket SAUDE_PROJECT_SILVER
resource "aws_s3_bucket" "saude_project_silver" {
  bucket = "saude-project-silver"

  tags = {
    Name           = "SAUDE_PROJECT_SILVER"
    SAUDE_PROJECT  = "true"
  }
}

resource "aws_s3_bucket_versioning" "saude_project_silver_versioning" {
  bucket = aws_s3_bucket.saude_project_silver.id

  versioning_configuration {
    status = "Enabled"
  }
}

# Bucket SAUDE_PROJECT_GOLD
resource "aws_s3_bucket" "saude_project_gold" {
  bucket = "saude-project-gold"

  tags = {
    Name           = "SAUDE_PROJECT_GOLD"
    SAUDE_PROJECT  = "true"
  }
}

resource "aws_s3_bucket_versioning" "saude_project_gold_versioning" {
  bucket = aws_s3_bucket.saude_project_gold.id

  versioning_configuration {
    status = "Enabled"
  }
}
```

![Criando os Buckets](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/b1576007-57af-4523-9dfb-872a94953611)


![Buckets Criados](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/d7e24874-c921-4cf3-91ed-9db61da9a3e2)


![Versionamento e Tags](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/b47ecd16-44fa-4804-be97-2c100fe88cd1)


Como podem observar os buckets forma criados todos ao mesmo tempo em segundos já com as configurações, também poderiam ter sido adicionadas lifecycle rules ou outras configurações da minha escolha, tudo via terraform.

## EC2 AWS

A princípio a intenção era utilizar o airbyte no serviço da AWS ECS que já é voltada para containers docker, mas devido a limitação do próprio Airbyte de acordo com a documentação deles o Airbyte até a data presente desse projeto dez.2023 a fev.2024 não era possível. Porém como solução com preço acessível utilizando também serviços da AWS, o airbyte será instalado em uma instancia EC2 com docker que terá sua programação de liga e desliga da instancia somente para o momento de utilização da mesma, economizando muito em comparação se a instancia ficasse ligada 24h por dia.

Para que possamos subir nossa instância EC2 com Airbyte com Terraform, alguns componentes precisam ser criados antes, pois fazem parte dos recuros do script terraform da instância.

### Chave PEM

A chave PEM (Privacy-Enhanced Mail) é usada como uma forma de autenticação para acessar uma instância EC2 na AWS. Ela funciona como uma espécie de "chave digital" que permite o acesso seguro à sua máquina virtual na nuvem. A chave possui criptografia e a conexão é feita via SSH. Para criarmos essa chave sem a necessidade de interação com o painel da AWS por meio de comandos, criaremos a chave através do CLI da AWS e teremos o resultado abaixo:

![Comandos para a criação da chave PEM](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/d6ae1bea-ae71-44a5-825d-e05f2368d97a)

A primeira linha de comando cria a chave chamada Airbyte_EC2 e o segundo comando garante que somente o usuário que criou a chave terá permissão de leitura.

![Chave criada](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/0fef0d03-88f2-4ca7-b726-84883d45b3ad)

Para mantermos a chave PEM e qualquer outra chave futura em segurança iremos utilizar o serviço da AWS chamada Secrets Manager, o AWS Secrets Manager é um serviço da Amazon Web Services (AWS) projetado para ajudar na gestão segura de informações sensíveis, como chaves de API, senhas, tokens e outras credenciais.

Sua principal vantagem reside na centralização e no gerenciamento seguro dessas informações sensíveis. Ele oferece:

Segurança Aprimorada: O Secrets Manager armazena suas credenciais de forma criptografada, ajudando a protegê-las contra acessos não autorizados.

Rotação Automática de Credenciais: Ele facilita a rotação regular e automática de credenciais, melhorando a segurança ao substituir automaticamente chaves e senhas antigas por novas.

Integração com Serviços AWS: Pode ser integrado de forma nativa com outros serviços AWS, como EC2, RDS, Lambda, entre outros, simplificando o gerenciamento de credenciais nessas plataformas.

Monitoramento e Auditoria: Oferece recursos para monitorar e registrar o acesso e o uso das credenciais, fornecendo trilhas de auditoria para garantir conformidade e segurança.

Para enviarmos nossa chave PEM para o Secrets Manager de forma gerenciável, também utilizaremos o Terraform conforme script abaixo

```terraform

provider "aws" {
  region = "us-east-1"  # Substitua com a região desejada
}

resource "aws_secretsmanager_secret" "key_secret" {
  name = "Airbyte_EC2"
}

resource "aws_secretsmanager_secret_version" "key_secret_version" {
  secret_id     = aws_secretsmanager_secret.key_secret.id
  secret_string = file("C:/Users/Raphael/Airbyte_EC2.pem")
}

```
Este script automatiza a criação de um segredo no AWS Secrets Manager chamado "Airbyte_EC2" e carrega uma versão desse segredo com o conteúdo do arquivo PEM fornecido,
que contem a chave de acesso para acessar a instância EC2 de maneira segura.

Além disso precisamos também criar um security group, s grupos de segurança (security groups) são uma parte fundamental da infraestrutura de segurança na Amazon Web Services (AWS) funcionam como um firewall. Eles desempenham um papel crucial na proteção das instâncias e recursos na nuvem, controlando o tráfego de entrada e saída para esses recursos. Para a criação desse também usaremos o terraform, no exemplo abaixo
deixamos o trafego livre ("0.0.0.0/0") para qualquer IP, porem como boas práticas defina exatamente quais IPs estarão autorizados a entrada e a saída.

```terraform

provider "aws" {
  region = "us-east-1"
  alias  = "security_group"
}
resource "aws_security_group" "airbyte_security_group" {
  name        = "airbyte"  # Substitua com o nome desejado para o grupo
  description = "security group sera utilizado na instancia do Airbyte com Docker"

  ingress {
    from_port   = 22   # Define a porta de origem para entrada (neste caso, porta 22)
    to_port     = 22   # Define a porta de destino para entrada (neste caso, porta 22)
    protocol    = "tcp"  # Define o protocolo (neste caso, TCP)
    cidr_blocks = ["0.0.0.0/0"]  # Permitir tráfego HTTP de qualquer lugar (altere para seu IP)
  }

  egress {
    from_port   = 0    # Define a porta de origem para saída (qualquer porta)
    to_port     = 0    # Define a porta de destino para saída (qualquer porta)
    protocol    = "-1"  # Define o protocolo para todos os protocolos (qualquer protocolo)
    cidr_blocks = ["0.0.0.0/0"]  # Permitir todo o tráfego de saída (altere para seu IP)
  }
}

```

Após a criação dos recursos necessários, podemos criar a nossa instância com o terraform

```terraform

provider "aws" {
  region = "us-east-1" # Substitua com a região desejada
  alias = "airbyte"  
}

resource "aws_instance" "ec2_instance" {
  ami           = "ami-00b8917ae86a424c9"  # Substitua com a AMI desejada
  instance_type = "t2.medium"  # Substitua com o tipo de instância desejado
  key_name      = "Airbyte_EC2"  # Substitua com o nome do seu keypair

  tags = {
    Name = "airbyte_saude_project"  # Substitua com o nome desejado (nome da instância)
  }

}

output "public_ip" {
  value = aws_instance.ec2_instance.public_ip
}

```


Após criar a instância e ela estar ativa para uso como na imagem abaixo, iremos realizar a instalação do docker e em seguida do Airbyte conforme a documentação oficial do Airbyte em https://docs.airbyte.com/deploying-airbyte/on-aws-ec2

![Instância em funcionamento](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/261a2d86-94ac-4168-aa5f-fa012040c849)

![Instalação Docker](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/bc3dbf66-9e4e-469e-a246-57d297191665)

![Instalação Airbyte](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/3ae48a8f-c803-41ec-ac80-7b807474c6ef)

![Airbyte start](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/9b984d90-9037-454e-805a-820750ca4e7f)

## Airbyte

![WhatsApp Image 2024-01-23 at 07 56 58](https://github.com/bifastsolutions/DatabricksAWS/assets/134235178/7252f6a6-65cd-4021-8013-06083af140ba)

Foram configuradas 3 conexões no airbyte

Google Drive(fonte) - AWS S3(Destino)
AWS RDS(fonte) - AWS S3(Destino)
API(Fonte) - AWS S3(Destino)




