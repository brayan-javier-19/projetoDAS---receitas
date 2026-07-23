# Relatório Final - Página Colaborativa de Receitas

## Integrantes do Grupo

- **Nome do projeto:** Página Colaborativa de Receitas
- **Repositório:** https://github.com/brayan-javier-19/projetoDAS---receitas

| Integrante | Utilizador GitHub | Contribuição principal |
|---|---|---|
| Brayan Gallardo | brayan-javier-19 | Criação do repositório, receita de bolo de laranja, lista de receitas |
| Bruno Xarez | BrunoXarez | Receita de bolo de maçã e canela |
| Daniel Tomé | Daniel-Tome123 | Receita de bolo de chocolate |
| Eduardo Valério | edvalerio2005-afk | Receita de bolo de iogurte |
| Idianete Borges | idianeteborges-ui | Receita de bolo de cenoura |

## Branches Criadas

O grupo adotou a convenção `feature/` seguida do nome da receita, com uma branch por tarefa, criadas a partir da branch principal. No total foram criadas 7 branches.

| Branch | Objetivo | Responsável |
|---|---|---|
| `main` | Branch principal, versão estável do projeto | — |
| `feature/bolo-de-laranja` | Adicionar a receita de bolo de laranja e a lista de receitas | brayan-javier-19 |
| `feature/bolo-de-cenoura` | Adicionar a receita de bolo de cenoura | idianeteborges-ui |
| `feature/bolo-de-chocolate` | Adicionar a receita de bolo de chocolate | Daniel-Tome123 |
| `feature/boloiogurte` | Adicionar a receita de bolo de iogurte | edvalerio2005-afk |
| `feature/bolo-maca-canela` | Adicionar a receita de bolo de maçã e canela | BrunoXarez |

Nenhuma alteração foi enviada diretamente para a branch principal. Todo o trabalho passou por uma branch própria e por Pull Request antes de ser integrado.

## Histórico de Commits

O grupo procurou escrever mensagens curtas e descritivas, que identificassem a alteração sem ser preciso abrir o ficheiro. Exemplos usados no projeto:

- `Adicionar receita de bolo de chocolate`
- `Preparacao do Bolo de Laranja`
- `Criacao da Lista de Receitas`
- `adicionar modo de preparação`
- `Add: receita de bolo de maca e canela`
- `Update: melhora formatacao da receita de bolo de maca e canela`

O gráfico de contribuições por integrante pode ser consultado no repositório em **Insights > Contributors**.

## Issues Criadas

Foram abertas 7 issues ao longo do projeto, todas concluídas e fechadas.

| Issue | Título | Responsável |
|---|---|---|
| #14 | Meter as receitas dentro do index.html | idianeteborges-ui |
| #11 | Relatório e ficheiro README | brayan-javier-19 |
| #9 | Renomear os ficheiros | brayan-javier-19 |

As issues serviram sobretudo para distribuir tarefas que não pertenciam a nenhuma receita em concreto, como a organização dos ficheiros e a preparação da página HTML principal. Cada uma foi fechada assim que o trabalho correspondente foi integrado na branch principal.

## Pull Requests

Foram abertos 6 Pull Requests ao longo do projeto, todos revistos e integrados na branch principal.

| PR | Título | Autor |
|---|---|---|
| #13 | Adição da receita de bolo de maçã e canela | BrunoXarez |
| #12 | Feature/boloiogurte | edvalerio2005-afk |
| #10 | Adicionar receita de bolo de chocolate | Daniel-Tome123 |
| #7 | receita-bolo-de-cenoura revisão | idianeteborges-ui |
| #6 | Adicionei a minha receita à lista principal | brayan-javier-19 |
| #4 | Bolo laranja | brayan-javier-19 |

O processo seguido foi sempre o mesmo: o autor abre o PR a partir da sua branch, descreve o que foi adicionado, e outro elemento do grupo revê antes do merge. O PR #13 é um exemplo de revisão explícita, com aprovação registada no GitHub antes da integração.

## Conflitos e Resoluções

Não houve conflitos de merge relevantes, porque cada integrante trabalhou num ficheiro próprio dentro de `src/`. A prática de correr `git pull` antes de começar cada alteração evitou a maior parte das situações de risco.

O ponto mais delicado foi a existência de duas branches principais no repositório, `main` e `master`, o que gerou confusão sobre para onde apontar os Pull Requests. Foi por causa disso, e da falta de uma convenção de nomes nos ficheiros, que se abriu a issue #9 para uniformizar a estrutura.

## Dificuldades Enfrentadas

A dificuldade mais concreta foi a autenticação no `git push`. O GitHub deixou de aceitar password no terminal e devolvia o erro *"Password authentication is not supported for Git operations"*. A solução foi gerar um Personal Access Token nas definições da conta, com o scope `repo`, e usá-lo no lugar da password.

Houve também alguma confusão inicial entre `git clone` e `git pull`. O `clone` só se usa uma vez, para trazer o repositório para o computador; o `pull` serve para atualizar uma cópia que já existe. Quem ainda não tinha o projeto localmente começou por tentar o `pull` e não percebia porque é que não funcionava.

Por fim, foi preciso perceber que editar um ficheiro diretamente pela interface do GitHub desatualiza a cópia local, e que sem um `git pull` a seguir o próximo `push` falha.

## Principais Comandos Git Utilizados

| Comando | Função |
|---|---|
| `git clone <url>` | Copia o repositório remoto para o computador local. Só é preciso na primeira vez |
| `git pull origin main` | Traz para local as alterações que os colegas já enviaram |
| `git checkout -b feature/nome` | Cria uma nova branch e muda para ela |
| `git status` | Mostra que ficheiros foram alterados e quais ainda não estão registados |
| `git add .` | Prepara todas as alterações para o próximo commit |
| `git commit -m "mensagem"` | Regista as alterações no histórico local |
| `git push -u origin feature/nome` | Envia a branch para o GitHub e liga-a ao remoto |
| `git config --global user.email` | Define o email da conta, para os commits ficarem associados ao autor correto |

## Conclusão

A atividade mostrou na prática o fluxo de trabalho usado em equipas de desenvolvimento: trabalhar numa branch isolada, submeter através de Pull Request e só integrar na branch principal depois de revisão. O valor deste processo tornou-se evidente quando cinco pessoas mexeram no mesmo projeto ao mesmo tempo sem se atropelarem.

Ficou também claro que a maior parte dos problemas não vem do Git em si, mas da falta de convenções combinadas à partida. A ausência de um padrão para os nomes dos ficheiros e a existência de duas branches principais deram mais trabalho do que qualquer comando, e obrigaram a abrir issues só para arrumar a casa. Da próxima vez, definir estas regras antes do primeiro commit pouparia tempo.

Do lado das ferramentas, o grupo consolidou o uso do Git pela linha de comandos e percebeu quando compensa usar a interface do GitHub: é prática para edições pequenas de texto, desde que se atualize a cópia local logo a seguir.
