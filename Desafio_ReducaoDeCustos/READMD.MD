# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

*Data:* 27/11/2025  
*Empresa:* Abstergo Industries  
*Responsável:* Gustavo Henrique Pich Carvalho

## Introdução
O projeto de implementação de serviços AWS *será estruturado* em três frentes estratégicas, com foco em reduzir custos e complexidade em um sistema de vendas: otimização da performance das APIs, gestão de identidades e entrega de conteúdo aos clientes.

---

## Etapa 1: Migração de APIs para Serverless
*Ferramenta Chave:* AWS Lambda  
*Descrição de Caso de Uso:* Faríamos a migração de APIs transacionais para o modelo serverless. O foco *será* implementar o AWS Lambda para as funcionalidades de backend mais críticas e com variação de demanda do sistema de vendas, como a criação de pedidos, atualização de estoque e cálculo de frete. Esta ação *visará* reduzir custos e aumentar a escalabilidade, adotando o modelo *Pay-per-Execution*.

---

## Etapa 2: Gerenciamento de Identidade com Cognito
*Ferramenta Chave:* Amazon Cognito  
*Descrição de Caso de Uso:* Terceirização da autenticação de clientes, implementando o Amazon Cognito como espinha dorsal para todo o gerenciamento de identidade do sistema de vendas. Isso *permitirá* que o cadastro, login e emissão de tokens de acesso *sejam* gerenciados de forma segura e escalável, sem necessidade de manutenção própria da infraestrutura de identidade.

---

## Etapa 3: Hospedagem e Distribuição de Frontend Estático
*Ferramenta Chave:* Amazon S3  
*Descrição de Caso de Uso:* O código do frontend (HTML, CSS, JavaScript) e as imagens de alta resolução dos produtos *serão movidos* para o *Amazon S3, que **proporcionará* o menor custo de armazenamento estático da AWS. A distribuição de conteúdo *será otimizada* usando o *CloudFront*, garantindo baixa latência e alta disponibilidade globalmente.

*Impacto no Custo:* O uso combinado do S3 e CloudFront *proporcionará* armazenamento de baixo custo e entrega eficiente de conteúdo estático.

---

## Conclusão
A implementação das ferramentas na empresa *Abstergo Industries* *trará* os benefícios esperados: redução de custos operacionais, aumento da escalabilidade das APIs, maior segurança e eficiência no gerenciamento de identidades, e entrega de conteúdo mais rápida e confiável aos clientes. Esses avanços *contribuirão* diretamente para o aumento da eficiência e produtividade da empresa. *Recomendar-se-á* a continuidade do uso das ferramentas implementadas, bem como a avaliação constante de novas tecnologias que *possam* otimizar ainda mais os processos e a experiência dos clientes.

## Anexos:
* [Arquitetura Proposta AWS](Arquitetura.png)
* [Estimativa de Custos AWS](Estimativa.pdf)
