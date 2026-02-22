# RELATORIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS
Data:22/02/2026
Empresa: Abstergo Industries
Responsável: Jorge Marley

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Jorge Marley. O objetivo do projeto foi de reduzir custos operacionais na infraestrutura em nuvem AWS, otimizar recursos computacionais e melhorar a eficiência no armazenamento e processamento de dados, com finalidade* realizar diminuição de custos imediatos.

## Descriçãop do Projeto
O projeto de implementação de ferramentas foi o divididos em 3 etapas, cada uma com seus objetivos especificos a seguir, serão descritas as etapas do projeto:Cenário atual (fictício)

A empresa possuía:

12 instâncias Amazon EC2 ligadas 24h

8 volumes Amazon EBS superdimensionados

15 TB de arquivos armazenados sem política de ciclo de vida no Amazon S3

💸 Custo mensal estimado: US$ 4.800

Etapa 1:
Ferramenta: AWS Compute Optimizer

Foco: Redução de custos com instâncias superdimensionadas

Caso de uso:
O Compute Optimizer analisou métricas de CPU, memória e rede das instâncias EC2 e identificou que:

7 instâncias estavam com uso médio de CPU abaixo de 15%

Recomendação: trocar de t3.large → t3.medium

💰 Economia estimada: US$ 1.200/mês

Etapa 2:
Ferramenta: Amazon S3 (Lifecycle + Glacier)

Foco: Redução de custos com armazenamento de arquivos antigos

Caso de uso:
Foi criada uma política:

Após 30 dias → mover para S3 Standard-IA

Após 90 dias → mover para S3 Glacier

Dos 15 TB:

9 TB eram arquivos antigos e raramente acessados

💰 Economia estimada: US$ 900/mês


Etapa 3:
Ferramenta: AWS Instance Scheduler

Foco: Desligar servidores fora do horário comercial

Caso de uso:

Instâncias de ambiente de desenvolvimento passaram a:

⏰ ligar às 08:00
⏰ desligar às 20:00

Antes: rodavam 24h
Depois: rodando apenas 12h/dia

💰 Economia estimada: US$ 700/mês

## Conclusão
A implementação das ferramentas AWS Compute Optimizer, políticas de ciclo de vida no Amazon S3 e o agendamento automático de instâncias EC2 proporcionaram redução significativa de custos, melhor utilização dos recursos e maior controle operacional.

Recomenda-se:

Monitoramento contínuo com Amazon CloudWatch

Adoção futura de AWS Auto Scaling para ajuste automático de capacidade

Revisões trimestrais de custos com AWS Cost Explorer
## Anexos
Planilha de custos antes/depois

Relatório do Compute Optimizer

Política de Lifecycle do S3

Cronograma de desligamento das instâncias

Assinatura do responsável pelo Projeto:
Jorge Marley
