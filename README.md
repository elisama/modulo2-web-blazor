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

- *App.razor*:

- *Routes.razor*:

- *BlazorApp.csproj*:

- *lauchSettings.json* ou *appsettings.json*:

[^1]: O middleware é um software montado em um pipeline de aplicativo para manipular solicitações e respostas. Os delegados de solicitação são configurados usando os métodos de extensão Run, Map e Use.
### 4.1 Rota
```cake
@page "/"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.
```

## 5    Modificações 


## 6    Material de Suporte

- [Sintaxe básica de gravação e formatação no GitHub](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Criar e realçar blocos de código](https://docs.github.com/pt/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)


## 7    Agradecimento

- Microsoft
- IBGE

## Data

28 de março de 2024.