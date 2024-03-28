# Modulo 2: Web Blazor

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


## 3    Qual a versão .NET do SDK foi instalada?

Caso se digite os comandos acima, a versão instalada será a mais recente que estiver em sua máquina, a qual pode ser conferida pelo comando:

    `dotnet --list-sdks`

Versão instalada como sendo a mais recente da máquina.

<img width="680" alt="versao_framework" src="https://github.com/elisama/modulo2-web-blazor/assets/7691281/ea35b035-8dc4-4bc6-a8b0-d87a5250d3ba">

Agora, caso haja em sua máquina outras versões do .NET e deseje instalar a aplicação com essa versão, ex. .NET 5, basta executar o comando abaixo:

    `dotnet new blazor -f net5.0`

