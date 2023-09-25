# **Alguns apontamentos a respeito de Git, Github e Markdown**

# Git

## Introdução

Git é um sistema de controle de versão distribuído que permite aos desenvolvedores colaborar em projetos de código-fonte. Com o Git, é possível acompanhar as alterações feitas no código ao longo do tempo, experimentar novas ideias em branches separados e mesclar essas alterações de volta ao branch principal quando estiverem prontas.

## Instalação

Para instalar o Git, siga as instruções para o seu sistema operacional:

- **Windows**: Baixe o instalador do site oficial do Git e execute-o.
- **macOS**: Use o gerenciador de pacotes Homebrew para instalar o Git com o comando `brew install git`.
- **Linux**: Use o gerenciador de pacotes da sua distribuição para instalar o Git. Por exemplo, no Ubuntu ou Debian, use o comando `sudo apt-get install git`.

## Configuração

Antes de começar a usar o Git, é importante configurá-lo com seu nome e endereço de e-mail. Isso pode ser feito com os seguintes comandos:
```
git config --global user.email you@example.com
git config --global user.name "Your Name"
```
*--global -> Configuração para a máquina toda*
*--local  -> Configuração para o projeto*

Para criar um novo repositório local, use o comando `git init` dentro do diretório do projeto. Para clonar um repositório existente, use o comando `git clone <url-do-repositório>`.

## Comandos básicos

Aqui estão alguns dos comandos básicos do Git que você usará com frequência:

- `git status`: Mostra o estado atual do repositório, incluindo quaisquer alterações não confirmadas.
- `git add <arquivo>`: Adiciona um arquivo ao índice de preparação para ser incluído no próximo commit.
- `git commit -m "mensagem"`: Cria um novo commit com as alterações preparadas e uma mensagem descritiva.
- `git push`: Envia os commits locais para o repositório remoto.
- `git pull`: Atualiza o repositório local com as alterações do repositório remoto.
- `git --version`: Verifica se o git está instalado e qual a sua versão



## Branches

Branches são uma maneira de experimentar novas ideias sem afetar o branch principal. Para criar um novo branch, use o comando `git branch <nome-do-branch>`. Para mudar para um branch existente, use o comando `git checkout <nome-do-branch>`. Para excluir um branch, use o comando `git branch -d <nome-do-branch>`.

## Merge e rebase

Para mesclar as alterações de um branch em outro, use o comando `git merge <nome-do-branch>`. Isso criará um novo commit que combina as alterações dos dois branches.

O comando `git rebase` permite reescrever o histórico do commit ao mover os commits de um branch para outro. Isso pode ser útil para manter um histórico limpo e linear.

## Resolução de conflitos

Quando duas branches modificam a mesma parte de um arquivo, pode ocorrer um conflito de mesclagem. O Git marcará os conflitos no arquivo e você precisará resolvê-los manualmente antes de poder continuar.

## Outros comandos:
  
Visualizar as configurações válidas para o projeto:  

```
git config user.name
```  
  
Erro SSL Certificate Problem:  
```
git config --global http.sslbackend schannel
```

3. Inicializando um repositório 
```
git init  
git status
```

4. Adicionando arquivos ao staged 

git add nome_arquivo   
git add . 

6. Consolidando alterações 

git commit -m "comentário"

- Adicionando e Consolidando as alterações em um único comando

git commit am “Criando website XPTO”


7. Mapeando um repositório remoto

git remote add origin "http://...url do rep remoto..."  
git remote -v 

8. Enviando as alterações para o repositório remoto (Sincronizando o Rep. Remoto)

git push -u origin master 
git push 
git push origin master --force   

9. Clonando um repositório remoto 

git clone "http://...url do rep remoto..."

10. Atualizando o Repositório Local 

git pull 

11. Renomeando a Branch

git branch -M main 


# GitHub

## Introdução

O GitHub é uma plataforma online que permite hospedar e colaborar em projetos de código-fonte. Com o GitHub, é possível acompanhar as alterações feitas no código ao longo do tempo, experimentar novas ideias em branches separados e mesclar essas alterações de volta ao branch principal quando estiverem prontas.

## Criação de conta

Para criar uma conta no GitHub, visite o site do GitHub e clique em "Sign up". Siga as instruções na tela para criar sua conta.

Depois de criar sua conta, você pode configurar seu perfil acessando a página "Settings" no canto superior direito da tela. Lá, você pode adicionar informações sobre você, incluindo seu nome, biografia e foto de perfil.

## Repositórios

Um repositório é um local onde o código-fonte de um projeto é armazenado. No GitHub, você pode criar repositórios para seus próprios projetos ou clonar repositórios existentes para contribuir com eles.

Para criar um novo repositório, clique no botão "+" no canto superior direito da tela e selecione "New repository". Siga as instruções na tela para criar seu repositório.

Para clonar um repositório existente, visite a página do repositório e clique no botão "Code" para copiar a URL do repositório. Em seguida, use o comando `git clone <url-do-repositório>` para clonar o repositório para sua máquina local.

Você também pode bifurcar (fork) um repositório existente para criar uma cópia dele em sua própria conta. Isso é útil quando você quer contribuir com um projeto, mas não tem permissão para fazer alterações diretamente no repositório original. Para bifurcar um repositório, visite a página do repositório e clique no botão "Fork" no canto superior direito da tela.

Para excluir um repositório, visite a página "Settings" do repositório e clique na aba "Danger Zone". Lá, você encontrará a opção para excluir o repositório.

## Colaboração

O GitHub oferece várias ferramentas para colaborar em projetos. Você pode enviar solicitações de pull (pull requests) para propor alterações ao código-fonte, revisar código enviado por outros colaboradores e gerenciar problemas (issues) relacionados ao projeto.

Para enviar uma solicitação de pull, crie um branch separado com suas alterações e envie-o para o repositório remoto. Em seguida, visite a página do repositório no GitHub e clique na aba "Pull requests". Lá, você pode criar uma nova solicitação de pull selecionando o branch que você enviou.

Outros colaboradores podem revisar suas alterações e deixar comentários na página da solicitação de pull. Quando suas alterações forem aprovadas, elas poderão ser mescladas ao branch principal.

Você também pode usar a aba "Issues" para gerenciar problemas relacionados ao projeto. Lá, você pode criar novos problemas (issues), atribuí-los a colaboradores específicos e acompanhar seu progresso.

## Fluxo de trabalho

O fluxo de trabalho típico do GitHub envolve criar branches separados para experimentar novas ideias, fazer commits com suas alterações, enviar solicitações de pull para propor essas alterações ao branch principal e mesclar as alterações quando elas forem aprovadas.

Exemplo de fluxo de trabalho:

1. Crie um branch separado para sua nova ideia com o comando `git checkout -b <nome-do-branch>`.
2. Faça suas alterações no código e use os comandos `git add` e `git commit` para preparar e confirmar suas alterações.
3. Envie seu branch para o repositório remoto com o comando `git push -u origin <nome-do-branch>`.
4. Visite a página do repositório no GitHub e crie uma nova solicitação de pull selecionando o branch que você enviou.
5. Aguarde a revisão de suas alterações por outros colaboradores. Faça as alterações necessárias de acordo com os comentários recebidos.
6. Quando suas alterações forem aprovadas, elas poderão ser mescladas ao branch principal.

## Recursos avançados

O GitHub oferece vários recursos avançados para ajudar a gerenciar seus projetos. Alguns desses recursos incluem:

- **Integração contínua (CI)**: O GitHub permite integrar ferramentas de CI como o Travis CI e o Jenkins para automatizar tarefas como a execução de testes e a implantação de código.
- **Actions**: O GitHub Actions permite automatizar tarefas como a execução de testes, a construção de código e a implantação de aplicativos usando workflows personalizados.
- **GitHub Pages**: O GitHub Pages permite hospedar páginas estáticas diretamente do seu repositório no GitHub. Isso é útil para criar documentação, portfólios e outros tipos de páginas.

# Markdown

## Introdução

Markdown é uma linguagem de marcação leve que permite formatar texto de maneira simples e legível. É amplamente usado em plataformas como o GitHub, onde é usado para formatar arquivos README, comentários e outras partes do site.

## Sintaxe básica

Elementos básicos da sintaxe do Markdown:

- **Cabeçalhos**: Use `#` para criar cabeçalhos. Adicione mais `#` para criar subcabeçalhos. Por exemplo:

```
# Título
## Subtítulo
### Sub-subtítulo
```
# Título
## Subtítulo
### Sub-subtítulo

- **Listas**: Use `*` ou `-` para criar listas não ordenadas. Use números seguidos de um ponto para criar listas ordenadas. Por exemplo:

```
* Item 1
* Item 2
* Item 3

1. Primeiro item
2. Segundo item
3. Terceiro item
```

- **Links**: Use `[texto](url)` para criar um link. Por exemplo: `[GitHub](https://github.com)`.

- **Imagens**: Use `![texto alternativo](url-da-imagem)` para inserir uma imagem. Por exemplo: `![Logo do GitHub](https://github.com/logo.png)`.

- **Código**: Use `` `código` `` para código inline e ``` ```código``` ``` para blocos de código. Por exemplo:

```
Este é um `código inline`.

```
Este é um bloco de código.
```
```

## Tabelas

Para criar tabelas no Markdown, use a sintaxe de tabela. Por exemplo:

```
| Cabeçalho 1 | Cabeçalho 2 | Cabeçalho 3 |
| --- | --- | --- |
| Célula 1 | Célula 2 | Célula 3 |
| Célula 4 | Célula 5 | Célula 6 |
```

Isso criará uma tabela como esta:

| Cabeçalho 1 | Cabeçalho 2 | Cabeçalho 3 |
| --- | --- | --- |
| Célula 1 | Célula 2 | Célula 3 |
| Célula 4 | Célula 5 | Célula 6 |

## Realce de sintaxe

Para usar o realce de sintaxe em blocos de código no Markdown, adicione o nome da linguagem após os três acentos graves iniciais. Por exemplo:

```
[Comment]:
(```python
def hello():
    print("Hello, world!"))
```
Isso criará um bloco de código com realce de sintaxe para a linguagem Python.

## GitHub Flavored Markdown

O GitHub usa uma versão personalizada do Markdown chamada GitHub Flavored Markdown (GFM). Ele inclui elementos adicionais como tarefas e menções.

Para criar uma lista de tarefas, use `- [ ]` para itens não marcados e `- [x]` para itens marcados. Por exemplo:

```
- [x] Tarefa concluída
- [ ] Tarefa pendente
```

Isso criará uma lista de tarefas como esta:

- [x] Tarefa concluída
- [ ] Tarefa pendente

Para mencionar outro usuário do GitHub, use `@nome-do-usuário`. Por exemplo: `@github`.

## Ferramentas

Ferramentas úteis para trabalhar com o Markdown:

- **Editores online**: Existem vários editores online que permitem escrever e visualizar o Markdown em tempo real. Alguns exemplos incluem [Dillinger](https://dillinger.io) e [StackEdit](https://stackedit.io).
- **Extensões para navegadores**: Existem extensões para navegadores como o Chrome e o Firefox que adicionam recursos úteis para trabalhar com o Markdown, como a visualização de arquivos `.md` locais e a formatação automática de texto selecionado.

# O básico de HTML

## Conceito
HTML, ou **HyperText Markup Language**, é uma linguagem de marcação utilizada para estruturar conteúdos na web. Ela permite que você crie documentos que podem ser lidos por navegadores web. O HTML não é uma linguagem de programação, mas sim uma linguagem de marcação que define a estrutura de seu conteúdo.

## História
O HTML foi criado em 1990 por **Tim Berners-Lee** enquanto trabalhava no CERN, o laboratório de física de partículas na Suíça. Ele desenvolveu o HTML para criar páginas web simples que pudessem ser entregues através da internet e visualizadas em um navegador web.

## Principais Comandos

### Estrutura Básica
Um documento HTML começa com a declaração do tipo de documento `<!DOCTYPE html>`. O documento HTML é então iniciado com a tag `<html>` e termina com `</html>`. Dentro dessas tags, temos duas partes principais: `<head>` e `<body>`.

```html
<!DOCTYPE html>
<html>
<head>
    <!-- Informações sobre a página -->
</head>
<body>
    <!-- Conteúdo da página -->
</body>
</html>
```

### Títulos e Parágrafos
Os títulos são definidos usando as tags `<h1>` a `<h6>`, onde `<h1>` define o título mais importante e `<h6>` o menos importante. Os parágrafos são definidos usando a tag `<p>`.

```html
<h1>Este é um título</h1>
<p>Este é um parágrafo.</p>
```

### Links
Os links são definidos usando a tag `<a>` (ancla). O atributo `href` especifica o URL do link.

```html
<a href="https://www.example.com">Este é um link</a>
```

### Imagens
As imagens são definidas usando a tag `<img>`. O atributo `src` especifica o caminho para a imagem e o atributo `alt` fornece um texto alternativo para a imagem.

```html
<img src="imagem.jpg" alt="Descrição da imagem">
```

### Listas
Existem dois tipos de listas em HTML: listas ordenadas e listas não ordenadas. As listas ordenadas são criadas com a tag `<ol>` e as listas não ordenadas com a tag `<ul>`. Os itens da lista são colocados dentro dessas tags usando a tag `<li>`.

```html
<ol>
    <li>Primeiro item</li>
    <li>Segundo item</li>
</ol>

<ul>
    <li>Item não ordenado</li>
    <li>Outro item não ordenado</li>
</ul>
```

### Tabelas
As tabelas são definidas com a tag `<table>`, e as linhas e células da tabela são definidas com as tags `<tr>` e `<td>` respectivamente.

```html
<table>
    <tr>
        <td>Célula 1</td>
        <td>Célula 2</td>
    </tr>
    <tr>
        <td>Célula 3</td>
        <td>Célula 4</td>
    </tr>
</table>
```

### Formulários
Os formulários são definidos com a tag `<form>`. Dentro de um formulário, você pode ter elementos de entrada, como campos de texto, caixas de seleção, botões de rádio e botões de envio.

```html
<form action="/submit_form" method="post">
    <label for="name">Nome:</label><br>
    <input type="text" id="name" name="name"><br>
    <input type="submit" value="Enviar">
</form>
```

### Divisões e Span
As tags `<div>` e `<span>` são usadas para agrupar outros elementos HTML. A tag `<div>` é um elemento de bloco, enquanto a tag `<span>` é um elemento inline.

```html
<div>
    Este é um bloco de texto.
    <span>Este é um trecho de texto.</span>
</div>
```

### Estilos CSS
Os estilos CSS podem ser aplicados a elementos HTML para alterar sua aparência. Os estilos podem ser definidos dentro da tag `<style>` no cabeçalho do documento, ou inline usando o atributo `style`.

```html
<head>
    <style>
        body {background-color: powderblue;}
        h1   {color: blue;}
        p    {color: red;}
    </style>
</head>

<body>
    <h1>Este é um título</h1>
    <p style="color:green;">Este é um parágrafo.</p>
</body>
```

# CSS

## Conceito
CSS, ou **Cascading Style Sheets**, é uma linguagem de folha de estilo usada para descrever a aparência de um documento escrito em HTML. O CSS descreve como os elementos HTML devem ser exibidos na tela, no papel, na fala ou em outras mídias.

## História
O CSS foi proposto pela primeira vez por Håkon Wium Lie em 1994. Na época, Lie estava trabalhando com Tim Berners-Lee no CERN. O desenvolvimento do CSS foi então assumido pela World Wide Web Consortium (W3C) e a primeira especificação CSS foi publicada em 1996.

## Principais Comandos

### Sintaxe Básica
A sintaxe CSS consiste em um seletor e um bloco de declaração. O seletor aponta para o elemento HTML que você deseja estilizar. O bloco de declaração contém uma ou mais declarações separadas por ponto e vírgula.

```css
seletor {
    propriedade: valor;
}
```

### Cores
As cores em CSS podem ser especificadas por nomes predefinidos, valores RGB, valores HEX, valores HSL, valores RGBA e valores HSLA.

```css
body {
    background-color: lightblue;
}

h1 {
    color: #ff0000;
}

p {
    color: rgb(0,0,255);
}
```

### Bordas
As bordas em CSS são usadas para especificar o estilo, a cor e o tamanho das bordas de um elemento.

```css
p {
    border-style: solid;
    border-color: red;
    border-width: 5px;
}
```

### Margens
As margens em CSS são usadas para criar espaço ao redor dos elementos, fora de quaisquer bordas definidas.

```css
p {
    margin-top: 50px;
    margin-bottom: 100px;
    margin-right: 150px;
    margin-left: 200px;
}
```

### Preenchimento
O preenchimento em CSS é usado para criar espaço ao redor do conteúdo do elemento, dentro de quaisquer bordas definidas.

```css
p {
    padding-top: 50px;
    padding-bottom: 100px;
    padding-right: 150px;
    padding-left: 200px;
}
```

### Fontes
O CSS permite que você controle o tipo de fonte, o tamanho, o peso, a cor e outras propriedades do texto.

```css
p {
    font-family: "Times New Roman", Times, serif;
    font-size: 20px;
    font-weight: bold;
    color: #ff0000;
}
```

### Posicionamento
O CSS permite que você controle a posição dos elementos na página usando as propriedades `position`, `top`, `right`, `bottom` e `left`.

```css
div {
    position: absolute;
    top: 50px;
    right: 100px;
    bottom: 150px;
    left: 200px;
}
```

### Display e Visibilidade
As propriedades `display` e `visibility` permitem que você controle a exibição e a visibilidade dos elementos.

```css
div {
    display: none; /* O elemento não será exibido */
}

p {
    visibility: hidden; /* O elemento será invisível, mas ainda ocupará espaço */
}
```

### Background
O CSS permite que você controle a cor de fundo, a imagem de fundo e outras propriedades de fundo dos elementos.

```css
body {
    background-color: #ff0000; /* Cor de fundo */
    background-image: url("imagem.jpg"); /* Imagem de fundo */
    background-repeat: no-repeat; /* A imagem de fundo não se repetirá */
    background-position: right top; /* Posição da imagem de fundo */
}
```

# Flexbox em CSS

## Conceito
Flexbox, ou modelo de layout flexível, é um conceito em CSS que permite que você crie layouts complexos com mais eficiência e consistência. Ele é especialmente útil quando você precisa alinhar elementos de maneira proporcional e dinâmica ou precisa de um layout que se adapte a diferentes tamanhos de tela.

## Principais Comandos

### Container Flex
Para começar a usar o flexbox, você precisa definir um container flex usando a propriedade `display` com o valor `flex` ou `inline-flex`.

```css
.container {
    display: flex;
}
```

### Direção Flex
A propriedade `flex-direction` define a direção principal em que os itens flex são colocados no container flex. Os valores possíveis são `row` (padrão), `row-reverse`, `column` e `column-reverse`.

```css
.container {
    flex-direction: row;
}
```

### Envolvimento Flex
A propriedade `flex-wrap` especifica se os itens flex devem ser forçados a uma única linha (não envolver) ou podem ser dispostos em várias linhas (envolver). Os valores possíveis são `nowrap` (padrão), `wrap` e `wrap-reverse`.

```css
.container {
    flex-wrap: wrap;
}
```

### Alinhamento Flex
Existem várias propriedades para alinhar itens em um container flex:

- `justify-content`: alinha os itens ao longo do eixo principal (por exemplo, da esquerda para a direita). Os valores possíveis incluem `flex-start`, `flex-end`, `center`, `space-between`, `space-around` e `space-evenly`.
- `align-items`: alinha os itens ao longo do eixo transversal (por exemplo, de cima para baixo). Os valores possíveis incluem `stretch`, `flex-start`, `flex-end`, `center` e `baseline`.
- `align-content`: alinha as linhas de envolvimento ao longo do eixo transversal. Isso só tem efeito se houver várias linhas de envolvimento. Os valores possíveis são os mesmos que para `align-items`.

```css
.container {
    justify-content: space-between;
    align-items: center;
}
```

### Itens Flex
Os itens flex podem ter as seguintes propriedades:

- `order`: especifica a ordem de um item em relação aos outros itens no container flex.
- `flex-grow`: especifica quanto um item deve crescer em relação aos outros itens, se houver espaço extra disponível.
- `flex-shrink`: especifica quanto um item deve encolher em relação aos outros itens, se o espaço for limitado.
- `flex-basis`: especifica o tamanho inicial de um item antes de o espaço restante ser distribuído.
- `flex`: é uma abreviação para definir as três propriedades anteriores de uma vez. O valor é uma lista separada por espaços de três valores correspondendo a `flex-grow`, `flex-shrink` e `flex-basis`.

```css
.item {
    order: 2;
    flex: 1 1 auto;
}
```