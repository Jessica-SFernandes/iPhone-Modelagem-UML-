# iPhone-Modelagem-UML-
Atividade Beck-and em Java - DIO e Santander.

# 📱 iPhone — Modelagem UML & Implementação em Java

Este projeto é um desafio de **POO (Programação Orientada a Objetos)** que modela o **iPhone** com suas principais funcionalidades apresentadas no lançamento de 2007:

- 🎵 **Reprodutor Musical**
- 📞 **Aparelho Telefônico**
- 🌐 **Navegador na Internet**

---

## 📊 Diagrama UML

Diagrama em **UML padrão**, modelando a classe `iPhone` e as interfaces implementadas:

```mermaid
classDiagram
    direction LR

    class ReprodutorMusical {
        <<interface>>
        +tocar() void
        +pausar() void
        +selecionarMusica(musica : String) void
    }

    class AparelhoTelefonico {
        <<interface>>
        +ligar(numero : String) void
        +atender() void
        +iniciarCorreioVoz() void
    }

    class NavegadorInternet {
        <<interface>>
        +exibirPagina(url : String) void
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
        +selecionarMusica(musica : String) void
        +ligar(numero : String) void
        +atender() void
        +iniciarCorreioVoz() void
        +exibirPagina(url : String) void
        +adicionarNovaAba() void
        +atualizarPagina() void
    }

    iPhone ..|> ReprodutorMusical
    iPhone ..|> AparelhoTelefonico
    iPhone ..|> NavegadorInternet
