# GIT + GITHUB CHEAT SHEET

Este documento foi gerado com base na imagem de referência, contendo os principais comandos e padrões para o uso do Git e GitHub.

## BRANCH
* `git branch new-branch`: Cria com o nome new-branch.
* `git checkout -b new-branch`: Criar e mudar o código para o branch new-branch.
* `git checkout new-branch`: Muda o código atual e a referência para a branch new-branch.
* `git checkout main`: Muda o código para a branch principal: main.
* `git branch -d new-branch`: Deleta a new-branch.
* `git branch`: Lista os branchs criados.
* `git branch -v`: Listar os branches criados com os logs de commit.
* `git push origin new-branch`: Criando um branch remoto com o mesmo nome.
* `git push origin new-branch:new-branch`: Criando um branch remoto com nome diferente.
* `git pull origin main`: Download de todos os os arquivos do repositório remoto para o local.
* `git fetch origin`: Download de todas as branchs remotas.
* `git checkout -b new-branch origin/new-branch`: Baixar um branch remoto para edição.
* `git merge new-branch`: Realiza o merge entre os branchs, ou seja, junta o ramo na árvore principal.

## STASH
* `git stash`: Cria um stash, salva temporariamente as modificações.
* `git stash list`: Lista os stashes criados.
* `git stash apply`: Volta ao último stash.
* `git stash apply stash@{2}`: Volta ao stash com índice 2.
* `git stash branch meu_branch`: Criar um branch a partir de um stash.

## GITHUB
* `git --version`: Verifica a versão instalada.
* `git config --global user.name "Seu Nome"`: Configura seu nome.
* `git config --global user.email "Seu Email"`: Configura seu e-mail.
* `git remote add origin git@github.com:"Usuário_github"/"repositorio"`: Envie o arquivo ao repositório remoto.
* `git remote -v`: Verifica os arquivos enviados.
* `git remote add origin https://github.com/nome/repositorio.git`: Sincroniza o repositório local com o remoto.

## INICIANDO UM REPOSITÓRIO
* `git init`: Inicia um repositório local.
* `git clone ssh://git@github.com/[username]/[repository-name].git`: Cria uma cópia do repositório local.

## LOG
* `git log`: Exibe histórico dos ultimos commits.
* `git log -p -3`: Exibe histórico com diff dos ultimos 3 commits.
* `git log --<caminho_do_arquivo>`: Exibir histórico no caminho_do_arquivo.
* `git log --pretty=oneline`: Exibe histórico de commits com informações resumidas em uma linha.
* `git log --diff-filter=M -- <caminho_do_arquivo>`: Exibe histórico de modificações de um arquivo.
* `git log --author=usuario`: Exibir histórico de um determinado autor.

## CHERRY-PICK
* `git cherry-pick <commit-id>`: Copia as informações desse commit.
* `git cherry-pick A^..B`: Copia todos os commits entre o commit A e o commit B, inclusive A e B.
* `git cherry-pick A..B`: Copia todos os commits entre o commit A e o commit B, excluindo A.

## ARQUIVOS (ADICIONAR, REMOVER E COMMIT)

### ADICIONAR
* `git add .`: Adiciona todos os arquivos ou diretórios modificados.
* `git add meu_programa.py`: Adiciona somente o arquivo meu_programa.py.
* `git add meu_diretorio`: Adiciona somente o diretorio meu_diretorio.
* `git add -f meu_programa_gitignore.py`: Adiciona um arquivo que está no .gitignore.

### REMOVER
* `git rm meu_arquivo.txt`: Remover arquivo.
* `git rm -r diretorio`: Remover diretório.

### COMMIT
* `git commit meu_programa.py`: Comitar um arquivo.
* `git commit file1.txt file2.txt`: Comitar vários arquivos.
* `git commit meuarquivo.txt -m "minha mensagem de commit"`: Comitar informando mensagem.

## MUDANÇAS
* `gitk`: Mostra as modificações totais do projeto.
* `git diff`: Modificações antes de enviar as modificações para o repositório remoto (commit).
* `git status`: Estado dos arquivos/diretório.
* `git commit --amend -m "Minha nova mensagem"`: Alterando mensagens de commit já realizado.
* `git rebase -i HEAD~3`: Alterar últimos commits, modificando as mensagens.
