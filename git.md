# Como enviar um novo projeto inicial para o github usando o VSCODE

Aqui estão os passos detalhados necessários para conseguir isso.

Os comandos existentes podem ser simplesmente executados através do terminal CLI do VSCODE. Entende-se que o Git está instalado no sistema, configurado com o nome de usuário e o ID de e-mail desejados.

1. Navegue até o diretório do projeto local e crie um repositório git local:

```html
git init
```

2. Uma vez que seja bem sucedido, clique no ícone 'Source Control' na barra de navegação à esquerda no VS-Code. Deve ser possível ver os arquivos prontos para serem confirmados. Pressione o botão 'Confirmar', forneça comentários, organize as alterações e confirme os arquivos. Como alternativa, você pode executar a partir do CLI

```html
git commit -m "Your comment"
```

3. Agora você precisa visitar sua conta do GitHub e criar um novo Repositório. Exclua a criação de arquivos 'README.md', '.gitIgnore'. Também não adicione nenhuma licença ao repositório. Às vezes, essas configurações causam problemas durante o envio.

4. Copie o link para este repositório GitHub recém-criado.

5. Volte para o terminal no VS-CODE e digite estes comandos em sucessão:

```html
git remote add Origin <link to GitHub Repo /> //maps the remote repo link to
local git repo
```

```html
git remote -v //this is to verify the link to the remote repo
```

```html
git Push -u Origin master // pushes the commit-ed changes into the remote repo
```

Nota: Se é a primeira vez que a conta git local está tentando se conectar ao GitHub, você pode ser solicitado a inserir credenciais no GitHub em uma janela separada.

6. Você pode ver a mensagem de sucesso no Terminal. Você também pode verificar atualizando o repositório on-line do GitHub.

---

## Alguns comando em Git e Github para serem executados no terminal

## Explicação

## Pastas

Entrar na pasta

```html
cd /<nome_da_pasta></nome_da_pasta>
```

Retornar uma pasta

```html
cd ..
```

Listar arquivos dentro da pasta

```html
ls
```

Listar arquivos dentro da pasta + arquivos ocultos

```html
ls -a
```

Criar uma pasta

```html
mkdir <nome_da_pasta></nome_da_pasta>
```

Mover um arquivo para dentro de uma pasta

```html
mv <nome_do_arquivo> ./<nome_da_pasta>/</nome_da_pasta></nome_do_arquivo>
```

## Git help

Lista de comandos

```html
git help
```

Lista de comandos especificos

```html
git help <qualquer_comando_git></qualquer_comando_git>
```

## Git init

Para começar um projeto que ainda não seja um repositório

```html
git init
```

## Git clone

Comando para baixar o código-fonte existente de um repositório remoto

```html
git clone <https://url-do-link>
```

Desvincular a sua cópia do original:

```html
git remote rm origin
```

## Git status

O comando status do Git fornece algumas informações sobre a branch em que você estiver no momento

```html
git status
```

Status possiveis

```html
(modified); (staged/index) (comitted);
```

## Git add

Quando criamos, modificamos ou excluímos um arquivo, essas alterações ocorrerão em nosso ambiente local e não serão incluídas no próximo commit (a menos que alteremos as configurações).

```html
git add
```

Para adicionar, de uma vez, todos os arquivos modificados:

```html
git add *
```

Ou:

```html
git add .
```

## Git commit

Este comando é como definir um ponto de verificação no processo de desenvolvimento, para o qual você pode voltar mais tarde, se necessário.

```html
git commit -m "Explicar o que foi alterado"
```

## Git push

Após confirmar as alterações, a próxima coisa que você deseja fazer é enviar as alterações para o servidor remoto.
O comando git push envia e salva suas confirmações no repositório remoto

```html
git push <remote> <nome_do_branch></nome_do_branch></remote>
```

## Git pull

```html
git pull <remote></remote>
```

O comando git pull é usado para obter atualizações do repositório remoto. O comando de pull depende do referencial de onde ele foi feito, ou seja, um git pull feito da sua máquina vai puxar informações do repositório original para ela.

## Git log

O comando log apresenta informações sobre o projeto

Author e Data de Criação:

```html
git log
```

Monstrar historico de commits

```html
git log --oneline
```

---
