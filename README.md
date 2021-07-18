# Git Flow

### Passos basicos
    Configuração de branch
    Pull Request  Templates para PR
    Code Review
    CodeOwners
    Plugin do VsCode

### Versionamento semantico
    Sememantical Versioning (SemVer)
    Conventional Commits

### Instalação do git flow
    https://github.com/petervanderdoes/gitflow-avh/wiki/Installation

### Comandos do git flow
    git flow
      init      Initialize a new git repo with support for the branching model.
      feature   Manage your feature branches.
      bugfix     Manage your bugfix branches.
      release   Manage your release branches.
      hotfix     Manage your hotfix branches.
      support   Manage your support branches.
      version   Shows version information.
      config     Manage your git-flow configuration.
      log       Show log deviating from base branch.

### Criar uma feature
    git flow feature start nome_da_feature
#### Encerrar uma feature
    git flow feature finish nome_da_feature

### Criando release
    git flow release start 0.1.2
#### Encerrando a release
    git flow release finish 0.1.2

## Assinaturas de Commits

### Listando chaves gpg
    gpg --list-secret-key --keyid-form LONG
### Criando chaves gpg
    gpg --full-generate-key

### Exportando chave publica gerada
    gpg --armor --export chave_rsa4096/
### Adicionando chave na config do git
    git config --global user.signingkey chave_rsa4096/

### Adicionado variavel de ambiente tty
    export GPG_TTY=$(tty)
    -> adicionar no bash profile ou zsh profile

### Criando assinaturas para commits
    git config --global commit.gpgsign true
### Criando assinaturas para tags
    git config --global tag.gpgSign true

### Editando a gpg
    gpg --edit-key rsa4096/
        adduid
        trust
        save
