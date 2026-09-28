# Kofi Aroma ☕

> Uma plataforma pessoal para entusiastas de café especial registrarem, lembrarem e entenderem suas experiências com café.

## Sobre o projeto

Kofi Aroma é um produto B2C voltado inicialmente para o seguinte ICP:

**Entusiasta de café especial que prepara café em casa.**

A proposta é transformar o registro de experiências com café em algo simples e útil ao longo do tempo.

O produto não busca apenas armazenar informações sobre cafés. A ideia central é ajudar o usuário a:

- registrar cafés experimentados;
- registrar experiências de preparo;
- lembrar dos cafés que já experimentou;
- identificar padrões de preferência;
- compreender melhor o próprio paladar;
- receber insights personalizados a partir do próprio histórico.

## Proposta do produto

O Kofi Aroma parte de três ações principais:

**Registrar → Lembrar → Entender**

O produto utiliza os dados e comportamentos registrados pelo próprio usuário para construir uma camada de personalização.

Essa personalização será inicialmente baseada em **regras, comportamentos e dados estruturados**, sem depender obrigatoriamente de uma API externa de inteligência artificial.

## ICP inicial

### Entusiasta de café especial que prepara café em casa

É o usuário que:

- gosta de café especial;
- prepara café em casa;
- experimenta diferentes cafés;
- presta atenção em métodos e características;
- possui interesse em entender melhor suas próprias preferências;
- pode ter dificuldade para lembrar quais cafés já experimentou e como foi cada experiência.

## MVP

O MVP será centrado em quatro pilares:

### 1. Coffee

Registro dos cafés experimentados pelo usuário.

### 2. Experience

Registro da experiência do usuário com determinado café e preparo.

### 3. Taste

Construção progressiva do perfil de paladar do usuário a partir das experiências registradas.

### 4. Personalization

Motor de personalização baseado inicialmente em regras e comportamento.

O objetivo é transformar os dados registrados em informações úteis para o próprio usuário.

## Personalization Engine

O Personalization Engine será uma camada de regras responsável por interpretar os dados existentes no sistema.

Exemplos futuros:

- identificar características recorrentes nos cafés bem avaliados;
- identificar métodos mais utilizados;
- encontrar padrões de preferência;
- gerar recomendações baseadas no histórico;
- produzir insights personalizados.

A primeira versão não depende necessariamente de inteligência artificial generativa.

A lógica será construída dentro do próprio sistema e poderá evoluir posteriormente.

## Newsletter

O produto poderá possuir uma newsletter como recurso de um plano superior.

A newsletter será enviada por e-mail e poderá utilizar os dados e comportamentos registrados pelo usuário para produzir conteúdo personalizado relacionado à sua jornada com café.

## Arquitetura

O projeto utiliza uma arquitetura organizada por responsabilidades.

```text
src/
├── app/
├── application/
├── components/
├── domain/
├── infrastructure/
├── lib/
└── types/
Camadas
app

Responsável pela aplicação Next.js, rotas e composição das páginas.

components

Componentes de interface reutilizáveis.

application

Casos de uso e orquestração das operações da aplicação.

domain

Regras e conceitos centrais do negócio.

domain/
├── coffee/
├── experience/
├── personalization/
└── taste/
infrastructure

Implementações relacionadas a recursos externos.

infrastructure/
├── auth/
├── database/
├── repositories/
└── storage/
lib
##
Bibliotecas auxiliares, validações e configurações.

types

Tipos compartilhados quando necessário.

Frontend

O projeto utiliza:

Next.js
React
TypeScript
Tailwind CSS

A aplicação será construída priorizando componentes leves e mantendo lógica complexa fora da camada visual sempre que possível.

Backend / Data

O projeto utiliza:

Supabase
PostgreSQL
Prisma ORM

O Supabase será utilizado como infraestrutura para o banco PostgreSQL e demais serviços que forem necessários.

O Prisma será responsável pela camada de acesso e modelagem do banco dentro da aplicação.

Tecnologias
Tecnologia	Função
Next.js	Framework principal
React	Interface
TypeScript	Tipagem
Tailwind CSS	Estilização
Supabase	Backend / PostgreSQL / serviços
PostgreSQL	Banco de dados
Prisma	ORM
Zod	Validação
React Hook Form	Formulários
Estrutura atual
kofi-aroma/
│
├── prisma/
│   └── schema.prisma
│
├── src/
│   ├── app/
│   ├── application/
│   │   ├── coffee/
│   │   ├── experience/
│   │   ├── insight/
│   │   └── profile/
│   │
│   ├── components/
│   │   ├── coffee/
│   │   ├── experience/
│   │   ├── profile/
│   │   └── ui/
│   │
│   ├── domain/
│   │   ├── coffee/
│   │   ├── experience/
│   │   ├── personalization/
│   │   └── taste/
│   │
│   ├── infrastructure/
│   │   ├── auth/
│   │   ├── database/
│   │   ├── repositories/
│   │   └── storage/
│   │
│   ├── lib/
│   │   ├── supabase/
│   │   ├── utils/
│   │   └── validation/
│   │
│   └── types/
│
├── prisma.config.ts
├── .env
├── package.json
└── README.md
Estado do projeto
Concluído
 Definição do nicho
 Definição do ICP inicial
 Jornada do ICP
 Product Brief
 MVP inicial
 Domain Model
 Personalization Engine
 ERD / Database Model v0
 API Contract
 Technical Stack
 Criação do projeto Next.js
 Estrutura inicial da arquitetura
 Instalação das dependências
 Projeto Supabase criado
 Prisma 7.10.0 configurado
 Prisma Client configurado
 Prisma Client gerado
Próximos passos
 Finalizar conexão Prisma ↔ Supabase PostgreSQL
 Criar configuração do Prisma Client
 Transformar o ERD v0 em schema.prisma
 Criar primeira migration
 Configurar Supabase Auth
 Configurar RLS
 Implementar repositories
 Implementar primeiros casos de uso
 Construir primeiras telas do MVP
Princípios técnicos

O projeto seguirá alguns princípios:

Manter a lógica de negócio fora dos componentes de UI.
Evitar lógica complexa desnecessária no frontend.
Centralizar acesso a dados na camada de infraestrutura.
Manter o domínio independente de tecnologias específicas.
Utilizar o backend para processamento e regras mais complexas.
Construir o Personalization Engine de forma incremental.
Priorizar simplicidade no MVP.
Evoluir a arquitetura conforme necessidades reais do produto.
Status

Em desenvolvimento — Bootstrap inicial

Kofi Aroma está atualmente na etapa de configuração da infraestrutura e preparação para implementação do MVP.