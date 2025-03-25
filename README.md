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

## Contribuição
Este repositório é um material de estudo pessoal, mas caso queira sugerir melhorias ou complementar as respostas, sinta-se à vontade para abrir um pull request!