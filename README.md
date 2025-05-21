# NextApprover - Projeto Power Apps

## Visão Geral

O **NextApprover** é um aplicativo desenvolvido no Power Apps para facilitar a revisão e correção de dados inconsistentes dos aprovadores de sistemas em uma organização. O app integra dados do **Dataverse** e do **SharePoint List (CheckInative)** para identificar usuários com e-mails inválidos ou desatualizados e permitir atualizações diretamente pelo aplicativo.

---

## Funcionalidades Principais

- Listar projetos com aprovadores que possuem e-mails inconsistentes.
- Mostrar detalhes dos aprovadores por projeto.
- Indicar visualmente (com cores e ícones) os e-mails considerados inválidos/inativos.
- Permitir a atualização dos dados dos aprovadores no Dataverse.
- Sincronizar e armazenar registros de e-mails inválidos no SharePoint List.
- Integração com Power Automate para processos automatizados (ex: validação de usuários).

---

## Estrutura do Aplicativo

- **srcAllApplication**: Tela inicial com listagem de projetos com inconsistências.
- **srcAllApplication_1**: Tela com detalhes dos aprovadores de um projeto selecionado.
- **scrCorrecao**: Tela para atualização dos dados dos aprovadores.
- **Galerias**: Utilizam dados do Dataverse e SharePoint para exibição e filtro.
- **Variáveis de contexto e globais**: Controle da navegação e dados selecionados (`varProjetoSelecionado`).

---

## Tecnologias e Serviços Utilizados

- Power Apps (Canvas App)
- Dataverse (tabela `AprovaçõeSistemicas` e outras)
- SharePoint List (`CheckInative`) para armazenamento de e-mails com erros
- Power Automate para automação de processos
- Conector Office365 Users para validação de e-mails

---

## Instruções para Uso

1. **Abrir o app** e visualizar a lista de projetos com problemas.
2. **Selecionar um projeto** para ver os aprovadores envolvidos.
3. **Visualizar quais e-mails estão inativos** (destacados em vermelho).
4. **Atualizar os e-mails inválidos** nos campos de texto apropriados.
5. **Salvar as alterações** usando o botão “Atualizar no Dataverse”.
6. O app atualiza os dados no Dataverse e sincroniza o registro na lista SharePoint se houver erro.

---

## Permissões Necessárias

- Usuário precisa de licença Power Apps com acesso ao Dataverse.
- Permissões de leitura/escrita nas tabelas do Dataverse envolvidas.
- Acesso à lista SharePoint `CheckInative`.
- Permissões para executar fluxos no Power Automate.

---

## Como Versionar o Projeto

- Exporte o arquivo `.msapp` do Power Apps e armazene no repositório GitHub.
- Para times com DevOps, utilize Power Platform CLI para controle detalhado do código.

---

## Contato

Para dúvidas e suporte, entre em contato com a equipe de desenvolvimento.

---

*Projeto desenvolvido por Gustavo para empresa Prysmian.*

