# Aula 01

## Workshop Node.JS

> Caso tenha duvidas de como navegar nas aulas e como foi estruturado nosso curso, você sempre pode voltar ao branch principal e ler o README.md usando o comando `git checkout master`

# O que vamos aprender?

Nessa primeira aula, vamos falar um pouco da história, como é porque usar o node, e no final vamos criar nosso primeiro servidor node.js com dicas importantes e já aplicando as melhores praticas :)

# O que é?

# Quem esta usando?

# Vantagens

# Frameworks que ajudam no desenvolvimento do dia a dia

- ## Configurando ambiente

- ## [Visual Estudio](https://visualstudio.microsoft.com/) ou Editor de sua preferência

- ## Instalando o Node.js

- ## O que é NPM

O npm é o gerenciador de pacotes do Node.Js _(Node Package Manager)_ que vem junto com ele e que é muito útil no desenvolvimento Node. Por anos, o Node tem sido amplamente usado por desenvolvedores JavaScript para compartilhar ferramentas, instalar vários módulos e gerenciar suas dependências. Sabendo disso, é realmente importante para pessoas que trabalham com Node.js entendam o que é npm.

**Como Funciona?**

O npm funciona baseado nesses dois ofícios:

- Ele é um repositório amplamente usado para a publicação de projetos Node.js de código aberto (open-source). Isso significa que ele é uma plataforma online onde qualquer pessoa pode publicar e compartilhar ferramentas escritas em JavaScript.
- O npm é uma ferramenta de linha de comando que ajuda a interagir com plataformas online, como navegadores e servidores. Essa utilidade auxilia na instalação e desinstalação de pacotes, gerenciamento da versões e gerenciamento de dependências necessárias para executar um projeto.

Para usar os pacotes, seu projeto deve conter um arquivo chamado de package.json. Dentro do pacote, você encontrará metadados específicos para os projetos. Os metadados mostram alguns aspectos do projeto na seguinte ordem:

- O nome do projeto;
- A versão inicial;
- A descrição;
- O ponto de entrada;
- Os comandos de teste;
- O repositório git;
- As palavras-chave;
- A licença;
- As dependências;
- As dependências do desenvolvedor (devDependencies).
- Os metadados ajudam a identificar o projeto e agem como uma - base para que os usuários obtenham as informações sobre ele.

Abaixo temos o `package.json` de nosso curso, ele ainda esta bem basico e sem nenhuma dependencia, a medida que formos criando o conteúdo, ele ira sendo modificado aual apos aula.

```json
{
  "name": "workshop-node",
  "version": "1.0.0",
  "description": "Descrição do meu projeto. API em express.js usando node.js para workshop de node em bh",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/comunita/workshop-node.js.git"
  },
  "keywords": ["nodejs", "front-end", "api", "full-stack"],
  "author": "",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/comunita/workshop-node.js/issues"
  },
  "homepage": "https://github.com/comunita/workshop-node.js#readme"
}
```

**Iniciando como npm**

Vamos criar o `package.json` do nosso curso, o que foi mostrado acima. Para isso, basta usarmos o seguinte comando

```shell
npm init
```

Esse comando tem uma interface para que possamos criar o arquivo com `steps` a outra forma é você criar o arquivo sozinho pelo editor. Mas recomendamos e vamos ensiar pelos padrões, usando o guia do npm.

Basta a gente ir preenchendo o ou dando `yes` ou `no` a medida que ele for interagindo com vocês. No final, teremos um arquivo parecido com esse da aula acima.

Pelo NPM também vamos instalar pacotes (helpes) que irá nos ajudar durante o desenvolvimento. Mas a frente vamos mostrar e insinar como usar essa parte.

- ## [Eslint](https://eslint.org/)

ESLint é uma ferramenta de análise de código estática para identificar padrões problemáticos encontrados no código JavaScript. Foi criado por Nicholas C. Zakas em 2013. As regras no ESLint são configuráveis ​​e regras personalizadas podem ser definidas e carregadas.

Vamos usar para que ele nos informe em real time, qualquer problema no código, assim podendo sempre escrever um código limpo e sementico. A longo prazo você estará escrevendo tão bem, que o EsLint quase não irá te alertar dos problemas.

Para instalar e adiconar o projeto, vamos usar o seguinte comando.

```shell
npm install -g eslint
```

Isso é para que o npm instale o pacote de mode global em nosssa maquina, é necessário para que o editor mostre os erros em tempo real quando estivermos escrevendo o código.

Mas também precisamos adicionar esse pacote em nosso projeto, para que em processos de testes, CI/CD (vamos esplicar no final do curso o que são) possamos executar esse cara, para que ele nos informe de problema e não deixe a gente colocar erros em produção para nossos usuários.

PAra isso, vamos instalar o npm usando o modo `--save -dev` que fala assim para npm, instala o pacote, mas adicione ele em nosso `package.json` dentro de `devDependecies` - Isso serve para quando a gente colocar o nosso projeto no servidor, tudo funcionára como queremos, pois antes de cada passo, como mostramos no readme.md no inicio do cursto, precisamos sempre fazer um `npm install` - Sempre que estiver fazendo um deploy para produção ou quando adicionarmos ou mudarmos algo em nosso `package.json`

```shel
npm install --save -dev eslint
```

- ## [Prettier](https://prettier.io/)
