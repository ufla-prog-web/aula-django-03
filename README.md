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
* [Próximas Etapas](#próximas-etapas)
* [Créditos e Referências](#créditos-e-referências)

## Introdução

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

Aula Django 03. Projeto utilizando o Django para ser desenvolvido na Aula de GAC116 - Programação Web. Essa aula é uma continuação da Aula Django 02.

O objetivo desse projeto é criar um sistema para gestão de biblioteca.

Este tutorial foi elaborado baseado no tutorial disponível no [curso de django da w3schools](https://www.w3schools.com/django/index.php) e também baseado na [documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/).

A aula está estruturada em forma de tutorial, de forma que cada estudante vá replicando em seu computador os conceitos e recursos aqui mostrados. A aula mostra a evolução do código/solução para que os estudantes possa compreender como as diferentes tecnologias se conectam.

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

Em seguida, execute comando abaixo para fazer a cópia dos arquivos estáticos:

```bash
python3 manage.py collectstatic
```

Inicie a execução do projeto django criado:

```bash
python3 manage.py runserver
```

**OBS:** Por padrão, o servidor de desenvolvimento escuta na porta 8000, mas você pode especificar uma porta diferente como argumento opcional, por exemplo, `python3 manage.py runserver 8081`.

Acesse através do navegdor web a página [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

A aula anterior avançou até aqui.

### Melhorando a Tela do Projeto com Bootstrap

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
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
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
                                <a class="nav-link" href="/livros">Livros</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/tccs">TCCs</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/dashboard">Dashboard</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/auth/login">Login</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/auth/cadastro">Cadastre-se</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/auth/logout">Logout</a>
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

### Adicionando Controle de Usuários no Django

Esta parte do tutorial foi baseada na [documentação oficial django](https://docs.djangoproject.com/pt-br/5.0/topics/auth/default/) e também na [videoaula](https://www.youtube.com/watch?v=gdhiA6wObw0).

O Django possui já prontos diversos recursos para trabalhar com autenticação de usuários e controle de nível de acesso.

Agora, iremos adicionar em nosso projeto um sistema de gestão de usuários. Para criarmos na sequência as telas de login e cadastro na plataforma.

Para isso, iremos criar uma outra aplicação/aplicativo web dentro do nosso projeto. Assim, digite o seguinte conteúdo.

```bash
python3 manage.py startapp usuarios
```

Agora, atualize a lista `INSTALLED_APPS` em `settings.py` na pasta `portal_biblioteca`:

```python
...
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'biblioteca',
    'usuarios', #adicone seu app aqui 
]
...
```

Agora, iremos criar uma pasta chamada `templates` dentro da aplicação `usuarios`. Nesta pasta, iremos criar um arquivo chamado `login.html` com o seguinte conteúdo:

```html
<h1>Login</h1>
```

Ainda nesta pasta, iremos criar também um arquivo chamado `cadastro.html` com o seguinte conteúdo:

```html
<h1>Cadastro</h1>
```

Em seguida, precisamos definir as views do nosso sistema de login e cadastro. Assim, digite o código abaixo no arquivo `views.py` na pasta `usuarios`:

```python
from django.http import HttpResponse
from django.shortcuts import render

def login(request):
    return render(request, 'login.html')

def cadastro(request):
    return render(request, 'cadastro.html')
```

Agora, crie na pasta `usuarios` um arquivo chamado `urls.py` com o seguinte conteúdo:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('login', views.login, name='login'),
    path('cadastro', views.cadastro, name='cadastro'),
]
```

Agora, precisamos informar a nossa aplicação principal da existência dessas novas URLs. Assim, edite o código `urls.py` da pasta `porta_biblioteca` da seguinte forma:

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('', include('biblioteca.urls')),
    path('auth/', include('usuarios.urls')),   #adicione essa linha aqui
    path('admin/', admin.site.urls),
]
```

Agora, reinicie o servidor:

```bash
python3 manage.py runserver
```

Por fim, acesse o endereço [127.0.0.1:8000/](127.0.0.1:8000/). Navegue pelas abas Login e Cadastre-se.

### Melhorando a Tela de Cadastro

Agora, iremos melhorar a exibição da tela de Cadastro.

Assim, no arquivo `cadastro.html` digite o seguinte:

```html
{% extends "base.html" %}

{% block titulo %}
    Portal Biblioteca - Cadastro
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <center>
            <h1>Cadastre-se</h1>
            <form action="{% url 'cadastro' %}" method="POST">
                {% csrf_token %}
                <div class="input-group">
                    <span class="input-group-text">Usuário: </span>
                    <input type="text" class="form-control" placeholder="Usuário ..." name="usuario">
                </div>
                <br>
                <div class="input-group">
                    <span class="input-group-text">E-mail: </span>
                    <input type="email" class="form-control" placeholder="E-mail ..." name="email">
                </div>
                <br>
                <div class="input-group">
                    <span class="input-group-text">Senha: </span>
                    <input type="password" class="form-control" placeholder="Senha ..." name="senha">
                </div>
                <br>
                <input type="submit" value="Cadastrar" class="btn btn-primary">
            </form>
        </center>
    </main>
{% endblock %}
```

**Explicação:** O código acima cria um formulário com os seguintes campos: usuário, email, senha e botão cadastrar. Neste formulário, quando clicado no botão cadastrar enviará uma ação via método POST para a url de nome `cadastro` (nome definida no arquivo `url.py`). A tag `csrf_token` é necessária para fazer uma verificação de segurança.

**Explicação:** O CSRF Token, que significa "Cross-Site Request Forgery Token" (Token de Proteção contra Solicitação Falsificada entre Sites), é uma medida de segurança utilizada em aplicações da web para proteger contra ataques CSRF (Cross-Site Request Forgery), também conhecidos como ataques de falsificação de solicitação entre sites. Um ataque CSRF ocorre quando um invasor engana um usuário autenticado a executar ações indesejadas em um site sem o conhecimento ou consentimento do usuário. Isso é feito explorando o fato de que os navegadores da web geralmente incluem automaticamente cookies de sessão em todas as solicitações para um domínio, incluindo solicitações maliciosas.

Em seguida, atualize o código do método cadastro na `view.py`.

```python
...
def cadastro(request): # atualize essa função
    if request.method == "GET":
        return render(request, 'cadastro.html')
    else: #senão será via método "POST":
        usuario = request.POST.get('usuario')
        email = request.POST.get('email')
        senha = request.POST.get('senha')
        return HttpResponse(usuario)
```

Em seguida, acesse o endereço [http://127.0.0.1:8000/auth/cadastro](http://127.0.0.1:8000/auth/cadastro) e efetue um cadastro e analise o resultado na tela.

Até aqui, não efetuamos de fato um cadastro, apenas exibimos na tela a informação do usuário.

Agora, iremos inserir as informações cadastradas no BD.

Assim, atualize o código do método `cadastro` na `view.py`.

```python
from django.contrib.auth.models import User  # faça essa inclusão

...

def cadastro(request):  # atualize essa função
    if request.method == "GET":
        return render(request, 'cadastro.html')
    else: #senão será via método "POST":
        usuario = request.POST.get('usuario')
        email = request.POST.get('email')
        senha = request.POST.get('senha')

        user = User.objects.filter(username=usuario).first()
        if user:
            return HttpResponse('Já existe um usuário com esse nome')

        # se não existir usuário com esse nome cria e salva o mesmo.
        user = User.objects.create_user(username=usuario, email=email, password=senha)
        user.save()

        return HttpResponse('Usuário cadastrado com sucesso')
```

Em seguida, acesse o endereço [http://127.0.0.1:8000/auth/cadastro](http://127.0.0.1:8000/auth/cadastro) e efetue um cadastro e analise o resultado na tela e também no menu administrativo do Django. Efetue também cadastro de dois usuários com mesmo nome e analise o resultado.

**OBS:** O Django não armazena senhas brutas (texto não criptografado) no modelo de usuário. Ele armazena apenas um hash da senha.

Para mais detalhes sobre a classe `User`, consulte a [documentação oficial](https://docs.djangoproject.com/pt-br/5.0/topics/auth/default/).

### Melhorando a Tela de Login

Agora, iremos melhorar a exibição da tela de Login.

Assim, atualize o código do arquivo `login.html` para o seguinte:

```html
{% extends "base.html" %}

{% block titulo %}
    Portal Biblioteca - Login
{% endblock %}

{% block conteudo %}
    <main class="container mt-5">
        <center>
            <h1>Login</h1>
            <form action="{% url 'login' %}" method="POST">
                {% csrf_token %}
                <div class="input-group">
                    <span class="input-group-text">Usuário: </span>
                    <input type="text" class="form-control" placeholder="Usuário ..." name="usuario">
                </div>
                <br>
                <div class="input-group">
                    <span class="input-group-text">Senha: </span>
                    <input type="password" class="form-control" placeholder="Senha ..." name="senha">
                </div>
                <br>
                <input type="submit" value="Logar" class="btn btn-primary">
            </form>
        </center>
    </main>
{% endblock %}
```

Em seguida, atualize o código do método `login` na `view.py`.

```python
from django.contrib.auth import authenticate   # adicione essa linha
...
def login(request):       #atualize essa função
    if request.method == "GET":
        return render(request, 'login.html')
    else:
        usuario = request.POST.get('usuario')
        senha = request.POST.get('senha')
        user = authenticate(username=usuario, password=senha)
        if user:
            return HttpResponse('Autenticado')
        else:
            return HttpResponse('Usuario ou Senha inválidos')

```

Em seguida, acesse o endereço [http://127.0.0.1:8000/auth/login](http://127.0.0.1:8000/auth/login) e efetue um login e analise o resultado na tela. Tente colocar um usuário válido e um usuário inválido.

Em seguida, atualize o código do método cadastro na `view.py`.

```python
from django.contrib.auth import login as login_django #importe também o login

...
def login(request):
    if request.method == "GET":
        return render(request, 'login.html')
    else:
        usuario = request.POST.get('usuario')
        senha = request.POST.get('senha')
        
        user = authenticate(username=usuario, password=senha)
        if user:
            login_django(request, user) # linha adicionada
            return HttpResponse('Autenticado')
        else:
            return HttpResponse('Usuario ou Senha inválidos')
```

Em seguida, acesse o endereço [http://127.0.0.1:8000/auth/login](http://127.0.0.1:8000/auth/login) e  efetue um login e analise o resultado na tela. Tente colocar um usuário válido e um usuário inválido. Neste ponto, ainda não dá para ver muita diferença entre os dois últimos passos.

**Explicação:** As principais diferenças entre "authenticate" e "login" do django são destacadas a seguir:

**authenticate:**
* O método "authenticate" é uma função fornecida pelo Django que é usada para verificar as credenciais de um usuário em um sistema de autenticação.
* Ele recebe as informações de login do usuário, como nome de usuário e senha, e verifica se essas informações correspondem a um usuário registrado no sistema.
* Se as credenciais estiverem corretas, o método "authenticate" retornará um objeto de usuário válido que representa o usuário autenticado. Caso contrário, retornará "None".

**login:**
* O método "login" refere-se ao processo de estabelecer uma sessão de usuário autenticada em um aplicativo da web após a autenticação bem-sucedida.
* O Django fornece uma função chamada "login" que permite que você associe um objeto de usuário autenticado a uma sessão. Isso é importante para manter o estado de autenticação do usuário durante a sessão.
* A função "login" normalmente é usada após o usuário ser autenticado com sucesso usando o "authenticate".

### Disponibilizando o Dashboard Apenas para Usuários Logados

Agora, iremos permitir que a visualização dos dashboards esteja disponível apenas se o usuário estiver logado na plataforma.

Dessa maneira, atualize o código da função dashboard em `view.py` da pasta `biblioteca` para o seguinte.

```python
...
def dashboard(request):
    if request.user.is_authenticated:
        template = loader.get_template('dashboard.html')
        return HttpResponse(template.render())
    return HttpResponse("Você precisa estar logado!")
```

Em seguida, abra uma guia anônima do navegador e acesse o endereço [http://127.0.0.1:8000](http://127.0.0.1:8000). Tente acessar a tela de dashboard. Na sequência, faça login na plataforma e então tente acessar o dashboard.

Uma outra forma de fazer a mesma operação é utilizando o decorador `login_required`. Atualize o seu código da função dashborad em `view.py` da pasta `biblioteca` para o seguinte.

```python
from django.contrib.auth.decorators import login_required
...
@login_required(login_url="/auth/login")
def dashboard(request):
    template = loader.get_template('dashboard.html')
    return HttpResponse(template.render())
```

Em seguida, abra uma guia anônima do navegador e acesse o endereço [http://127.0.0.1:8000](http://127.0.0.1:8000). Tente acessar a tela de dashboard. Perceba que portal redireciona para a tela de login, isso ocorre, pois colocamos isso no parâmetro `login_url`. Na sequência, faça login na plataforma e então tente acessar o dashboard.

### Adicionando Logout no Sistema

Agora, iremos adicionar no nosso sistema o recurso de logout.

Para isso, vá no arquivo `views.py` da pasta `usuarios` e adicione o seguinte conteúdo:

```python
from django.contrib.auth import logout as logout_django
...

def logout(request):
    logout_django(request)
    return HttpResponse('Usuario deslogado do sistema!')
```

**Explicação:** Quando você chama `logout()` do django ou `logout_django()` neste caso, os dados da sessão da solicitação atual são completamente limpos. Todos os dados existentes são removidos. Isso evita que outra pessoa use o mesmo navegador para fazer login e ter acesso aos dados da sessão do usuário anterior.

Em seguida, vá no arquivo `urls.py` da pasta `usuarios` e adicione a seguinte rota.

```python
...
    path('logout', views.logout, name='logout'),
...
```

Por fim, acesse o endereço [http://127.0.0.1:8000](http://127.0.0.1:8000). Faça logout e tente acessar a página de dashboard. Faça login e tente acessar a página de dashboard. Analise as mensagens impressas.

### Adicionando no Dashboard Informação do Usuário Logado

Nessa etapa, desejamos adicionar informações do usuário logado na tela do dashboard.

Primeiramente, é necessário atualizar parte do conteúdo do arquivo `dashboard.html` da `biblioteca` e subpasta `templates`.

```html
...
    <main class="container mt-5">
        <!-- Início do bloco de código adicionado -->
        <div class="row">
            <div class="col-md-12">
                <center>
                    <div class="card" style="width:180px">
                        <img class="card-img-top" src="{% static 'img_avatar.png' %}" alt="Imagem do card" width="30">
                        <div class="card-body">
                            <h4 class="card-title"> {{ usuario }} </h4>
                            <p class="card-text">Email: {{ email }} </p>
                        </div>
                    </div>
                </center>
            </div>
        </div>
        <!-- Fim do bloco de código adicionado -->
        <h1>Dashboard</h1>
...
```

Em seguida, é necessário copiar o arquivo `img_avatar.png` da pasta `docs` para a pasta `staticfiles`.

Em seguida, iremos atualizar o método dashboard no arquivo `views.py` da pasta `biblioteca`.

```python
@login_required(login_url="/auth/login")
def dashboard(request):
    template = loader.get_template('dashboard.html')
    # Você pode acessar o usuário logado através de request.user
    user = request.user
    # Agora, você pode fazer qualquer coisa com o objeto 'user', como acessar seus campos, por exemplo:
    username = user.username
    email = user.email
    context = {
        'usuario': username,
        'email': email,
    }
    return HttpResponse(template.render(context, request))
```

Em seguida, execute o comando abaixo:

```bash
python3 manage.py collectstatic
```

Em seguida, reinicie o servidor:

```bash
python3 manage.py runserver
```

Por fim, acesse o endereço [http://127.0.0.1:8000](http://127.0.0.1:8000) e analise a página de dashboard com diferentes usários logados no sistema.

### Algumas Informações Adicionais

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

## Próximas Etapas

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

Agora que você sabe como construir uma página web utilizando o framework Django, utilize os conhecimentos e exemplos aqui apresentados para fazer o seu trabalho final de implementação.

## Créditos e Referências

<a href="#índice"><img align="right" width="15" height="15" src="./docs/up-arrow.png" alt="Voltar para topo"></a>

Este tutorial foi inspirado nos seguintes recursos:

* [Documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/)
* [Curso de Django da w3schools](https://www.w3schools.com/django/index.php)
