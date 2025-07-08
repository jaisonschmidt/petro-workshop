# Git - Comandos Essenciais

Este guia apresenta os principais comandos do Git para controle de versão. Alterei este README no GitHub.

## Configuração Inicial

```bash
# Configurar nome de usuário
git config --global user.name "Seu Nome"

# Configurar email
git config --global user.email "seu@email.com"

# Verificar configurações
git config --list
```

## Inicializando um Repositório

```bash
# Inicializar um novo repositório
git init

# Clonar um repositório existente
git clone https://github.com/usuario/repositorio.git
```

## Comandos Básicos

### Status e Informações

```bash
# Verificar status dos arquivos
git status

# Ver histórico de commits
git log

# Ver histórico resumido
git log --oneline

# Ver diferenças nos arquivos
git diff
```

### Adicionando e Commitando

```bash
# Adicionar arquivo específico
git add arquivo.txt

# Adicionar todos os arquivos
git add .

# Fazer commit
git commit -m "Mensagem do commit"

# Adicionar e commitar em um comando
git commit -am "Mensagem do commit"
```

## Trabalhando com Branches

```bash
# Listar branches
git branch

# Criar nova branch
git branch nome-da-branch

# Mudar para uma branch
git checkout nome-da-branch

# Criar e mudar para nova branch
git checkout -b nome-da-branch

# Deletar branch
git branch -d nome-da-branch

# Mergear branch
git merge nome-da-branch
```

## Comandos Remotos

```bash
# Adicionar repositório remoto
git remote add origin https://github.com/usuario/repositorio.git

# Ver repositórios remotos
git remote -v

# Enviar mudanças para o repositório remoto
git push origin main

# Baixar mudanças do repositório remoto
git pull origin main

# Baixar mudanças sem fazer merge
git fetch origin
```

## Comandos de Desfazer

```bash
# Desfazer mudanças não commitadas
git checkout -- arquivo.txt

# Remover arquivo do staging
git reset HEAD arquivo.txt

# Voltar ao commit anterior (mantém mudanças)
git reset --soft HEAD~1

# Voltar ao commit anterior (remove mudanças)
git reset --hard HEAD~1

# Reverter um commit específico
git revert hash-do-commit
```

## Comandos Úteis

```bash
# Ver arquivos ignorados
git ls-files --ignored --exclude-standard

# Limpar arquivos não rastreados
git clean -fd

# Salvar mudanças temporariamente
git stash

# Recuperar mudanças salvas
git stash pop

# Listar stashes
git stash list

# Ver detalhes de um commit
git show hash-do-commit

# Buscar por texto no histórico
git log --grep="texto"
```

## Exemplo de Workflow Básico

```bash
# 1. Clonar repositório
git clone https://github.com/usuario/projeto.git

# 2. Entrar no diretório
cd projeto

# 3. Criar nova branch para feature
git checkout -b minha-feature

# 4. Fazer mudanças nos arquivos
# ... editar arquivos ...

# 5. Adicionar mudanças
git add .

# 6. Fazer commit
git commit -m "Adicionar nova feature"

# 7. Enviar para repositório remoto
git push origin minha-feature

# 8. Voltar para branch principal
git checkout main

# 9. Fazer merge da feature
git merge minha-feature

# 10. Enviar mudanças finais
git push origin main
```

## Arquivo .gitignore

Crie um arquivo `.gitignore` para ignorar arquivos desnecessários:

```
# Dependências
node_modules/
*.log

# Arquivos de configuração
.env
.DS_Store

# Arquivos compilados
*.class
*.jar
build/
dist/
```

## Dicas Importantes

- Use mensagens de commit descritivas
- Faça commits pequenos e frequentes
- Sempre teste antes de fazer push
- Use branches para novas features
- Mantenha o histórico limpo

## GitHub Flow

O GitHub Flow é uma metodologia de trabalho leve e baseada em branches que facilita a colaboração em projetos. O fluxo consiste em: criar uma branch a partir da `main`, fazer commits com suas mudanças, abrir um Pull Request para discussão e revisão, fazer ajustes baseados no feedback recebido, e finalmente fazer o merge para a branch principal após aprovação. Esta abordagem promove um desenvolvimento contínuo e seguro, onde cada mudança é revisada antes de ser integrada, mantendo a branch principal sempre estável e deployable. É ideal para equipes que trabalham com deploy contínuo e querem manter um histórico linear e limpo.

---

*Este README serve como referência rápida para os comandos Git mais utilizados.*
