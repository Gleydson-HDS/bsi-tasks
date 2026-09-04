# TAREFA 01 - CONCEITOS DE BD, ACID E SGBD
---
**Nome:** Gleydson Henrique Dantas da Silva  
**Github:** Gleydson-HDS  
---
**QUESTÃO 01 - Descreva o que é um Banco de Dados e o que é um Sistema Gerenciador de Banco de Dados. Cite exemplos de Bancos de Dados e seus SGBDs.**  
- Um Banco de Dados representa um sistema organizado para armazenar, gerenciar e recuperar dados de um progama. Um exemplo é o Banco de Dados de uma escola, que pode armazenar informações sobre alunos, professores, funcionários, disciplinas, etc. O SGBD (Sistema de Gerenciamento de Banco de Dados) representam os softwares que irão realizar a manipulação dessas informações, como por exemplo o PostgreSQL e o Oracle.
---
**QUESTÃO 02 - Quais os principais problemas de utilizar Sistemas de Arquivos para armazenagem de dados?**  
- Um dos principais problemas em utilizar Sistemas de Arquivos para o armazenamento de dados está na sua ineficiência de busca, sua falta de integridade, dificuldade de acesso, falta de segurança, redundância de dados e dificuldade de compartilhamento e recuperação dos mesmos. 
---
**QUESTÃO 03 - Explique as propriedades ACID: atomicidade, consistência, isolamento e durabilidade. Para cada propriedade, descreva um exemplo prático no contexto de uma transferência bancária e explique o que aconteceria se o SGBD não garantisse essa propriedade.**  

- Atomicidade: Transações são executadas totalmente ou desfeitas, como um conjunto. Em uma transferência bancária o valor debitado da conta de origem deve ser creditado na conta destino, ocorrendo a transferência de uma para a outra. Se essa propriedade não fosse garantida, o dinheiro poderia ser retirado da primeira conta sem chegar à segunda.
  
- Consistência: Mudança para um estado válido, íntegro, após a realização de uma transição. Após uma transferência, ambos os saldos da conta de origem e de destino devem ser atualizados. Se duas transferências forem realizadas ao mesmo tempo, o SGBD deve garantir que cada operação seja processada corretamente sem interferir na outra. Sem essa propriedade, os saldos poderiam ficar incorretos.

- Isolamento: Transações são tratadas de forma independente, de forma que não haja conflitos por concorrência. Se duas transferências forem realizadas ao mesmo tempo, o SGBD deve garantir que cada operação seja processada corretamente sem interferir na outra. Sem isolamento, uma transferência poderia utilizar um saldo desatualizado e causar erros.

- Durabilidade: Transações que já persistiram na base não serão desfeitas por erros futuros. Depois que uma transferência for confirmada, ela deve continuar registrada no banco de dados mesmo após uma falha ou queda de energia. Sem essa propriedade, a transferência poderia ser perdida mesmo tendo sido confirmada.
---
