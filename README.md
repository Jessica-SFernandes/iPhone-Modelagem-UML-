# iPhone-Modelagem-UML-
Atividade Beck-and em Java - DIO e Santander.

# iPhone — Modelagem UML

Este projeto é um desafio de **POO (Programação Orientada a Objetos)** que modela o **iPhone** com suas principais funcionalidades apresentadas no lançamento de 2007:

**Reprodutor Musical** 🎶
**Aparelho Telefônico** 📱
**Navegador na Internet** 🧭

---

## 📊 Diagrama UML

Diagrama em **UML padrão**, modelando a classe `iPhone` e suas interfaces:

```mermaid
classDiagram
    direction LR

    class ReprodutorMusical {
        +tocar() void
        +pausar() void
        +selecionarMusica(String musica) void
    }

    class AparelhoTelefonico {
        +ligar(String numero) void
        +atender() void
        +iniciarCorreioVoz() void
    }

    class NavegadorInternet {
        +exibirPagina(String url) void
        +adicionarNovaAba() void
        +atualizarPagina() void
    }

    class iPhone {
        -musicaAtual : String
        -emLigacao : boolean
        -abasAbertas : int
        +iPhone()
        +tocar() void
        +pausar() void
        +selecionarMusica(String musica) void
        +ligar(String numero) void
        +atender() void
        +iniciarCorreioVoz() void
        +exibirPagina(String url) void
        +adicionarNovaAba() void
        +atualizarPagina() void
    }

    iPhone ..|> ReprodutorMusical
    iPhone ..|> AparelhoTelefonico
    iPhone ..|> NavegadorInternet
