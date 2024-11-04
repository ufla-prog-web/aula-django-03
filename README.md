# Aula Django 03 - Sistema para Portal Biblioteca

<p align="center">
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Python-brightgreen.svg" alt="Aula Python">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Django-blue.svg" alt="Aula Django">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Portal_Biblioteca-orange.svg" alt="Aula Portal Biblioteca">
  </a>
</p>

## Índice

* [Introdução](#introdução)
* [Recursos Utilizados](#recursos-utilizados)
* [Fundamentos Teóricos](#fundamentos-teóricos)
* [Objetivo da Aula](#objetivo-da-aula)
* [Desenvolvimento do Projeto](#desenvolvimento-do-projeto)
* [Créditos e Referências](#créditos-e-referências)

## Introdução

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

Aula Django 03. Projeto utilizando o Django para ser desenvolvido na Aula de GAC116 - Programação Web. Essa aula é uma continuação da Aula Django 02.

O objetivo desse projeto é criar um sistema para gestão de biblioteca.

Este tutorial foi elaborado baseado no tutorial disponível no [curso de django da w3schools](https://www.w3schools.com/django/index.php) e também baseado na [documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/).

A aula está estruturada em forma de tutorial, de forma que cada estudante vá replicando em seu computador os conceitos e recursos aqui mostrados. A aula mostra a evolução do código/solução para que os estudantes possam compreender como as diferentes tecnologias se conectam.

## Recursos Utilizados

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

A seguir estão listados os principais recursos utilizados no desenvolvimento desta aula.

### Linguagens

* Python - Linguagem de Programação Principal
    * [link do site python](https://www.python.org/)
    * [link do curso da w3schools](https://www.w3schools.com/python/default.asp)
* HTML - Estrutura da Página Web
    * [link do curso da w3schools](https://www.w3schools.com/html/default.asp)
* CSS - Apresentação da Página Web
    * [link do curso da w3schools](https://www.w3schools.com/css/default.asp)
* JavaScript - Comportamento da Página Web
    * [link do curso da w3schools](https://www.w3schools.com/js/default.asp)
* SQL - Linguagem para Consultas no Banco de Dados
  * [link do curso da w3schools](https://www.w3schools.com/sql/default.asp)

### Framework

* Django - Framework Web
    * [link do site do django](https://www.djangoproject.com/)
    * [link do curso da w3schools](https://www.w3schools.com/django/index.php)
* Bootstrap - Framework CSS
    * [link do site do bootstrap](https://getbootstrap.com/)
    * [link do curso da w3schools](https://www.w3schools.com/bootstrap5/index.php)

### Bibliotecas

* Jinja - Biblioteca Python para Templates
    * [link do site do jinja](https://jinja.palletsprojects.com/en/3.1.x/)
* Chart.js - Biblioteca JavaScript para Gráficos
    * [link do site do chart.js](https://www.chartjs.org/)
* FontAwesome - Biblioteca CSS para Ícones
     * [link do site do fontawesome](https://fontawesome.com/)
* WhiteNoise - Biblioteca Python para Servir Arquivos Estáticos
    * [link do site do whitenoise](https://whitenoise.readthedocs.io/)

### Ferramentas

* Git - Sistema de Controle de Versão - [link](https://git-scm.com/)
* Github - Plataforma de Hospedagem de Códigos - [link](https://github.com/)
* Visual Studio Code - IDE - [link](https://code.visualstudio.com/)
* Pip - Gerenciador de Pacotes do Python - [link](https://pypi.org/project/pip/)
* Venv - Ambiente Virtual do Python - [link](https://docs.python.org/pt-br/3/library/venv.html)
* SQLite Online - SGBD - [link](https://sqliteonline.com/)
* DB Browser for SQLite - SGBD - [link](https://sqlitebrowser.org/)

## Fundamentos Teóricos

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

A seguir estão destacados alguns dos principais fundamentos teóricos para entendimento desse tutorial.

### Características do Django

**1. Framework completo:** Django oferece tudo o que é necessário para o desenvolvimento de uma aplicação web, incluindo roteamento de URLs, mapeamento objeto-relacional (ORM), sistema de templates, autenticação, etc.

**2. Administração automática:** Com base nos modelos definidos, Django gera automaticamente uma interface administrativa poderosa e personalizável, economizando tempo no desenvolvimento de funcionalidades administrativas.

**3. ORM (Object-Relational Mapping):** O Django possui um ORM que facilita a interação com bancos de dados relacionais, permitindo que os desenvolvedores escrevam consultas em Python ao invés de SQL.

**4. Sistema de templates:** Django possui um sistema de templates eficiente que permite criar HTML dinâmico de forma organizada, utilizando lógica básica como laços e condicionais.

**5. Segurança embutida:** O Django se preocupa com a segurança, oferecendo proteção contra ataques comuns como SQL Injection, Cross-site Scripting (XSS), Cross-site Request Forgery (CSRF), e Clickjacking.

**6. Escalabilidade:** Django é altamente escalável, podendo lidar com grandes volumes de tráfego, como em sites populares que utilizam o framework (por exemplo, Instagram e Pinterest).

**7. Comunidade ativa e documentação:** Django conta com uma ampla comunidade de desenvolvedores e uma documentação completa e detalhada, facilitando a resolução de problemas e o aprendizado.

**8. Reutilização de código:** Django promove a reutilização de componentes por meio de pacotes chamados "apps". Cada app é modular e pode ser usado em diferentes projetos ou em diferentes partes da mesma aplicação.

**9. Suporte a várias bases de dados:** O Django suporta diferentes sistemas de banco de dados, como PostgreSQL, MySQL, SQLite e Oracle, tornando-o flexível para diversos ambientes.

**10. Testes integrados:** O Django tem suporte nativo para testes automatizados, permitindo que desenvolvedores escrevam e executem testes facilmente para garantir a qualidade do código.

### Arquitetura Web de Três Camadas

A arquitetura web de três camadas é um padrão de design de software que organiza uma aplicação em três níveis distintos, cada um com responsabilidades bem definidas. Essas camadas são:

**1. Camada de Apresentação (Frontend)**:

* Também chamada de interface de usuário, essa camada é responsável pela interação com o usuário. Ela inclui tudo o que o usuário vê e utiliza para interagir com o sistema, como páginas web, formulários, botões, e elementos visuais em geral.
* Aqui, são usados tecnologias como HTML, CSS, JavaScript e frameworks frontend (React, Angular, etc.).
* A camada de apresentação envia as entradas dos usuários para a camada de negócios e exibe os resultados de volta para o usuário.

**2. Camada de Negócios (Lógica da Aplicação - Backend)**:

* Nessa camada está a lógica de negócios da aplicação, ou seja, as regras que governam como os dados devem ser processados e as operações que devem ser realizadas. Ela trata os pedidos recebidos da camada de apresentação e executa as operações necessárias.
* Essa camada pode incluir validações, cálculos e chamadas ao banco de dados. Em termos de tecnologia, é geralmente desenvolvida com linguagens de programação como Python, Java, PHP, ou frameworks como Django, Spring Boot, Laravel, etc.

**3. Camada de Dados (Banco de Dados - Backend)**:

* A camada de dados gerencia o armazenamento e recuperação de dados em um banco de dados. Ela é responsável pela persistência dos dados e operações como criar, ler, atualizar e deletar (CRUD).
* Geralmente, são usados sistemas de gerenciamento de banco de dados relacionais (como MySQL, PostgreSQL) ou não relacionais (como MongoDB).
* A camada de negócios interage com essa camada para armazenar e buscar dados conforme necessário.

**Fluxo da Arquitetura de Três Camadas**:

* O usuário interage com a Camada de Apresentação.
* A Camada de Apresentação faz requisições para a Camada de Negócios.
* A Camada de Negócios processa a lógica e, se necessário, interage com a Camada de Dados.
* A Camada de Dados responde com os dados necessários para a Camada de Negócios.
* A Camada de Negócios retorna os resultados processados para a Camada de Apresentação.
* A Camada de Apresentação exibe os resultados para o usuário.

Essa separação facilita a manutenção e escalabilidade da aplicação, permitindo que cada camada possa ser modificada ou melhorada de forma independente.

![Arquitetura das Aplicações Web](./docs/arquitetura-web.png)

### Arquitetura MVT do Django

O modelo MVT (Model-View-Template) é uma arquitetura usada no framework Django para desenvolvimento de aplicações web. Ele organiza a aplicação em três componentes principais:

* **Model (Modelo)**: Responsável pela definição da estrutura dos dados e a interação com o banco de dados. Ele define as classes que representam as tabelas e seus relacionamentos, além de métodos para realizar consultas e operações nos dados.

* **View (Visão)**: Contém a lógica da aplicação. A view recebe as requisições dos usuários, processa os dados (geralmente acessando o Model), e retorna uma resposta, como uma página HTML renderizada ou dados em formato JSON.

* **Template (Apresentação)**: É a camada de apresentação, onde o conteúdo dinâmico gerado pela View é inserido em arquivos HTML. Os templates permitem a separação da lógica de negócio da interface de usuário, tornando o código mais organizado.

Diferente do padrão MVC, onde o controller gerencia a lógica de controle, no Django, a função das views cumpre esse papel, enquanto os templates gerenciam a apresentação.

A figura abaixo detalha os componentes descritos acima.

![Arquitetura MVT - Geral](./docs/mvt-1.png)

No modelo MVT do Django, as requisições seguem um fluxo bem definido, onde cada componente (Model, View, Template) desempenha um papel específico no processamento e resposta de uma requisição HTTP. O fluxo funciona da seguinte forma:

* **Recebimento da Requisição (HTTP Request)**: Quando um usuário acessa uma URL no navegador, o Django recebe a requisição HTTP correspondente. Esse processo começa no URL *dispatcher* (mapeador de URLs), que verifica qual view deve ser chamada com base na URL requisitada.

* **View (Visão)**: A View é o ponto de entrada para o processamento da requisição. A função ou classe associada à URL recebida é executada. Ela é responsável por: Receber a requisição do usuário; Executar a lógica necessária, que pode incluir validações, processamento de dados, ou interações com o banco de dados através dos Models; e Retornar uma resposta apropriada.

* **Model (Modelo)**: Se a View precisar acessar ou manipular dados, ela fará isso por meio do Model. O Model contém a lógica de negócios relacionada à persistência de dados, permitindo a View realizar operações como criar, ler, atualizar ou deletar registros no banco de dados.

* **Template (Apresentação)**: Após processar os dados, a View geralmente prepara um contexto (um dicionário de dados) e passa esse contexto para o Template. O Template é um arquivo HTML com marcações especiais do Django que permitem a inserção de dados dinâmicos. O Template renderiza esses dados em uma estrutura HTML, exibindo o conteúdo adequado com base nas informações passadas pela View.

* **Resposta (HTTP Response)**: Depois que o Template é renderizado, a View retorna uma resposta HTTP (normalmente uma página HTML ou dados JSON em APIs) ao navegador ou cliente. Essa resposta contém o conteúdo processado e visualizado pelo usuário.

A figura abaixo detalha o fluxo descrito acima.

![Arquitetura MVT - Requisição](./docs/mvt-2.png)

A figura abaixo detalha ainda mais a arquitetura MVT e as tecnologias envolvidas.

![Arquitetura MVT - Detalhes](./docs/mvt-3.png)

### Modelo ORM

O Django suporta o conceito de Mapeamento Objeto-Relacional (ORM). Através do ORM você define a modelagem de dados através de classes em Python. Com isso é possível gerar suas tabelas no banco de dados e manipulá-las sem necessidade de utilizar SQL (o que também é possível). Os registros de cada tabela são representados como instâncias das classes correspondentes.

## Objetivo da Aula

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

A animação abaixo mostra de forma visual o resultado esperado nesta aula.

![Sistema Objetivo da Aula](./docs/objetivo.gif)

## Desenvolvimento do Projeto

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

Os passos a seguir devem ser seguidos para alcançar o objetivo da aula.

### Clonando o Repositório

Inicialmente, clone o repositório da seguinte forma:

```bash
git clone https://github.com/ufla-prog-web/aula-django-03.git
```

### Baixando o Repositório

Caso deseje ao invês de clonar o repositório (método acima), baixe o repositório do [link](https://github.com/ufla-prog-web/aula-django-03) clicando em `Code` e `Download ZIP`.

### Abrindo o Visual Studio Code

Abra a IDE Visual Studio Code na pasta `aula-django-03`.

**Dica:** Abra o arquivo `README.md` e clique em `Open Preview to the Side` para facilitar a construção da aplicação.

**Dica:** Abra um terminal utilizando a IDE clicando em `Terminal` e `New Terminal`.

### Navegando até a Pasta do Projeto

Em seguida, navegue até a pasta do projeto (`portal_biblioteca`) dentro da pasta baixada do github (`aula-django-03`):

```bash
cd aula-django-03/
cd portal_biblioteca/
```

### Criando o Ambiente Virtual

Crie o ambiente virtual (venv) para isolar as instalações/dependências do Python:

Unix/macOS

```bash
python3 -m venv venv
```

Windows

```bash
py -m venv venv
```

**OBS:** no comando acima, o segundo nome `venv` é o nome que escolhemos para o nosso ambiente virtual (isso pode ser alterado).

### Ativando o Ambiente Virtual

Ative o ambiente virtual (venv) no seu computador utilizando o comando abaixo:

**Sistema Operacional:** Unix/Mac OS:

```bash
source venv/bin/activate
```

**Sistema Operacional:** Windows

```bash
Set-ExecutionPolicy Unrestricted -Scope Process
venv\Scripts\activate.bat
```

Quando desejar sair do ambiente virtual, basta digitar:

```bash
deactivate
```

### Fluxo de Trabalho no Django

A seguir é apresentado um fluxo de trabalho que pode ser seguido durante o desenvolvimento de um projeto utilizando o Django.

[![](https://mermaid.ink/img/pako:eNqN1E1y2yAUB_CrMHThTVLvveiMbcnfX9Nm0UTKgkrPDikCFZBTNxPfJaseoNMT-GJ9Qq5DNSyqlfjzAwF6wzPNVA60R7dCPWUPTFtyE6WS4NNPUjqVxjLBTj9Pv8GQFWRgzOlVc2ZSek-urz-QAaohBppstHoEq4hUJHpkcqeQNDMNnBxeZL8sA2roVJR0U9q3FRP8B9KOAWu53Jn35aGT0jQ948jhuIUL3Is40-5Zxk6Oaum-3n3zN1CUglkwb3rk9Dik-_pbxffKkNjY06vlmfLGjd24SWs9ew5PreVMHJyGPtCpdHvxU6dnrWlZXnDZOpCZk_P_O725w4sax98hq2xtMyUEZBZ_OO7N1wunl__qgn2Fgu80YiWNz5eOr1rcUfDdyrl14jNdSQN6D7pzKYu1YxtkfYnbMsg-gqmEZbmrtRXbww7ftRvRjNk0Bec3Ir8R-42R3xj7jYnfmNaTN8HnZP1F8x2zp1-aq3tyPB7JbdJdlxmeBRN_f95t3XGHecaM63Bbb_qMPQhAseVC9N6NooEfx-F4FI7H4XgSjqft2O-8u3RGfhyF41k4nofjRThehuOVH9MrWoAuGM_xonquWUrtAxSQ0h6-5rBlWA9YWvIFKaus-nSQGe1ZXcEVrcocKy_iDCuwoL0tEwZTyLlVetlcfu4OfPkDBV6NXw?type=png)](https://mermaid.live/edit#pako:eNqN1E1y2yAUB_CrMHThTVLvveiMbcnfX9Nm0UTKgkrPDikCFZBTNxPfJaseoNMT-GJ9Qq5DNSyqlfjzAwF6wzPNVA60R7dCPWUPTFtyE6WS4NNPUjqVxjLBTj9Pv8GQFWRgzOlVc2ZSek-urz-QAaohBppstHoEq4hUJHpkcqeQNDMNnBxeZL8sA2roVJR0U9q3FRP8B9KOAWu53Jn35aGT0jQ948jhuIUL3Is40-5Zxk6Oaum-3n3zN1CUglkwb3rk9Dik-_pbxffKkNjY06vlmfLGjd24SWs9ew5PreVMHJyGPtCpdHvxU6dnrWlZXnDZOpCZk_P_O725w4sax98hq2xtMyUEZBZ_OO7N1wunl__qgn2Fgu80YiWNz5eOr1rcUfDdyrl14jNdSQN6D7pzKYu1YxtkfYnbMsg-gqmEZbmrtRXbww7ftRvRjNk0Bec3Ir8R-42R3xj7jYnfmNaTN8HnZP1F8x2zp1-aq3tyPB7JbdJdlxmeBRN_f95t3XGHecaM63Bbb_qMPQhAseVC9N6NooEfx-F4FI7H4XgSjqft2O-8u3RGfhyF41k4nofjRThehuOVH9MrWoAuGM_xonquWUrtAxSQ0h6-5rBlWA9YWvIFKaus-nSQGe1ZXcEVrcocKy_iDCuwoL0tEwZTyLlVetlcfu4OfPkDBV6NXw)

### Instalando o Django

Instale o django dentro do ambiente virtual criado (testado na versão 5.0.3):

```bash
pip3 install django
```

ou

```bash
python -m pip install Django
```

Verifique a versão instalada do django (para ter certeza que tudo ocorreu bem):

```bash
django-admin --version
```

ou

```bash
python3 -m django --version
```

**OBS:** Caso o terminal não encontre o django-admin, execute o seguinte comando (utilizado geralmente quando não se utiliza o venv no laboratório DCC07):

```bash
export PATH=$PATH:~/.local/bin
```

### Executando o Projeto

Antes de executar o projeto, execute o comando para fazer as migrações:

```bash
python3 manage.py migrate
```

Uma saída semelhante a essa deverá ser exibida:

```bash
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  No migrations to apply.
```

Em seguida, execute comando abaixo para fazer a cópia dos arquivos estáticos:

```bash
python3 manage.py collectstatic
```

Uma saída semelhante a essa deverá ser exibida:

```bash
130 static files copied to '/media/jesimar/Workspace/Work3/1-Github/2-ufla-prog-web/aula-django-03/portal_biblioteca3/productionfiles'.
```

Inicie a execução do projeto django criado:

```bash
python3 manage.py runserver
```

**OBS:** Por padrão, o servidor de desenvolvimento escuta na porta 8000, mas você pode especificar uma porta diferente como argumento opcional, por exemplo, `python3 manage.py runserver 8081`.

Acesse através do navegdor web a página [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

A aula anterior avançou até aqui.

### Melhorando a Aparência do Projeto com Bootstrap

Agora, iremos melhorar a aparência do nosso sistema utilizando o framework Bootstrap. Além de deixar a página mais bonita o Bootstrap a torna responsiva, se corretamente utilizado. Caso tenha dúvidas em como funciona o Bootstrap consulte a [documentação oficial](https://getbootstrap.com/docs/5.3/getting-started/introduction/) ou o [curso da w3schools](https://www.w3schools.com/bootstrap5/index.php).

Para incorporar o bootstrap no nosso sistema primeiro, atualize o arquivo `base.html` da pasta `biblioteca` e subpasta `templates` conforme código abaixo:

```html
{% load static %}
<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>{% block titulo %}{% endblock %}</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
        <link rel="stylesheet" href="{% static 'mystyles.css' %}">
    </head>
    <body>
        <header>
            <nav class="navbar navbar-expand-lg navbar-dark">
                <div class="container-fluid">
                    <a class="navbar-brand" href="/">Portal Biblioteca</a>
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav">
                            <li class="nav-item">
                                <a class="nav-link active" href="/">Principal</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/livros">Livros</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/tccs">TCCs</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/dashboard">Dashboard</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/auth/login">Login</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/auth/cadastro">Cadastre-se</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/auth/logout">Logout</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/admin">Admin</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </nav>
        </header>

        {% block conteudo %}
        {% endblock %}

        <footer class="text-white text-center p-3 mt-5">
            <p>&copy; Portal Biblioteca. Todos os direitos reservados.</p>
        </footer>

        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    </body>
</html>
```

Comentários sobre as alterações relacionadas ao Bootstrap: 

1. Linha de Importação do CSS do Bootstrap:

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
```

Esta linha importa o CSS do Bootstrap da versão 5.3.3 via CDN, o que aplica automaticamente os estilos do Bootstrap em toda a página, possibilitando o uso de classes CSS prontas para layout e formatação.

2. Elementos com Classes do Bootstrap:

* `<nav class="navbar navbar-expand-lg navbar-dark">`:

    * `navbar`: Aplica o estilo básico de uma barra de navegação.
    * `navbar-expand-lg`: Faz a barra de navegação ser expansível (colapsável) em telas menores, exibindo todos os itens em telas grandes.
    * `navbar-dark`: Aplica cores para a navbar que são apropriadas para fundos escuros.

* `<div class="container-fluid">`:

    * `container-fluid`: Define um contêiner que ocupa toda a largura disponível, mantendo uma estrutura fluida e adaptável ao tamanho da tela.

* `<a class="navbar-brand" href="/">Portal Biblioteca</a>`:

    * `navbar-brand`: Aplica estilo a um elemento de marca (logo ou nome) na navbar, deixando-o em evidência.

* `<button class="navbar-toggler"`:
    
    * `navbar-toggler`: Define um botão de colapso para a navbar em telas pequenas.
    * `data-bs-toggle="collapse"` e `data-bs-target="#navbarNav"`: Atributos data usados pelo JavaScript do Bootstrap para controlar o comportamento de colapso.

* `<span class="navbar-toggler-icon"></span>`:

    * `navbar-toggler-icon`: Exibe o ícone de "hambúrguer", indicando que a navbar é expansível em dispositivos móveis.

* `<div class="collapse navbar-collapse" id="navbarNav">`:

    * `collapse`: Define que este conteúdo é colapsável.
    * `navbar-collapse`: Estilo específico para o colapso em uma barra de navegação.
    * `id="navbarNav"`: Identificador usado para associar o botão navbar-toggler a este conteúdo colapsável.

* `<ul class="navbar-nav">`:

    * `navbar-nav`: Aplica estilos para agrupar itens de navegação dentro da navbar.

* `<li class="nav-item">`:

    * `nav-item`: Aplica estilos a um item de navegação individual dentro da lista de navegação (`<ul>`).

* `<a class="nav-link active" href="/">`:

    * `nav-link`: Estilo padrão para um link de navegação dentro da navbar.
    * `active`: Estilo que destaca o link atualmente ativo.

* `<img src="{% static 'img_avatar.png' %}" alt="Avatar" style="width:40px;" class="rounded-pill">`:

    * `rounded-pill`: Aplica um estilo de borda arredondada na imagem do avatar.

3. Footer com Classes do Bootstrap:

* `<footer class="text-white text-center p-3 mt-5">`

    * `text-white`: Define o texto em branco.
    * `text-center`: Centraliza o conteúdo do footer.
    * `p-3`: Aplica padding de 3 unidades em todas as direções.
    * `mt-5`: Aplica uma margem superior de 5 unidades, criando espaço entre o conteúdo acima e o footer.

4. Importação do JavaScript do Bootstrap:

```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

Essa linha importa o JavaScript do Bootstrap, essencial para os componentes interativos, como o botão de colapso da navbar e outros elementos interativos da interface.

Em seguida, altere o código do arquivo `principal.html` para o código abaixo:

```html
{% extends "base.html" %}

{% load static %}

{% block titulo %}
    Portal Biblioteca
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <h1>Portal Biblioteca</h1>
        <h4>Bem-vindo ao Portal da Biblioteca</h4>
        <p>Explore nosso acervo de Livros e TCCs, veja seus dashboards e entre na sua conta para mais funcionalidades.</p>
        <br>
        <center>
            <img src="{% static 'logo-portal.png' %}" alt="logo-portal" width="400" height="300">
        </center>
    </main>
{% endblock %}
```

Em seguida, altere o código do arquivo `livros.html` para o código abaixo:

```html
{% extends "base.html" %}

{% block titulo %}
    Portal Biblioteca - Livros
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <h1>Livros</h1>
        {% for l in livros %}
            <div class="card">
                <div class="card-header card-title-obra">
                    <em>Livro:</em> {{ l.nome }}
                </div>
                <div class="card-body">
                    <p class="card-title"><em>Autor:</em> {{ l.autor }}</p>
                    <p class="card-title"><em>Ano:</em> {{ l.ano }}</p>
                </div>
            </div>
            <br>
        {% endfor %}
        <br>
        <br>
        <br>
    </main>
{% endblock %}
```

Em seguida, altere o código do arquivo `tccs.html` para o código abaixo:

```html
{% extends "base.html" %}

{% block titulo %}
    Portal Biblioteca - TCCs
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <h1>Trabalhos de Conclusão de Curso</h1>
        {% for tcc in tccs %}
            <div class="card">
                <div class="card-header card-title-obra">
                    <em>Título:</em> {{ tcc.titulo }}
                </div>
                <div class="card-body">
                    <p class="card-title"><em>Autor:</em> {{ tcc.autor }}</p>
                    <center><a href="tccs/detalhes/{{ tcc.id }}" class="btn btn-primary">Ver Detalhes</a></center>
                </div>
            </div>
            <br>
        {% endfor %}
        <br>
        <br>
        <br>
    </main>
{% endblock %}
```

Em seguida, altere o código do arquivo `tcc_detalhes.html` para o código abaixo:

```html
{% extends "base.html" %}

{% block titulo %}
    Portal Biblioteca - TCC - Detalhes
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <h1>Trabalho de Conclusão de Curso - Detalhes</h1>
        <div class="card">
            <div class="card-header card-title-obra">
                <em>Título:</em> {{ tcc.titulo }}
            </div>
            <div class="card-body">
                <p class="card-title"><em>Autor:</em> {{ tcc.autor }}</p>
                <p class="card-title"><em>Orientador:</em> {{ tcc.orientador }}</p>
                <p class="card-title"><em>Ano:</em> {{ tcc.ano }}</p>
            </div>
        </div>
        <br>
        <center><a href="/tccs" class="btn btn-primary">Voltar</a></center>
    </main>
{% endblock %}
```

Em seguida, altere o código do arquivo `dashboard.html` para o código abaixo:

```html
{% extends "base.html" %}

{% load static %}

{% block titulo %}
    Portal Biblioteca - Dashboard
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <h1>Dashboard</h1>
        <p>Visualize aqui os gráficos e informações de dados do Portal Biblioteca.</p>
        <div class="row">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">Dashboard 1</h5>
                        <p class="card-text">Informações sobre o número de obras por categoria em gráfico de barras.</p>                        
                        <div class="chart-container" style="position: relative; height:40vh;">
                            <canvas id="graficoNumVolumes"></canvas>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">Dashboard 2</h5>
                        <p class="card-text">Informações sobre o número de obras por categoria em gráfico de pizza.</p>
                        <div class="chart-container" style="position: relative; height:40vh;">
                            <canvas id="graficoPizza"></canvas>
                        </div>
                        
                    </div>
                </div>
            </div>
        </div>
    </main>

    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="{% static 'myscripts.js' %}"></script>
{% endblock %}
```

Por fim, altere o código do arquivo `mystyles.css` para o código abaixo:

```css
body {
  font-family: Arial, sans-serif;
}

h1 {
  color: #343a40;
}

header {
  background-color: #4D70EF;
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #4D70EF;
}

.card:hover {
  transform: scale(1.02);
}

.card-title-obra {
  background-color: #375BDC;
  color: white;
}
```

Em seguida, execute o seguinte comando abaixo:

```bash
python3 manage.py collectstatic
```

Em seguida, execute o servidor com este comando:

```bash
python3 manage.py runserver
```

Por fim, acesse o endereço [http://127.0.0.1:8000](http://127.0.0.1:8000) e análise a nova interface do sistema.

**OBS**: Caso a página não seja exibida corretamente tente apagar o histórico de navegação para limpar a cache.

### Melhorando a Aparência do Projeto com FontAwesome

Agora, iremos melhorar a aparência do nosso sistema utilizando os ícones da biblioteca CSS [FontAwesome](https://fontawesome.com/). Caso tenha dúvidas em como funciona essa biblioteca, consulte a [página oficial do FontAwesome](https://fontawesome.com/).

Para incorporar o FontAwesome no nosso sistema primeiro, atualize o arquivo `base.html` da pasta `biblioteca` e subpasta `templates` conforme código abaixo:

```html
{% load static %}
<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>{% block titulo %}{% endblock %}</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
        <link rel="stylesheet" href="{% static 'mystyles.css' %}">
    </head>
    <body>
        <header>            
            <nav class="navbar navbar-expand-lg navbar-dark">
                <div class="container-fluid">
                    <a class="navbar-brand" href="/">Portal Biblioteca</a>
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav">
                            <li class="nav-item">
                                <a class="nav-link active" href="/"><i class="fas fa-home"></i> Principal</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/livros"><i class="fas fa-book"></i> Livros</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/tccs"><i class="fas fa-graduation-cap"></i> TCCs</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/dashboard"><i class="fas fa-chart-line"></i> Dashboard</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/auth/login"><i class="fas fa-sign-in-alt"></i> Login</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/auth/cadastro"><i class="fas fa-user-plus"></i> Cadastre-se</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/auth/logout"><i class="fas fa-sign-out-alt"></i> Logout</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active" href="/admin"><i class="fa-solid fa-lock"></i> Admin</a>
                            </li>
                        </ul>
                    </div>                    
                </div>
            </nav>
        </header>

        {% block conteudo %}
        {% endblock %}

        <footer class="text-white text-center p-3 mt-5">
            <p>&copy; Portal Biblioteca. Todos os direitos reservados.</p>
        </footer>

        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    </body>
</html>
```

A seguir temos algumas explicações sobre as alterações no código HTML:

* `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">`: Adiciona o link para a CDN pública do Font Awesome, na versão 6.0.0-beta3. Com essa linha no `<head>`, você poderá utilizar os ícones sem precisar baixar a biblioteca localmente ou criar um kit.
* `<i class="fas fa-home"></i>`: inclui o ícone de "casa" com a classe `fa-home`. A classe `fas` define que é um ícone sólido (do inglês, "Font Awesome Solid").

**OBS:** Recomendamos criar uma conta no Font Awesome e criar um kit no desenvolvimento da sua plataforma web, ou seja, não utilize a CDN pública sugerida em seu projeto final.

Em seguida, execute a aplicação.

```bash
python3 manage.py runserver
```

Para mais informações sobre o FontAwesome, consulte o [link](https://docs.fontawesome.com/web/setup/get-started) ou faça o [curso da w3schools](https://www.w3schools.com/icons/fontawesome5_intro.asp).

### Criando o Primeiro Modelo no Django

Até esse momento fizemos a nossa aplicação web com a interface de usuário, com URLs e algum processamento, mas não trabalhamos com Banco de Dados. Os dados estavam inseridos diretamente no código.

Agora, iremos criar o nosso modelo para representar Livros e TCCs no Banco de Dados SQLite disponível no Django. No Django, os dados são criados em objetos, chamados Modelos, que na verdade, são tabelas em um banco de dados.

Esse mapeamento entre objetos e tabelas é feito através do ORM (*Object-Relational Mapping*). ORM é uma técnica de programação que permite aos desenvolvedores de software manipular e acessar dados do BD usando objetos da linguagem de programação, em vez de escrever consultas SQL diretamente. Com o ORM, os desenvolvedores podem interagir com o banco de dados utilizando operações em objetos, métodos e propriedades, sem precisar se preocupar com os detalhes específicos do banco de dados subjacente. O ORM mapeia os objetos da aplicação para as tabelas do banco de dados, e vice-versa, facilitando o trabalho com dados de banco de dados em um ambiente de programação orientado a objetos.

Em um framework como Django, o ORM é uma parte fundamental. Ele permite que os desenvolvedores definam modelos de dados (classes Python) que representam as tabelas do banco de dados. Esses modelos incluem campos que representam as colunas do banco de dados e métodos que definem o comportamento dos objetos. O ORM traduz as operações realizadas nos objetos (como salvar, atualizar, excluir) em instruções SQL apropriadas para interagir com o banco de dados.

Usando o ORM, os desenvolvedores podem escrever código mais legível, portátil e seguro, pois não precisam lidar diretamente com SQL. Além disso, o ORM facilita a migração entre diferentes sistemas de gerenciamento de banco de dados (como PostgreSQL, MySQL, SQLite) sem a necessidade de alterações significativas no código da aplicação.

![Modelo ORM do Django](./docs/orm.png)

Fonte: [https://medium.com/@mochammadagusyahya](https://medium.com/@mochammadagusyahya/mastering-data-magic-unleashing-the-power-of-django-orm-in-your-web-development-journey-62fa851bf49a)

Primeiramente, iremos criar uma classe chamada `Livro`. Para isso, abra o arquivo `models.py` na pasta `biblioteca` e digite o seguinte conteúdo:

```python
from django.db import models

class Livro(models.Model):
    nome = models.CharField(max_length=255)
    autor = models.CharField(max_length=255)
    ano = models.IntegerField()
```

O código acima irá criar uma Tabela chamada Livro no BD SQLite. Os campos `nome` e `autor` são campos de texto e estão configurados para ter no máximo 255 caracteres. O campo `ano` é um campo numérico inteiro.

OBS: Quando criamos o projeto Django, obtivemos um banco de dados SQLite vazio. Ele estava na raiz da pasta `portal_biblioteca` e possui o nome de arquivo `db.sqlite3`. Por padrão, todos os modelos criados no projeto Django serão criados como tabelas neste banco de dados.

Em seguida, execute o código abaixo para que seja criado a tabela Livro no banco de dados de fato:

```bash
python3 manage.py makemigrations biblioteca
```

**OBS:** Após definir os modelos, você cria migrações com este comando. Isso cria arquivos de migração que descrevem como o banco de dados deve ser modificado para refletir as alterações nos modelos.

O que resultará nesta saída:

```bash
Migrations for 'biblioteca':
  biblioteca/migrations/0001_initial.py
    - Create model Livro
```

O Django cria um arquivo descrevendo as alterações e armazena o arquivo na pasta `/biblioteca/migrations/` com nome `0001_initial.py`. Abra esse arquivo para analisar o conteúdo. Observe que o Django insere um campo `id` para suas tabelas, que é um número auto incrementado.

A tabela ainda não foi criada, você terá que executar mais um comando, então o Django criará e executará uma instrução SQL, baseada no conteúdo do novo arquivo da pasta `/biblioteca/migrations/`.

Execute o comando de migração:

```bash
python3 manage.py migrate
```

**OBS:** Este comando aplica as migrações, ou seja, atualiza o esquema do banco de dados de acordo com as mudanças nos modelos.

O que resultará nesta saída:

```bash
Operations to perform:
  Apply all migrations: admin, auth, biblioteca, contenttypes, sessions
Running migrations:
  Applying biblioteca.0001_initial... OK
```

### Interagindo com o Modelo Usando Linha de Comando

Usaremos o interpretador Python (Python Shell) para interagir e adicionar alguns livros a tabela criada no BD. Para abrir um shell Python, digite este comando:

```bash
python3 manage.py shell
```

O que resultará nesta saída:

```bash
Python 3.10.12 (main, Jun 11 2023, 05:26:28) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>>
```

Na parte inferior, após os três, `>>>` escreva o seguinte:

```bash
>>> from biblioteca.models import Livro
```

Pressione `enter` e escreva o código abaixo para ver a tabela Livro vazia:

```bash
>>> Livro.objects.all()
```

Isso deve fornecer um objeto QuerySet vazio, como este:

```bash
<QuerySet []>
```

Um QuerySet é uma coleção de dados de um banco de dados.

Adicione um registro à tabela, executando estas duas linhas:

```bash
>>> livro = Livro(nome='O Senhor dos Anéis', autor='J.R.R. Tolkien', ano=1954)
>>> livro.save()
```

Execute este comando para ver se a tabela Livro possui um membro:

```bash
Livro.objects.all().values()
```

O que resultará nesta saída:

```bash
<QuerySet [{'id': 1, 'nome': 'O Senhor dos Anéis', 'autor': 'J.R.R. Tolkien', 'ano': 1954}]>
```

Para sair do ambiente shell digite:

```bash
quit()
```

Você acaba de aprender como criar uma tabela no BD e como inserir informações nessa tabela utilizando o interpretador do Python. Existem outras formas de fazer a inserção de informações nessa tabela e veremos isso adiante.

### Acessando o Ambiente Administrativo do Django

O Django Admin é uma ferramenta ótima do Django, na verdade é uma interface de usuário CRUD (Criar, Ler, Atualizar, Excluir) para todos os seus modelos!

Para entrar na interface do usuário administrativo, inicie o servidor com este comando:

```bash
python3 manage.py runserver
```

Na janela do navegador, digite na barra de endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/)

A razão pela qual esta URL vai para a página de login do administrador do Django pode ser encontrada no arquivo `urls.py` do seu projeto:

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('', include('biblioteca.urls')),
    path('admin/', admin.site.urls), # definição da rota do ambiente adminstrativo
]
```

**Explicação:** A lista `urlpatterns[]` recebe solicitações na rota `admin/` e as envia para `admin.site.urls`, que faz parte de um aplicativo integrado que vem com o Django e contém muitas funcionalidades e interfaces de usuário, sendo uma delas a interface de usuário de login.

### Criando um Usuário no Sistema no Django

Para poder fazer login no ambiente administrativo do Django, precisamos criar um usuário. Isso é feito digitando este comando:

```bash
python3 manage.py createsuperuser
```

O que dará um prompt como esse:

```bash
Username: admin
Email address: 
Password: 
Password (again): 
The password is too similar to the username.
This password is too short. It must contain at least 8 characters.
This password is too common.
Bypass password validation and create user anyway? [y/N]: y
```

**OBS:** Aqui você deve inserir: nome de usuário, endereço de e-mail (você pode simplesmente deixar em branco ou escolher um endereço de e-mail falso) e senha. Em meu caso coloquei usuário `admin` email em branco e senha `admin`.

Minha senha não atendeu aos critérios, mas este é um ambiente de teste, e opto por criar usuário mesmo assim, digitando `y` gerando assim a saída:

```bash
Superuser created successfully.
```

Agora, reinicie o servidor:

```bash
python3 manage.py runserver
```

Na janela do navegador, digite na barra de endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/).

Preencha o formulário com o nome de usuário e senha corretos (`admin` e `admin`).

### Exibindo os Modelos no Ambiente Administrativo

No ambiente administrativo aberto você pode criar, ler, atualizar e excluir grupos e usuários, além poder trabalhar nos seus modelos. Mas onde está o modelo de Livro criado?

O modelo Livro está faltando, como deveria estar. Você tem que informar ao Django quais modelos devem estar visíveis na interface administrativa.

Para incluir o modelo Livro na interface administrativa, temos que dizer ao Django que este modelo deve estar visível na interface administrativa.

Isso é feito em um arquivo chamado `admin.py`, e está localizado na pasta do seu aplicativo, que no nosso caso é a pasta `biblioteca`.

Abra-o, o mesmo deve estar assim:

```python
from django.contrib import admin

# Register your models here.
```

Insira algumas linhas aqui para tornar o modelo Livro visível na página de administração:

```python
from django.contrib import admin
from .models import Livro

admin.site.register(Livro)
```

Agora, acesse o endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/).

Clique em Livros e veja o registro de livros que inserimos anteriormente neste tutorial:

Na lista de Livros, vemos "Livro object (1)", "Livro membro (2)" etc., que podem não ser os dados que você deseja que sejam exibidos na lista. Seria melhor exibir "nome" e "autor".

Para mudar isso para um formato mais fácil de ler, temos duas opções:

* Alterar a função de representação de string `__str__()` do modelo de Livro.
* Definir a propriedade `list_details` do modelo de Livro.

Para alterar utilizando a primeira forma, devemos alterar a função de representação de string `__str__()` do modelo de Livro. Para isso faça o seguinte no arquivo `models.py` dentro da pasta `biblioteca`:

```python
from django.db import models

class Livro(models.Model):
    nome = models.CharField(max_length=255)
    autor = models.CharField(max_length=255)
    ano = models.IntegerField()

    def __str__(self):           # função adionada
        return f"{self.nome} - {self.autor}" 
```

Agora, acesse o endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/) e analise o resultado.

Para alterar utilizando a segunda forma (RECOMENDADA), devemos definir a propriedade `list_display` do arquivo `admin.py`. Primeiro crie uma classe `LivroAdmin()` e especifique a tupla `list_display`, assim:

```python
from django.contrib import admin
from .models import Livro

class LivroAdmin(admin.ModelAdmin):
    list_display = ("nome", "autor", "ano")

admin.site.register(Livro, LivroAdmin)
```

**OBS:** Lembre-se de adicionar LivroAdmin como um argumento no arquivo, como em: `admin.site.register(Livro, LivroAdmin)`.

Agora, acesse o endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/) e analise o resultado.

### Adicionando Novos Livros

Agora, podemos criar, atualizar e excluir livros em nosso banco de dados.

Iremos adicionar mais dois livros, clique no botão "ADD LIVRO" no canto superior direito:

Você receberá um formulário vazio onde poderá preencher os campos do livro. Utilize as informações a seguir para preenchimento:

```json
{
    "nome": "1984",
    "autor": "George Orwell",
    "ano": 1949
},
{
    "nome": "Dom Quixote",
    "autor": "Miguel de Cervantes",
    "ano": 1605
}
```

Preencha os campos e clique em `SAVE`:

### Carregando a Interface Livro com Dados do BD

Até aqui, vimos como trabalhar com o Banco de Dados, mas a interface da nossa aplicação (livro) ainda não está fazendo a leitura dos dados do BD.

Agora, iremos atualizar a interface para puxar/pegar os dados do BD.

Assim, é necessário atualizar o código `views.py` da pasta `biblioteca`. Devemos remover os dados que estavam inseridos estaticamente nesse arquivo.

```python
...
from .models import Livro    # adicione esta importação

...

def livros(request):         # atualize esta função
    livros = Livro.objects.all().values()
    template = loader.get_template('livros.html')
    context = {
        'livros': livros,
    }
    return HttpResponse(template.render(context, request))
```

Por fim, acesse o endereço [127.0.0.1:8000/livros](127.0.0.1:8000/livros) e analise o resultado. Repare que os livros listados são somente os livros cadastrados no Banco de Dados.

### Configurando o Projeto Django em Português

Repare que todo o ambiente administrativo do django está em Inglês, vamos agora, alterar isso para português.

Assim, no arquivo `settings.py` (na pasta `portal_biblioteca`), faça a seguinte alteração:

```python
...
LANGUAGE_CODE = 'pt-BR'
...
```

Por fim, acesse o endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/) e analise o resultado.

### Criando o Modelo de TCC

Até aqui criamos apenas uma Tabela no BD que é Livro. Agora, iremos criar uma Tabela TCC no Modelo do BD.

Primeiramente, iremos criar uma classe chamada `TCC`. Para isso, abra o arquivo `models.py` na pasta `biblioteca` e digite o seguinte conteúdo:

```python
...

class TCC(models.Model):    # classe adiconada
    titulo = models.CharField(max_length=255)
    autor = models.CharField(max_length=255)
    orientador = models.CharField(max_length=255)
    ano = models.IntegerField()

    def __str__(self):
        return f"{self.titulo} - {self.autor}"
```

O código acima irá criar uma Tabela chamada TCC no BD SQLite.

Em seguida, execute o código abaixo para que seja criado a tabela TCC no banco de dados de fato:

```bash
python3 manage.py makemigrations biblioteca
```

O que resultará nesta saída:

```bash
Migrations for 'biblioteca':
  biblioteca/migrations/0002_tcc.py
    - Create model TCC
```

A tabela ainda não foi criada, execute o comando de migração para que a tabela seja de fato criada:

```bash
python3 manage.py migrate
```

O que resultará nesta saída:

```bash
Operations to perform:
  Apply all migrations: admin, auth, biblioteca, contenttypes, sessions
Running migrations:
  Applying biblioteca.0002_tcc... OK
```

Agora, iremos informar ao Django quais modelos devem estar visíveis na interface administrativa. Para incluir o modelo TCC na interface administrativa, temos que dizer ao Django que este modelo deve estar visível na interface administrativa.

Isso é feito em um arquivo chamado `admin.py`, e está localizado na pasta do seu aplicativo, que no nosso caso é a pasta `biblioteca`. Digite o seguinte código:

```python
from django.contrib import admin
from .models import Livro
from .models import TCC    #linha adicionada

class LivroAdmin(admin.ModelAdmin):
    list_display = ("nome", "autor", "ano")

class TCCAdmin(admin.ModelAdmin):  # função adicionada
    list_display = ("titulo", "autor", "orientador", "ano")

admin.site.register(Livro, LivroAdmin)
admin.site.register(TCC, TCCAdmin) # linha adicionada
```

Agora, reinicie o servidor:

```bash
python3 manage.py runserver
```

Em seguida, acesse o endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/).

### Adicionando Novos TCCs

Agora, podemos criar, atualizar e excluir TCCs em nosso banco de dados.

Iremos adicionar mais três TCCs, clique no botão "ADICIONAR TCC" no canto superior direito.

Você receberá um formulário vazio onde poderá preencher os campos do TCC. Utilize as informações a seguir para preenchimento:

```json
{
    "titulo": "Sistemas de Recomendação Personalizados",
    "autor": "Maria Silva",
    "orientador": "Prof. João Santos",
    "ano": 2021
},
{
    "titulo": "Segurança de Redes em Ambientes Corporativos",
    "autor": "Pedro Oliveira",
    "orientador": "Profa. Ana Rodrigues",
    "ano": 2020
},
{
    "titulo": "Inteligência Artificial Aplicada à Análise de Dados",
    "autor": "Luana Costa",
    "orientador": "Prof. André Martins",
    "ano": 2019
}
```

Preencha os campos e clique em `SAVE`.

### Pegando Dados de TCC do BD

Agora, iremos atualizar a interface do TCC para puxar/pegar os dados do BD.

Assim, é necessário atualizar o código `views.py` da pasta `biblioteca`.

```python
...
from .models import TCC    # adicione esta importação

...

def tccs(request):         # atualize esta função
    tccs = TCC.objects.all().values()
    template = loader.get_template('tccs.html')
    context = {
        'tccs': tccs,
    }
    return HttpResponse(template.render(context, request))
```

Agora, acesse o endereço [127.0.0.1:8000/tccs](127.0.0.1:8000/tccs) e analise o resultado. Repare que os TCCs listados são somente os TCCs cadastrados no Banco de Dados.

Ainda no código `views.py` da pasta `biblioteca`, atualize a função `tcc_detalhes` para que a mesma pegue os dados também do banco de dados baseado no `id`.

```python
...
def tcc_detalhes(request, id):
    tcc = TCC.objects.get(id=id)
    template = loader.get_template('tcc_detalhes.html')
    context = {
        'tcc': tcc,
    }
    return HttpResponse(template.render(context, request))
```

Agora, acesse o endereço [127.0.0.1:8000/tccs](127.0.0.1:8000/tccs) e analise o resultado. Repare que os detalhes dos TCCs são os cadastrados no Banco de Dados.

Para mais informações, consulte a [documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/topics/db/models/).

### Personalizando o Modelo de Página 404

Se você tentar acessar uma página que não existe (será gerado um erro 404), então o Django o direcionará para uma visualização interna que lida com erros 404.

Você aprenderá como personalizar essa visualização 404 mais adiante, mas primeiro, tente acessar uma página que não existe.

Na janela do navegador, digite a seguinte URL [http://127.0.0.1:8000/blabla](http://127.0.0.1:8000/blabla).

Você obterá o seguinte resultado:

![Sistema Objetivo da Aula](./docs/erro404-1.png)

Isso ocorreu, pois a variável `DEBUG` está definida como `True` nas suas configurações no arquivo `settings.py`. 

No entanto, a forma esperada de saída de erro, quando o sistema estiver em produção, é a exibida abaixo: 
 
![Sistema Objetivo da Aula](./docs/erro404-2.png)

Para obter uma saída semelhante a segunda forma (correta), você deve definir a variável `DEBUG` como `False`. Assim, você será direcionado para o modelo Django 404 integrado.

Isso é feito no arquivo `settings.py`, onde você também deve especificar o nome do host de onde seu projeto é executado:

```python
...
# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = False

ALLOWED_HOSTS = ['*']
...
```

**Importante**: Quando `DEBUG = False`, o Django exige que você especifique os hosts nos quais permitirá que este projeto Django seja executado.

Quando o sistema estiver em produção, isso deve ser substituído por um nome de domínio adequado, semelhante abaixo:

```python
ALLOWED_HOSTS = ['yourdomain.com']
```

Mas, como ainda estamos em desenvolvimento, então podemos colocar qualquer domínio como abaixo:

```python
ALLOWED_HOSTS = ['*']
```

Escolhemos `*`, o que significa que qualquer endereço tem permissão para hospedar este site. Isso deve ser alterado para um nome de domínio real quando você implantar seu projeto em um servidor público.

O Django procurará um arquivo chamado `404.html` na pasta `templates` e o exibirá quando houver um erro 404. Se esse arquivo não existir, o Django mostrará o "Not Found" que você viu no exemplo acima.

Para personalizar esta mensagem, basta criar um arquivo na pasta `templates` e nomeá-lo `404.html`, e preenchê-lo com o que quiser. Utize o exemplo a seguir:

```html
{% extends "base.html" %}

{% load static %}

{% block titulo %}
    Portal Biblioteca - Erro 404
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <h1>Portal Biblioteca</h1>
        <h4>Página não encontrada</h4>
        <p>Não existe uma página para a URL solicitada.</p>
    </main>
{% endblock %}
```

Em seguida, execute o servidor.

```bash
python3 manage.py runserver
```

Na janela do navegador, digite na barra de endereço uma URL inexistente e você obterá o modelo 404 personalizado. Exemplo: [http://127.0.0.1:8000/blabla](http://127.0.0.1:8000/blabla).

![Sistema Objetivo da Aula](./docs/erro404-4.png)

No entanto, esse modelo deveria aparecer como abaixo. Precisaremos incluir uma biblioteca externa para que o Django consiga servir arquivos estáticos.

![Sistema Objetivo da Aula](./docs/erro404-3.png)

### Manipulando Arquivos Estáticos

Devido a modificação anterior `DEBUG = False`, o Django passou a não mais servir arquivos estáticos, pelo menos não em produção. Para resolver isso, teremos que usar uma biblioteca de terceiros.

Existem muitas alternativas, mostraremos como usar uma biblioteca Python chamada `WhiteNoise`.

Para instalar o WhiteNoise em seu ambiente virtual, digite o comando abaixo:

```bash
pip3 install whitenoise
```

Para que o Django saiba que você deseja executar o WhitNoise, você precisa especificá-lo na lista `MIDDLEWARE` do arquivo `settings.py`:

```python
...
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
    'whitenoise.middleware.WhiteNoiseMiddleware',   # linha adicionada
]
...
```

Há mais uma ação que você precisa executar antes de poder servir o arquivo estático. Você precisa coletar todos os arquivos estáticos utilizando o comando abaixo.

```bash
python3 manage.py collectstatic
```

Em seguida, execute o servidor.

```bash
python3 manage.py runserver
```

Em modo de produção, o WhiteNoise será responsável por servir os arquivos estáticos automaticamente. Acesse um arquivo estático (por exemplo, [http://127.0.0.1:8000/static/mystyles.css](http://127.0.0.1:8000/static/mystyles.css)) para confirmar que o WhiteNoise está servindo o conteúdo corretamente.

Na janela do navegador, digite na barra de endereço uma URL inexistente e você obterá o modelo 404 personalizado. Exemplo: [http://127.0.0.1:8000/blabla](http://127.0.0.1:8000/blabla).

![Sistema Objetivo da Aula](./docs/erro404-3.png)

### Exibindo Dashboard com Dados do BD

Agora, iremos atualizar o nosso código para que o dashboard exibido contenha gráficos com dados vindo do BD e não gráficos com dados fixados em código.
Para isso, precisamos fazer a seguinte atualização no arquivo `views.py`.

```python
...
def dashboard(request):
    template = loader.get_template('dashboard.html')
    context = {
        'labels': ['Livros', 'TCCs', 'Dissertações', 'Teses', 'Apostilas', 'Jornais'],
        'data': [12, 19, 8, 5, 2, 10]
    }
    return HttpResponse(template.render(context, request))
```

**OBS**: Repare que os dados ainda estão fixos, mas agora vem do template via Python.

Em seguida, precisamos atualizar o arquivo `dashboard.html` conforme abaixo:

```html
...
    <script> <!-- Incluí esse script -->
        <!-- Cria variáveis globais para vindas do template para serem acessadas no JS externo "myscripts.js". -->
        const vlabels = {{ labels|safe }};
        const vdata = {{ data|safe }};
    </script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="{% static 'myscripts.js' %}"></script>
...
```

**Explicação**: Quando o JavaScript está em um arquivo separado, você não pode usar diretamente as tags de template do Django (`{{ }}`) dentro do arquivo. Uma solução é definir as variáveis no próprio HTML e, em seguida, acessá-las no arquivo JavaScript externo. No seu template HTML, defina as variáveis de dados (`vlabels` e `vdata`) dentro de um bloco `<script>` para que fiquem disponíveis globalmente. O `| safe` é um filtro do Django usado para garantir que os dados sejam renderizados sem qualquer escape adicional de HTML. Esse filtro é importante quando você está passando dados JSON ou arrays para JavaScript, pois ele impede que o Django faça a escapada automática (substituindo, por exemplo, `"` por `&quot;`). Sem o filtro `|safe`, o Django escaparia caracteres especiais nos dados, resultando em valores incorretos ou erro de sintaxe.

Em seguida, precisamos atualizar o arquivo `myscripts.js` conforme abaixo:

```javascript
function graficoBarras() {
    const ctx = document.getElementById('graficoNumVolumes');

    new Chart(ctx, {
        type: 'bar',
        data: {
        labels: vlabels, // Alterei aqui. Acessa variável global 'labels'
        datasets: [{
            label: 'Número de Volumes',
            data: vdata,  // Alterei aqui. Acessa a variável global 'data'
            borderWidth: 1
        }]
        },
        options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
        }
    });
}          

function graficoPizza(){
    const ctx = document.getElementById('graficoPizza');

    new Chart(ctx, {
        type: 'pie',
        data: {
        labels: vlabels, // Alterei aqui. Acessa variável global 'labels'
        datasets: [{
            label: 'Número de Volumes',
            data: vdata, // Alterei aqui. Acessa a variável global 'data'
            backgroundColor: [
                'rgb(255, 99, 132)',
                'rgb(54, 162, 235)',
                'rgb(255, 205, 86)',
                'rgb(80, 60, 200)',
                'rgb(255, 100, 86)',
                'rgb(54, 255, 150)'
            ],
            hoverOffset: 8
        }]
        }
    });
}

graficoBarras();

graficoPizza();
```

**Explicação**: No arquivo `myscripts.js`, você pode agora acessar as variáveis `vlabels` e `vdata` diretamente, pois elas foram definidas no escopo global do HTML.

Em seguida, execute comando abaixo para fazer a cópia dos arquivos estáticos alterados:

```bash
python3 manage.py collectstatic
```

Em seguida, execução do projeto:

```bash
python3 manage.py runserver
```

Após essas alterações, os dados exibidos nos gráficos vêem da View e não do JavaScript, mas ainda continuam fixos. Experimente alterar os valores do quantitativo de livros no arquivo `views.py` e analise o resultado.

Agora, iremos pegar os dados de uma nova tabela do BD. Para issso, no arquivo `models.py` inclua o seguinte código:

```python
...
class QuantitativoMateriais(models.Model):
    livros = models.IntegerField()
    tccs = models.IntegerField()
    dissertacoes = models.IntegerField()
    teses = models.IntegerField()
    apostilas = models.IntegerField()
    jornais = models.IntegerField()

    def __str__(self):
        return f"{self.livros} - {self.tccs} - {self.dissertacoes} - {self.teses} - {self.apostilas} - {self.jornais}"
```

Esse código cria uma tabela chamada `QuantitativoMateriais` com o quantitativo de livros, TCCs, dissertações, teses, apostilas e jornais presentes na Biblioteca.

No arquivo, `admin.py` inclua o seguinte código: 

```python
...
from .models import QuantitativoMateriais
...
class QuantitativoMateriaisAdmin(admin.ModelAdmin):
    list_display = ("id", "livros", "tccs", "dissertacoes", "teses", "apostilas", "jornais")
...
admin.site.register(QuantitativoMateriais, QuantitativoMateriaisAdmin)
```

Esse código informa ao Django que essa tabela deverá estar disponível no ambiente administrativo.

Agora, execute o comando para criar as migrações:

```bash
python3 manage.py makemigrations
```

Agora, execute o comando para fazer as migrações:

```bash
python3 manage.py migrate
```

Nessa etapa, iremos agora executar o projeto e, em seguida, cadastrar um quantitativo de materiais na tabela criada.

```bash
python3 manage.py runserver
```

Por fim, no arquivo `views.py` inclua o seguinte código:

```python
...
from .models import QuantitativoMateriais
...
def dashboard(request):
    qtd = QuantitativoMateriais.objects.all().values()
    template = loader.get_template('dashboard.html')
    v = qtd[0]
    context = {
        'labels': ['Livros', 'TCCs', 'Dissertações', 'Teses', 'Apostilas', 'Jornais'],
        'data': [v['livros'], v['tccs'], v['dissertacoes'], v['teses'], v['apostilas'], v['jornais']]
    }
    return HttpResponse(template.render(context, request))
```

Em seguida, execução do projeto:

```bash
python3 manage.py runserver
```

Avalie os gráficos mostrados. Atualize os valodres da tabela de quantitativo e veja a mudança refletida nos gráficos.

### Informações Adicionais sobre BD

Caso queira ver o que foi feito no BD, basta digitar o comando abaixo com o número da migração:

```bash
python3 manage.py sqlmigrate biblioteca 0001
```

**Obs:** no comando acima `biblioteca` representa o nome da nossa aplicação web e o número 0001 é o número da migração.

A saída desse comando é algo parecido com:

```sql
BEGIN;
--
-- Create model Livro
--
CREATE TABLE "biblioteca_livro" ("id" integer NOT NULL PRIMARY KEY AUTOINCREMENT, "nome" varchar(255) NOT NULL, "autor" varchar(255) NOT NULL, "ano" integer NOT NULL);
COMMIT;
```

Para vermos com detalhes o conteúdo do BD, podemos utilizar a ferramenta [DB Browser for SQLite](https://sqlitebrowser.org/). Assim, basta abrir o arquivo do BD chamado `db.sqlite3` que está na raiz do projeto.

## Créditos e Referências

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

Este tutorial foi inspirado nos seguintes recursos:

* [Documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/)
* [Curso de Django da w3schools](https://www.w3schools.com/django/index.php)
