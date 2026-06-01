1. O que é Controle de Versão Distribuído?

Significa que você não depende de um servidor central para trabalhar. Quando você clona um projeto com o Git, o seu computador recebe uma cópia idêntica de todo o histórico dele. Dá para ver o passado do código e fazer alterações mesmo se você estiver sem internet.
 2. Git vs. GitHub

O Git é o programa que você instala na máquina para registrar o histórico e as alterações do código. O GitHub é a rede social dos programadores na nuvem, onde a gente joga o código para o resto da equipe ter acesso e trabalhar junta.

 3. O que é um Commit?

Pense no commit como um "salvamento" ou uma foto do seu código naquele exato momento. Ele gera um código único (chamado hash) e serve para deixar registrado quem mexeu, quando mexeu e o que foi feito.

4. Working Directory, Staging Area e Repository

Working Directory: É a pasta no seu computador onde você está abrindo e editando os arquivos agora.
Staging Area:É a sala de espera. Quando você usa o git add, o arquivo fica guardado ali, esperando para entrar no próximo commit.
Repository: É o cofre. Quando você faz o git commit, as alterações saem da sala de espera e entram oficialmente para o histórico do projeto.

5. O que é uma Branch?

É uma linha do tempo paralela. Em vez de todo mundo mexer no código principal ao mesmo tempo (o que daria um erro atrás do outro), cada um cria a sua própria ramificação para testar suas ideias sem estragar o que já está funcionando.

6. Merge vs. Rebase

Merge: Pega a sua linha do tempo e junta com a principal, criando um histórico que mostra exatamente quando os caminhos se cruzaram. É mais seguro para projetos em equipe.
Rebase:Pega os seus commits e "cola" eles direto no topo da linha principal, deixando o histórico em uma linha reta e limpa. A desvantagem é que ele apaga o rastro de como as coisas aconteceram cronologicamente.

7. Para que serve ogitignore?

Serve para dizer ao Git: "Não olhe para essa pasta". É indispensável para ignorar arquivos pesados (como a pasta `img/` do nosso trabalho) ou senhas e dados sensíveis que não podem ir para a internet de jeito nenhum.

 8. Git Push vs. Git Pull

Git Push: Pega os commits que você fez no seu computador e envia para o GitHub.
Git Pull:Traz as novidades que a sua equipe enviou para o GitHub direto para a sua máquina, atualizando seu código local.

 9. O que são Conflitos de Merge?

Acontecem quando duas pessoas alteram a mesma linha do mesmo arquivo e tentam juntar tudo. O Git fica confuso e avisa: "Não sei qual versão manter". Para resolver, um programador precisa abrir o arquivo, escolher a linha certa na mão, salvar e fazer um novo commit.

 10. Por que versionar o código?

Porque trabalhar em equipe sem isso é impossível. O versionamento traz rastreabilidade (para descobrir onde um bug começou), manutenção (para voltar atrás se tudo quebrar) e permite que várias pessoas mexam no mesmo projeto sem se atropelarem.

11. O que é um Pull Request (PR)?

É o famoso "dá uma olhada aqui". Quando você termina sua tarefa na sua branch, você abre um PR no GitHub para que o líder do projeto (ou sua equipe) revise as alterações antes de jogá-las na versão principal.

12. Recuperação e Auditoria no Git

Se alguém fizer besteira no código, comandos como git checkout ou git revert salvam a pátria, permitindo voltar para uma versão antiga que funcionava. Além disso, o git log mostra a ficha completa do projeto: quem alterou, o que alterou e a data de cada modificação.