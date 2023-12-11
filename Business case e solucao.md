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


