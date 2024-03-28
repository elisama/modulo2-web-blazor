# Modulo 2: Web Blazor

[Criar o seu primeiro aplicativo Web com o Blazor](https://learn.microsoft.com/pt-br/training/modules/build-your-first-blazor-web-app/)

## 1    Objetivos de aprendizagem

Neste módulo, você vai:

- Configurar o seu ambiente local para o desenvolvimento do Blazor.
- Crie um novo projeto de aplicativo Web do Blazor.
- Adicione lógica de componente a um aplicativo Web do Blazor.

## 2    Criação (instalação) do aplicativo Blazor

Caso já esteja dentro da pasta de arquivos que ficará a aplicação, basta executar o seguinte comando:

    `dotnet new blazor`

Caso deseje criar juntamente a pasta que ele irá ser instalado, use o seguinte comando:

    `dotnet new blazor -o nome-da-nova-pasta`

Verificando se a instalação ocorreu com sucesso:

    `dotnet watch`

Após a execução desse último comando, o aplicativo iniciará e aplicacará todas as alterações de código ao aplicativo em execução. Para encerrar a execução da aplicação, basta acionar *Ctrl + C*.

## 3    Qual a versão .NET do SDK foi instalada?

Caso se digite os comandos acima, a versão instalada será a mais recente que estiver em sua máquina, a qual pode ser conferida pelo comando:

    `dotnet --list-sdks`

Versão instalada como sendo a mais recente da máquina, o qual fica no arquivo com as principais configurações do projeto *arquivo.csproj*.

<img width="340" alt="versao_framework" src="https://github.com/elisama/modulo2-web-blazor/assets/7691281/ea35b035-8dc4-4bc6-a8b0-d87a5250d3ba">

Agora, caso haja em sua máquina outras versões do .NET e deseje instalar a aplicação com essa versão, ex. .NET 5, basta executar o comando abaixo:

    `dotnet new blazor -f net5.0`

## 4    Arquivos Importantes

- *Program.cs*: é o ponto de entrada do aplicativo, como se fosse o código de start. Aqui o servidor é configurado e o programador pode configurar os serviços de aplicativos e o [middleware](https://learn.microsoft.com/pt-br/aspnet/core/fundamentals/middleware/?view=aspnetcore-8.0) [^1].

- *App.razor*: é o componente raiz do aplicativo;

- *Routes.razor*: configura as rotas das páginas;

- *BlazorApp.csproj*: define o tipo de SDK utilizado, a versão do .NET, o tipo de aplicativo, se é razor, assembly, etc, e suas dependências;

<img width="399" alt="csproj" src="https://github.com/elisama/modulo2-web-blazor/assets/7691281/01ad0d4e-3690-4d10-a888-2646e5dd71aa">

- *lauchSettings.json*: fica no diretório 'Properties', contém informações como:
  - windowsAuthentication: <span style="color:red">false</span> ou <span style="color:blue">true</true>, define se haverá autentição necessária na aplicação. A autenticação do Windows (anteriormente chamada de NTLM e também chamada de autenticação de Desafio/Resposta do Windows NT) é uma forma segura de autenticação porque o nome de usuário e a senha são criptografados antes de serem enviados pela rede;
  - anonymousAuthentication: <span style="color:red">false</span> ou <span style="color:blue">true</true>, a autenticação anônima dá aos usuários acesso às áreas públicas do seu site da Web ou FTP sem solicitar um nome de usuário ou senha;
  - dotnetRunMessages: <span style="color:red">false</span> ou <span style="color:blue">true</true>, oferecer um pronto feedback ao programador após a aplicação ser colocada para rodar e ocorra alguma alteração;
  - launchBrowser: informa se após a aplicação entrar em funcionamento após o `dotnet run` ou `dotnet watch`, o browser será aberto automaticamente na aplição;
  - applicationUrl: informa a URL local em que a aplicação irá rodar, como por exemplo "http://localhost:5234"


[^1]: O middleware é um software montado em um pipeline de aplicativo para manipular solicitações e respostas. Os delegados de solicitação são configurados usando os métodos de extensão Run, Map e Use.
### 4.1 Rota

As rotas das páginas no razor são definidas no arquivo *nome.razor* logo na primeira linha, após o código `@page "/nomedarota"`. Será esse "nomedarota" que aparecerá na barra de endereço do navegador, logo após o nome completo do domínio.

```cake
@page "/nomedarota"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.
```

## 5    Modificações 

### 5.1 Incorporação de componente


### 5.2 Passagem de parâmetro

```cake
    @page "/"

    <h1>Hello, world!</h1>

    Welcome to your new app.

    <Counter IncrementAmount="10" />
```

```cake
    @page "/counter"
    @rendermode InteractiveServer

    <PageTitle>Counter</PageTitle>

    @code {
        private int currentCount = 0;

        [Parameter]
        public int IncrementAmount { get; set; } = 1;

        private void IncrementCount()
        {
            currentCount += IncrementAmount;
        }
    }
```



## 6    Material de Suporte

- [Sintaxe básica de gravação e formatação no GitHub](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Criar e realçar blocos de código](https://docs.github.com/pt/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)


## 7    Agradecimento

- Microsoft
- IBGE

## Data

28 de março de 2024.