# Projeto do painel de meetups da Fácil Informática

Projeto feito para apresentação do meetup interno da Fácil informática.
Apresentando o Next.JS e seus conceitos como Headless

Desenvolvido com [Nextra](https://nextra.vercel.app)

**Nextra** é uma biblioteca desenvolvida em [Next.js](https://nextjs.org) e [MDX](https://mdxjs.com)  no-code site gerador.

![Painel de meetups](/public/Meetups.png)

---
Created by [@shuding](https://github.com/shuding) and [@pacocoursey](https://github.com/pacocoursey) at [Vercel](https://vercel.com). Released under the MIT license.
Adaptado por Anderson Rissardi.

Melhor visualização através do link publico do Notion. Veja [aqui](https://www.notion.so/15-Meetup-F-cil-985dae955b094596860ad5f454d58026)


---
# 15º Meetup Fácil

# Criando um painel de meetups com Next.JS

### **OBJETIVO**

Criar um painel interno em que seja possível visualizar todos os meetups que já aconteceram na Fácil conhecendo o NEXT.JS

### PROJETO

![Painel](/public/Meetups.png)

Mookup do painel de meetups

Painel bem simples, uma lista de meetups que ao selecionar o meetup o vídeo seria exibido no player.

Alinhado a esquerda um grid de cards que seriam os registros. 

Ao selecionar, os dados do Meetup seriam carregados

---

### VAMOS VER COMO FICOU?!?!

Pode ser acessado a qualquer momento através do endereço interno: 

[](http://sup-meetups:3000/)

Publicado somente internamente**

http://sup-meetups:3000

### O QUE É NEXT.JS?

![O que é?!?](/public/logo_next.png)

→ É um framework para criação de sistemas WEB;  

- Parte cliente é React
    - Prós:
        1. Melhores bibliotecas de componentes
        2. Maiores comunidades
        3. Performance
    - Contras:
        1. Pode acontecer um overhead no client-side
        2. Constantes atualizações
- Parte servidor é Node.JS
    - Prós:
        1. Altamente escalável
        2. Simples e leve para hospedar
        3. Rápido para começar a desenvolver
    - Contras:
        1. Dificuldades no tratamento de erros assíncronos
        2. Não tipado

→ Sistema híbrido SSG(Geração statica) e SSR(Server Side Rendering)

![usar.png](/public/usar.png)

- Páginas completamente staticas, geradas ou não no momento do build
- Páginas staticas geradas no build com a utilização de dados externos
- Páginas sempre serão processadas no servidor
- Páginas processadas no servidor somente a primeira vez
- Páginas processadas no servidor somente quando determinada condição for atendida(UpdatedOn > Última geração)

## Nosso dia a dia com WebForms

![WEB_Forms.png](/public/WEB_Forms.png)

**Nenhuma página statica, todas geradas sempre sobdemanda.**

---

### POR QUE USAR NEXT.JS?

![Untitled.png](/public/Untitled.png)

Principais diferenciais 

---

### COMO COMEÇAR UM PROJETO

- Ter o Node.JS ≥ 10.13

```bash
> npx create-next-app
> npm run dev
```

Pronto!

Basta acessar http://localhost:3000

Estrutura de pastas

![/Untitled%201.png](/public/Untitled%201.png)

---

### ROTEAMENTO BASEADO EM SISTEMA DE ARQUIVOS

- Não é necessário desenvolver toda a estrutura de rotas da aplicação
- Utiliza um sistema parecido com o WebForms e outras tecnologias mais antigas
    - Para criar uma página, basta criar um arquivo .js(React) na pasta ~/Pages
    - O nome do arquivo será utilizado como rota

    Então:

    Ao criar um arquivo about.js dentro da pasta pages bastaria acessar:

    ***http://localhost:3000/about***

---

### ENTREGA

O ponto de maior interesse talvez seja a geração do pacote final.

No momento em que o build será feito é quando um grande processamento ocorre gerando o pacote final a ser hospedado.

```bash
npm run build
```

Todo o processamento começa, fazendo conexão com banco de dados e tudo o que mais for necessário.

O pacote gerado é enviado para o diretório: ~/.next

![Untitled%202.png](/public/Untitled%202.png)

Para rodar o pacote gerado é necessário acessar a pasta do projeto e executar o comando

```bash
npm run start
```

---

### LANÇAMENTO DAVERSÃO 10.1

Lançamento oficial da nova versão foi em 29/03/2021

- 3x mais rápido que a versão 10.
- Mais de 1.540 colaboradores independentes atuaram no projeto.
- Projeto totalmente público no GitHub.
- Pronto para escalabilidade
- Provedor agnóstico para os maiores sistema de comércio eletrônico do mundo, como Shopify por exemplo.

---

### BIBLIOTECA NEXTRA

É uma biblioteca feita em NEXTJS que já está integrada a VERCEL, empresa criadora do Next.JS.

Ela faz a exibição de arquivos markdown (.md) e .mdx que estão no diretório ~/pages/doc da aplicação.

Arquivos .mdx são arquivos .md que permitem a adição de JS, geralmente com bibliotecas como React entre outras.

[Components | MDX](https://mdxjs.com/advanced/components)

Ela faz todo o roteamento, navegação e exibição da aplicação.

Basta alimentar com os conteúdos e a visualização será feita.

### CRIANDO UM PROJETO COM A FERRAMENTA NEXTRA

- Documentação Nextra

[Nextra: Next.js static site generator](https://nextra.vercel.app/docs/get-started)

### PROJETO DA FÁCIL NO GITHUB

[desenvolvimentoFacil/meetups](https://github.com/desenvolvimentoFacil/meetups)

- Estrutura do projeto

    **./root** 

    - **next.config.js**

        → Esse arquivo faz as configurações iniciais da ferramenta, definindo qual arquivo deve utilizar para controlar o tema da aplicação.

    - **theme.config.js**

        → Esse arquivo faz o controle do tema da aplicação. Definindo coisas como:
        - Identidade visual
        - Tipografia
        - Titulo da Navbar
        - Opções de responsividade/portabilidade
        - Logotipo e todos os ícones
        - Rodapé

    - **Pasta public**
    → Dentro dessa pasta ficam todos os "resources" da aplicação. No geral todo tipo de imagem que é utilizado como ícone ou até mesmo imagens de conteúdo do site.

        → No momento em que o build da aplicação é feito, a plataforma processa todos os arquivos dessa pasta otimizando ao máximo esses arquivos, inclusive, adaptando para se adequar a todos os viewport necessários.

    - **Pasta pages**

        → Todas as "páginas" desenvolvidas sobre a ferramenta NextJS ficam, obrigatoriamente no diretório ~/pages. Nesse caso, como estamos utilizando a biblioteca Nextra, as páginas são feitas em arquivos .md ou .mdx.

        → meta.json
        Esse arquivo define a ordem dos itens que serão exibidos na navegação.

        É ele quem define como funciona a navegação entre as páginas.

        É um JSON aonde o nome da propriedade deve ser o mesmo nome do arquivo, o valor da propriedade é a legenda que será exibida na página.

        → index.md
        Esse é o "EntryPoint" da ferramenta. É a página configurada para ser exibida primeiro.

        Ao acessar o site, essa página será exibida.

- Sempre que um Meetup for apresentado, deverá ser criado um arquivo .mdx na pasta ~/pages/doc/Nome meetup

---

### PUBLICANDO A APLICAÇÃO NA VERCEL

- A vercel é a empresa que criou, mantém e estimula a comunidade NEXT.JS.
- Ela criou um ambiente de publicação de aplicações totalmente voltado para o Next.

[Develop. Preview. Ship. For the best frontend teams - Vercel](https://vercel.com/)

- Upload do sistema é todo baseado no sistema Git
    - Possuí integração com GitHub, GitLabs e as principais plataformas do mercado
- Custo de hospedagem zero - até determinada quantidade de requisições

Comecei fazendo o Deploy para produção. A Vercel é bem intuitiva e bastou meia dúzia de cliques e já tinha um site pronto e um repositório pronto no github.

[Nextra: Next.js static site generator](https://facilmeetups.vercel.app/)

Devido ao conteúdo e direitos de imagem dos participantes não é podemos hospedar publicamente o painel. Ele foi exibido somente no momento da apresentação e excluído após a apresentação. Deve-se utilizar somente o endereço interno.

---

### Links de interesse

Explicando SSG x SSR

[](https://betterprogramming.pub/server-side-rendering-vs-static-site-generation-53a34872728c)

Next.JS mecânica hibrida

[Basic Features: Data Fetching | Next.js](https://nextjs.org/docs/basic-features/data-fetching)

Nextra

[shuding/nextra](https://github.com/shuding/nextra)

Boilerplates:

- MaterialUI:

[NextJS Material Kit by Creative Tim](https://demos.creative-tim.com/nextjs-material-kit/documentation/tutorial)

- e-commerce:

[Next.js Commerce](https://nextjs.org/commerce)

- Vários templates:

[15 Free React Templates for Your Next Project](https://dev.to/exwhyzed/15-free-reactjs-templates-for-your-next-project-313m)

---

### SE DER TEMPO...

Vamos fazer uma liberação na plataforma Vercel..

1 - Mostrar o e-commerce criado com a ferramenta ecommerce da Vercel desenvolvido com Next.JS

[ACME Storefront | Powered by Next.js Commerce - ACME Storefront](https://commerce-phi-sable-33.vercel.app/)

2 - Acessar o blog

3 - Alterar o conteúdo loremIpsum do site pelo conteúdo do Mussum Ipsum

[Mussum Ipsum - O melhor lorem ipsum do mundis](https://mussumipsum.com/)

→ Gerar 4 parágrafos

→ Alterar o texto

→ Fazer o commit

→ Verificar o comportamento do site