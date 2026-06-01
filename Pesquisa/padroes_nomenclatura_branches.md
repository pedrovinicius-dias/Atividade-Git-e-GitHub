# Principais Nomenclaturas de Branches no Mundo

No desenvolvimento de software, a padronização dos nomes de branches é fundamental para manter o repositório organizado e facilitar o trabalho em equipe. O padrão mais adotado globalmente é inspirado no **Git Flow** e em metodologias ágeis.

Abaixo estão os prefixos e padrões de nomenclaturas mais utilizados:

## 1. Branches Principais (Permanentes)
* **`main`** ou **`master`**: É a branch principal e oficial. O código nela deve estar sempre estável e pronto para produção.
* **`develop`** ou **`dev`**: É a branch de integração. Todas as novas funcionalidades são mescladas (merged) nela antes de irem para a `main`. Representa o próximo estado de lançamento.

## 2. Branches de Suporte (Temporárias)

### Novas Funcionalidades (Features)
* **Prefixo:** `feature/` ou `feat/`
* **Uso:** Criada a partir da `develop` para desenvolver uma nova funcionalidade.
* **Exemplos:**
  * `feature/tela-de-login`
  * `feat/integracao-pagamento`
  * `feature/JIRA-123-novo-botao` (incluindo o ID da tarefa/ticket)

### Correção de Bugs (Bugfixes)
* **Prefixo:** `bugfix/` ou `fix/`
* **Uso:** Criada para corrigir bugs que não estão em produção (geralmente identificados durante testes na `develop` ou `release`).
* **Exemplos:**
  * `bugfix/erro-calculo-carrinho`
  * `fix/ajuste-layout-mobile`

### Correções Urgentes em Produção (Hotfixes)
* **Prefixo:** `hotfix/`
* **Uso:** Criada a partir da `main` para corrigir um problema crítico que já está no ambiente de produção. Após a correção, deve ser feito merge tanto na `main` quanto na `develop`.
* **Exemplos:**
  * `hotfix/falha-seguranca-api`
  * `hotfix/crash-ao-abrir-app`

### Lançamentos (Releases)
* **Prefixo:** `release/`
* **Uso:** Criada a partir da `develop` quando um conjunto de features está pronto para ir para produção. Usada para testes finais, correção de pequenos bugs e preparação de metadados antes de ir para a `main`.
* **Exemplos:**
  * `release/v1.2.0`
  * `release/fase-2`

### Outros Prefixos Comuns
* **`chore/`**: Manutenção geral, atualização de dependências, configurações que não afetam o código da aplicação diretamente (ex: `chore/atualizar-webpack`).
* **`docs/`**: Criação ou atualização de documentação (ex: `docs/atualizar-readme`).
* **`test/`**: Adição ou refatoração de testes automatizados (ex: `test/testes-unitarios-login`).
* **`refactor/`**: Refatoração de código que não adiciona novas funcionalidades nem corrige bugs (ex: `refactor/limpeza-codigo-antigo`).

## Boas Práticas Gerais
1. **Use letras minúsculas:** Evite letras maiúsculas para não causar conflitos em sistemas operacionais case-sensitive.
2. **Use hífens para separar palavras:** Em vez de espaços ou *camelCase*, use `-` (kebab-case) ou `/` para categorizar. (Ex: `feature/minha-nova-funcionalidade`).
3. **Seja descritivo e conciso:** O nome deve explicar rapidamente o propósito da branch.
4. **Use IDs de Tarefas:** Se a equipe usar ferramentas como Jira, Trello ou Azure DevOps, incluir o ID da tarefa no nome é uma ótima prática (Ex: `feature/T-405-adicionar-logs`).
