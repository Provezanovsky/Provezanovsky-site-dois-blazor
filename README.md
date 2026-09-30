# SiteDoisBlazor

Projeto acadêmico em **C# / Blazor Web App (.NET 8)**, com componentes interativos renderizados no servidor.

## Atividades

| Página | Rota | Funcionalidade |
| --- | --- | --- |
| Conversor | `/conversor` | Conversão de Celsius para Fahrenheit: `(C × 9 / 5) + 32`. |
| Calculadora de Média | `/media` | Média de duas notas; aprovado com média maior ou igual a 7,0. |
| Sorteador | `/sorteio` | Geração de um número inteiro entre 1 e 100, inclusive. |

As três páginas incluem `@rendermode InteractiveServer` na segunda linha, logo abaixo de `@page`. O menu lateral utiliza `NavLink` para acessar todas as atividades.

## Pré-requisitos

- [SDK do .NET 8](https://dotnet.microsoft.com/download/dotnet/8.0).
- Para executar no Visual Studio: Visual Studio 2022 (17.8 ou superior), com a carga de trabalho **ASP.NET e desenvolvimento Web**.

## Executar pelo terminal

Na pasta do repositório:

```bash
dotnet restore SiteDoisBlazor.sln
dotnet watch --project SiteDoisBlazor --launch-profile http
```

Abra **http://localhost:5180** e navegue pelos links do menu lateral.

## Estrutura

- `SiteDoisBlazor/Components/Pages/`: páginas dos exercícios.
- `SiteDoisBlazor/Components/Layout/NavMenu.razor`: menu de navegação.
- `SiteDoisBlazor/Program.cs`: configuração da interatividade no servidor.
- `.gitignore`: modelo do Visual Studio.
- `LICENSE`: licença MIT.

## Roteiro de verificação

1. Acesse **Conversor** pelo menu: `0 °C → 32 °F`, `100 °C → 212 °F`, `−40 °C → −40 °F`.
2. Acesse **Calculadora de Média**: notas `8` e `6` resultam em média `7` e **Aprovado!** em verde; notas `5` e `6` resultam em média `5,5` e **Reprovado!** em vermelho. O resultado fica oculto antes do primeiro cálculo.
3. Acesse **Sorteador**: clique em **Gerar Número Aleatório** e confirme um inteiro entre `1` e `100`. Repetições são possíveis em um sorteio aleatório.
4. Volte para **Início** pelo menu, sem digitar rotas manualmente.

## Autor e licença

Rafael Provezano. Distribuído sob a [licença MIT](LICENSE).
