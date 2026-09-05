# 🛠️ ControleChamadosTI — Backend

API REST do sistema web de gerenciamento de **equipamentos, patrimônio e chamados de TI**.

Desenvolvida em **C# / ASP.NET Core**, com **Entity Framework Core** e **PostgreSQL**, e preparada para execução utilizando **Docker**.

## 🚀 Tecnologias

![C#](https://img.shields.io/badge/C%23-512BD4?style=flat&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=flat&logo=dotnet&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-512BD4?style=flat&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

## 📌 Sobre o projeto

O backend foi desenvolvido como uma **API REST**, buscando manter uma separação clara entre as responsabilidades da aplicação.

A arquitetura atualmente utiliza principalmente as camadas:

```text
Controller
    ↓
Service / IService
    ↓
Entity Framework Core
    ↓
PostgreSQL
```

Essa separação permite concentrar as regras de negócio nos Services (atualmente em correção), mantendo os Controllers focados no fluxo HTTP da aplicação.

## 🧩 Princípios de desenvolvimento

O projeto aplica alguns princípios do **SOLID**, principalmente:

- **SRP — Single Responsibility Principle**
- **DIP — Dependency Inversion Principle**

As interfaces dos Services também permitem trabalhar com **Dependency Injection**, reduzindo o acoplamento entre os componentes da aplicação.

## 🗄️ Banco de dados

A persistência é realizada utilizando:

- **PostgreSQL** como banco de dados relacional;
- **Entity Framework Core** como ORM;
- **Migrations** para versionamento da estrutura do banco.

As migrations são aplicadas durante o processo de deploy, mantendo a estrutura do banco sincronizada com a aplicação.

## 🐳 Deploy

A aplicação é preparada para execução em containers utilizando **Docker**.

O objetivo é manter o ambiente de execução reproduzível e facilitar o processo de deploy da API e de suas dependências.

## 🧪 Testes

A implementação de **testes automatizados** está prevista como uma próxima etapa do projeto, incluindo testes unitários dos Services e testes de integração da API.

## 🔗 Projeto relacionado

Este backend possui um frontend desenvolvido separadamente:

👉 **[ControleChamadosTI — Frontend](https://github.com/LucasFonteneleDev/gerenciamento_ti_front)**

---

### 📚 Objetivo

Além de atender à necessidade de gerenciamento de equipamentos e chamados de TI, o projeto é utilizado como **laboratório para aplicação prática de conceitos de desenvolvimento de software**, incluindo arquitetura em camadas, SOLID, ORM, banco de dados, APIs REST e containerização.