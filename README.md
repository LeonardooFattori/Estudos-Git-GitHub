# Repositório contendo meus estudos sobre Git e GitHub

Este repositório contém uma coletânea de perguntas e respostas sobre Git e GitHub, com o objetivo de aprofundar meu conhecimento sobre controle de versão e gerenciamento de repositórios.

## Perguntas e Respostas

### 1) O que são sistemas de controle de versão e quais são suas vantagens?
**Resposta:** Sistemas de controle de versão armazenam códigos de um projeto, permitindo o versionamento ao longo das atualizações. Vantagens incluem:
- Permitir a navegação por todas as versões anteriores.
- Facilitar o trabalho em equipe.

### 2) Tipos de sistemas de controle de versão e suas vantagens/desvantagens:
- **Controle de Versão Centralizado:** Simples de gerenciar, mas depende de um servidor.
- **Controle de Versão Distribuído:** Permite trabalho offline, mas pode ser complexo inicialmente.

### 3) Diferença entre Git e GitHub:
- **Git:** Sistema de controle de versão local.
- **GitHub:** Plataforma online para hospedar repositórios Git.

### 4) Diferença entre `git init` e `git clone`:
- **git init:** Cria um novo repositório vazio.
- **git clone:** Faz uma cópia de um repositório existente.

### 5) Principais áreas do Git:
- **Diretório de trabalho:** Manipulado pelo usuário.
- **Stage area:** Manipulado pelo usuário.
- **Repositório local:** Gerenciado pelo Git.
- **Repositório remoto:** Gerenciado pelo Git.

### 6) O que o Git armazena na pasta `.git`?
- Configurações, histórico de commits e branches.

### 7) Comando para mover arquivos para a stage area:
- `git add nome_do_arquivo`

### 8) Comando para mover arquivos da stage area para o repositório local:
- `git commit -m "Mensagem do commit"`

### 9) Estado do arquivo `file.txt` após ser criado sem `git add`:
- O arquivo está presente, mas não está versionado.

### 10) Diferença entre `git add .` e `git add --all`:
- `git add .` adiciona arquivos do diretório atual e subpastas.
- `git add --all` adiciona todos os arquivos modificados e não rastreados.

### 11) Estados de um arquivo no Git:
- **Tracked:** Versionado.
- **Untracked:** Não está no Git.
- **Staged:** Pronto para commit.
- **Not Staged:** Modificado, mas não adicionado.

### 12) O que acontece quando um arquivo da stage area é modificado?
- Ele volta ao estado de **Not Staged**, exigindo um novo `git add`.

### 13) Diferença entre `git status` e `git log`:
- `git status`: Mostra o estado atual dos arquivos.
- `git log`: Exibe o histórico de commits.

### 14) Para que serve o hash de um commit?
- Identifica de forma única cada commit.

### 15) Para que serve `git diff`?
- Exibe as diferenças entre versões dos arquivos antes do commit.

### 16) Para que serve `git push`?
- Envia commits do repositório local para o remoto.

### 17) Explicação do comando `git push -u origin main`:
- **push:** Envia commits.
- **-u:** Define o repositório remoto padrão.
- **origin:** Nome do repositório remoto.
- **main:** Nome da branch atualizada.

### 18) Diferença entre `git pull` e `git fetch`:
- `git pull`: Atualiza o repositório local com as mudanças remotas.
- `git fetch`: Baixa as mudanças, mas não aplica automaticamente.

### 19) Dois desenvolvedores estão trabalhando em um mesmo projeto.  

**a) Por que o comando da Linha 6 irá falhar?**  
Porque a Desenvolvedora B já realizou um push com novas alterações, e o repositório remoto tem mudanças que o Desenvolvedor A ainda não baixou. O Git impede que um push sobrescreva alterações remotas para evitar perda de dados.  

**b) O que aconteceria se o Desenvolvedor A executasse um comando pull entre as Linhas 5 e 6?**  
Ele baixaria as alterações da Desenvolvedora B antes de tentar o push. Se houver conflitos, ele precisaria resolvê-los antes de concluir o push.  

### 20) O que fazer caso ocorra um conflito de merge após um `git pull`?  
O conflito deve ser resolvido manualmente editando os arquivos, escolhendo quais mudanças manter e, em seguida, realizando um novo commit. Para evitar conflitos em equipe, boas práticas incluem sempre fazer `git pull` antes de iniciar mudanças e comunicar alterações grandes.  

### 21) O que são branches e qual sua função?  
Branches são ramificações independentes do código usadas para desenvolver novas funcionalidades sem afetar o código principal.  

### 22) Diferença entre `git branch` e `git branch issue-22`:  
- `git branch`: Lista todas as branches do repositório.  
- `git branch issue-22`: Cria uma nova branch chamada `issue-22`.  

### 23) Para que serve `git checkout`?  
1. Mudar para outra branch (`git checkout nome-da-branch`).  
2. Restaurar um arquivo para sua versão mais recente (`git checkout -- nome-do-arquivo`).  
3. Criar uma nova branch e mudar para ela (`git checkout -b nova-branch`).  

### 24) Como funciona o processo de merge entre branches?  
Unir mudanças de uma branch a outra. Exemplo:  
```bash
# Alternar para a branch principal
git checkout main
# Fazer o merge da branch de desenvolvimento
git merge feature-branch
```
Se houver conflitos, é necessário resolvê-los antes de concluir o merge.  

### 25) O que é merge hell?  
Situação onde muitos conflitos de merge ocorrem, tornando difícil integrar mudanças.  

### 26) O que é Integração Contínua e como evita merge hell?  
Prática de integrar mudanças frequentemente para evitar acúmulo de conflitos.  

### 27) Para que serve a variável HEAD? O que é Detached HEAD?  
- **HEAD** aponta para o commit atual.  
- **Detached HEAD** ocorre quando se acessa um commit antigo, sem estar em uma branch. Mudanças feitas nesse estado podem ser perdidas se não forem salvas corretamente.  

### 28) Como ficará o grafo de commits após os comandos listados?  
O histórico terá um novo commit `add something.py`, seguido pelo merge da branch `issue-22`.  

### 29) Para que serve `git stash`?  
Salva temporariamente mudanças não commitadas, permitindo mudar de branch sem perdê-las.  

### 30) Diferença entre `git stash pop` e `git stash apply`:  
- `git stash pop`: Aplica as mudanças salvas e remove do stash.  
- `git stash apply`: Aplica as mudanças, mas mantém no stash.  

### 31) Para que serve `.gitignore`?  
Define arquivos que devem ser ignorados pelo Git, como logs e configurações locais.  

### 32) Para que serve `git rebase`?  
Reorganiza commits para manter um histórico linear.  

### 33) Por que `git rebase` deve ser usado com cautela?  
Se usado em commits já enviados ao repositório remoto, pode causar problemas para outros desenvolvedores.  

### 34) O que são pull requests e sua importância?  
Solicitação para mesclar mudanças em um repositório remoto, permitindo revisão antes da integração.  

### 35) Para que serve `git squash`?  
Combina múltiplos commits em um só, útil para manter o histórico limpo antes de um pull request.  

### 36) Para que serve um fork? Diferença entre fork e clone?  
- **Fork**: Cria uma cópia independente de um repositório no GitHub.  
- **Clone**: Copia um repositório para o computador local, mas ainda vinculado ao original.  

### 37) Como utilizar fork para colaborar em software livre?  
Fluxo básico para contribuir:  
```bash
# Fazer fork do repositório no GitHub
git clone URL_DO_FORK
cd projeto
git checkout -b minha-correção
# Fazer mudanças, commit e push
git push origin minha-correção
# Criar um pull request no GitHub
```

### 38) O que são issues no GitHub?  
São registros de problemas, sugestões ou tarefas dentro de um repositório.

## Contribuição
Este repositório é um material de estudo pessoal, mas caso queira sugerir melhorias ou complementar as respostas, sinta-se à vontade para abrir um pull request!