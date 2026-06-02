# GIT + GITHUB CHEAT SHEET

## 🌲 BRANCH
Comandos para gerenciar ramificações de código.

* `git branch`: Lista as branches locais criadas.
* `git branch -v`: Lista as branches locais exibindo o último commit de cada uma.
* `git branch new-branch`: Cria uma nova branch chamada `new-branch` (sem mudar para ela).
* `git checkout new-branch`: Alterna para a branch `new-branch`.
* `git checkout -b new-branch`: Cria e alterna imediatamente para a `new-branch`.
* `git checkout main`: Alterna para a branch principal (`main`).
* `git branch -d new-branch`: Deleta a branch `new-branch` (apenas se ela já tiver passado por um merge).
* `git push origin new-branch`: Envia a branch local para o repositório remoto com o mesmo nome.
* `git push origin new-branch:outra-branch`: Envia a branch local para o repositório remoto com um nome diferente.
* `git fetch origin`: Baixa o histórico e as branches do repositório remoto (sem aplicar alterações no seu código atual).
* `git pull origin main`: Baixa as novidades da branch remota e já aplica o merge na sua branch local atual.
* `git checkout -b new-branch origin/new-branch`: Cria uma branch local baseada em uma branch remota específica.
* `git merge new-branch`: Junta o histórico de alterações da `new-branch` na branch em que você está atualmente.

<p align="center">
  <img width="290" height="422" alt="Diagrama de Branches" src="https://github.com/user-attachments/assets/5086cc16-2ad7-4775-a3ac-5250a12e2afa" />
</p>

---

## 📦 STASH
Área de armazenamento temporário para quando você precisa mudar de contexto sem dar commit em códigos incompletos.

* `git stash`: Salva temporariamente na pilha as modificações atuais do seu diretório de trabalho.
* `git stash list`: Exibe a lista com todos os stashes criados.
* `git stash apply`: Reaplica o stash mais recente sem removê-lo da lista.
* `git stash apply stash@{2}`: Reaplica um stash específico utilizando o seu índice.
* `git stash branch meu_branch`: Cria uma nova branch a partir do estado salvo em um stash.

<p align="center">
  <img width="288" height="178" alt="Fluxo do Stash" src="https://github.com/user-attachments/assets/f0f6c713-0b82-4e03-9a47-10fb2ab98d2d" />
</p>

---

## ⚙️ CONFIGURAÇÃO E CONFIGURAÇÃO REMOTA
Comandos globais e configurações de servidores remotos.

* `git --version`: Verifica a versão do Git instalada na máquina.
* `git config --global user.name "Seu Nome"`: Configura o nome que assinará seus commits.
* `git config --global user.email "seu_email@provedor.com"`: Configura o e-mail que assinará seus commits.
* `git remote add origin https://github.com/nome/repositorio.git`: Vincula o seu repositório local ao endereço do repositório remoto (via HTTPS).
* `git remote add origin git@github.com:usuario/repositorio.git`: Vincula o seu repositório local ao endereço remoto (via SSH).
* `git remote -v`: Lista as conexões com os servidores remotos configurados.

---

## 🚀 INICIANDO UM REPOSITÓRIO
Como começar um projeto com controle de versão.

* `git init`: Inicializa um novo repositório Git local na pasta atual.
* `git clone ssh://git@github.com/[username]/[repository-name].git`: Clona um repositório existente para a sua máquina local via SSH.

<p align="center">
  <img width="290" height="315" alt="Iniciando Repositorio" src="https://github.com/user-attachments/assets/a72095cc-7544-40fd-91cb-e782cac0b4aa" />
</p>

---

## 📜 LOGS E HISTÓRICO
Navegação pelos commits passados do projeto.

* `git log`: Exibe o histórico cronológico dos commits efetuados.
* `git log -p -3`: Exibe as alterações de código detalhadas (*diff*) dos últimos 3 commits.
* `git log -- <caminho_do_arquivo>`: Exibe o histórico de commits que afetaram apenas o arquivo especificado.
* `git log --pretty=oneline`: Exibe o histórico de forma compacta (um commit por linha).
* `git log --diff-filter=M -- <caminho_do_arquivo>`: Filtra o histórico para exibir apenas quando o arquivo foi modificado.
* `git log --author="Nome do Autor"`: Filtra e exibe os commits feitos por um autor específico.

<p align="center">
  <img width="274" height="195" alt="Visualização de Logs" src="https://github.com/user-attachments/assets/5ae930a0-ec4b-4a6b-b708-e7cd302c4b5e" />
</p>

---

## 🍒 CHERRY-PICK
Cópia cirúrgica de commits entre ramificações.

* `git cherry-pick <commit-id>`: Copia as alterações de um commit específico de outra branch e as aplica na sua branch atual.
* `git cherry-pick A^..B`: Copia um intervalo de commits do commit A até o commit B (incluindo o commit A).
* `git cherry-pick A..B`: Copia o intervalo de commits de A até B (excluindo o commit A).

<p align="center">
  <img width="274" height="152" alt="Cherry Pick" src="https://github.com/user-attachments/assets/38bd9a7d-02a4-4c62-82e2-55b20b2509b8" />
</p>

---

## 📁 MANIPULAÇÃO DE ARQUIVOS
Preparação, remoção e salvamento de arquivos no histórico.

### Adicionar (Staging Area)
* `git add .`: Adiciona todas as modificações atuais do diretório ao próximo commit.
* `git add meu_programa.py`: Prepara apenas o arquivo especificado.
* `git add meu_diretorio/`: Prepara todos os arquivos dentro do diretório especificado.
* `git add -f meu_arquivo_no_gitignore.py`: Força a adição de um arquivo que está listado no `.gitignore`.

### Remover
* `git rm meu_arquivo.txt`: Remove o arquivo do disco local e o prepara para a remoção no próximo commit.
* `git rm -r diretorio/`: Remove um diretório inteiro do disco e o prepara para remoção.

### Commitar (Salvar)
* `git commit meu_programa.py`: Abre o editor de texto padrão para criar um commit apenas com o arquivo especificado.
* `git commit file1.txt file2.txt`: Comita múltiplos arquivos selecionados de uma só vez.
* `git commit -m "Mensagem do commit"`: Cria o commit com todo o conteúdo que estava no *stage* usando a mensagem definida.

---

## 🔄 DIAGNÓSTICO E MUDANÇAS
Análise do estado atual e edições de commits antigos.

* `git status`: Mostra o estado atual das suas modificações (arquivos não rastreados, modificados ou na *staging area*).
* `git diff`: Exibe as alterações no código que ainda não foram enviadas para a *staging area*.
* `gitk`: Abre uma interface gráfica nativa do Git para visualização do histórico e modificações.
* `git commit --amend -m "Nova mensagem"`: Altera a mensagem do último commit realizado (caso ainda não tenha sido feito o push).
* `git rebase -i HEAD~3`: Abre o modo interativo para editar, agrupar ou alterar as mensagens dos últimos 3 commits.

<p align="center">
  <img width="228" height="370" alt="Fluxos de Mudanças" src="https://github.com/user-attachments/assets/1a03a21d-5528-4484-b607-33d299d1dd34" />
</p>
