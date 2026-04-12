![Thiago Caja Dev Header](docs/assets/img/thiagocajadev-github-header-banner-v8.png)

# Seja bem-vindo(a) <img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" alt="Hand Wave" />

[**🇺🇸 English Version**](docs/md/en/README.en.md)

Olá **Dev**, **Tech Recruiter** e **entusiasta do código**!

Sou o **Thiago Cajá**. Comecei na Tecnologia em **2007**, passando pelo suporte técnico e administração de servidores. Foi criando meus primeiros scripts `.bat` para automatizar tarefas repetitivas que entendi o valor de ganhar tempo e eficiência. Desde então, busco sempre por melhoria continua.

Explorei diferentes linguagens, como Java, VB e PHP, até me encontrar no ecossistema **.NET (C#)**. Liderar um time de suporte (**Helpdesk**) me ensinou algo para a vida: nunca é só o computador ou o sistema que está com problema. O código é apenas uma ferramenta para resolver dores de pessoas reais e garantir que os processos fluam com tranquilidade.

Hoje, utilizo uma **stack moderna** (**.NET**, **React**, **Docker**, **Postgres**) unindo a solidez da engenharia de software com a agilidade do mundo **AI-Native**. Minha meta é construir sistemas robustos e seguros, sempre buscando simplificar e facilitar a rotina de desenvolvedores e usuários.

Eu nunca vou saber todas as respostas, mas sei pesquisar e buscar alternativas. Dificilmente me consideraria Senior ou Especialista. Prefiro ser um **Resolvedor de Problemas**.

> [!IMPORTANT]
> **"Evite o complexo, prefira o simples e sofisticado"**

[![Status](https://img.shields.io/badge/Status-Dispon%C3%ADvel%20para%20Projetos-success?style=for-the-badge&logo=github)](mailto:contato@thiagocaja.dev)

<details>
<summary><b> 📖 Um pouco mais sobre mim</b></summary>

<br>

Valores que guiam minha jornada: **Humildade**, **Trabalho**, **Sinceridade** e **Dedicação**.
<br>

Essa aqui é a minha "rede social" favorita de longe! Mais códigos e menos papo furado 😄.
<br>

Meu propósito de vida é ajudar. Percorro esse caminho via TI, consertando e construindo coisas.
<br>

> **"Em tempos de IA, pratique a IE (Inteligência Emocional)."**
>
> Decisões devem ser tomadas com base em dados e não achismos.

Está começando a utilizar a metodologia SDD (Spec-Driven Development) nos projetos? Esse guia pode te ajudar [specdrivenguide.org](https://specdrivenguide.org). Venha fazer parte!
<br>

Ultimamente faço um `dump` de pensamentos, escrevendo no meu [blog](https://thiagocaja.dev).
<br>

---

</details>

<details>
<summary><b> 👨🏻‍💻 Vamos falar de código</b></summary>

<br>

> "Código bom é aquele que conta a história de forma linear."

Tem que seguir a narrativa, mostrando passo a passo o que está acontecendo. Aplicações são feitas para resolver problemas, então o código deve refletir isso.

Programar é a última etapa. Primeiro, é definido o processo. Depois o planejamento e quais as tarefas a serem executadas, reduzindo a chance de falhas.

> **"Alinhamento de processo é fundamental para o sucesso do projeto."**

`PROCESSO` → `PLANEJAMENTO` → `TAREFAS` → `PROGRAMAÇÃO` → `TESTES` → `ENTREGA`

Se estou atuando em um projeto, preciso pensar em como ele será executado, mantido e evoluído. O próximo desenvolvedor que for atuar deve entender o código sem dificuldade e contar com uma documentação que esclarece as decisões técnicas. Os melhores profissionais são os que **geram valor para o negócio e pessoas**.
<br>

```js
// ✅ Código Narrativo
// Orquestrador no topo, detalhes agrupados (Lexical Scoping), densidade visual e nomes expressivos.

// Exemplo simplificado. O código conta a história, sem precisar de comentários.

await realizaVenda(123);

async function realizaVenda(codigoDoPedido) {
  const detalhesDoPedido = buscaPedido(codigoDoPedido);
  if (pedidoInvalido(detalhesDoPedido)) return;

  const notaFiscalEmitida = emiteNotaFiscal(detalhesDoPedido);
  return notaFiscalEmitida;

  // Detalhes das funções sempre abaixo do fluxo principal

  function pedidoInvalido(detalhesDoPedido) {
    if (detalhesDoPedido === null || detalhesDoPedido.itens.length === 0)
      return true;

    if (detalhesDoPedido.cliente.inadimplente)
      return notificaInadimplencia(detalhesDoPedido);

    return false;
  }

  function emiteNotaFiscal(detalhesDoPedido) {
    aplicaDescontos(detalhesDoPedido);
    const notaFiscal = salvaPedido(detalhesDoPedido);
    return notaFiscal;
  }
}
```

O foco do código acima não é aplicação em si, mas sim demonstrar o código narrativo. Vou falar no próximo tópico sobre **anti-padrões** e **padrões** que procuro aplicar nos projetos.

---

</details>

<details>
<summary><b>⚠️ Anti-Padrões e Padrões</b></summary>

## Anti-Padrão: Código Espaguete

Acredito que ninguem saiba ou conheça tudo. Somos seres humanos e isso é uma caracteristica normal. Porém, uma coisa que certa é evitar aquilo que pode dar problema.

```js
// ❌ Versão espaguete do exemplo anterior, com o código todo misturado e sem conceitos.

realizaVenda(123);

function realizaVenda(x) {
  let resultado;
  // nomes ruins
  let p = buscaPedido(x);

  if (p != null) {
    if (p.itens && p.itens.length > 0) {
      if (!p.c.inadimplente) {
        // começa a fazer um monte de coisa no meio
        if (p.total > 100) {
          p.desconto = 10;
        } else {
          p.desconto = 0;
        }

        apply(p);

        function apply(p) {
          if (p.desconto) {
            p.total = p.total - p.desconto;
          }
        }

        let salvo = salvaPedido(p);

        if (salvo) {
          resultado = salvo;

          // lógica aleatória no meio
          if (Math.random() > 0.5) {
            console.log("Log qualquer");
          } else {
            console.warn("Outro log");
          }
        } else {
          resultado = null;
        }
      } else {
        // mais lógica aninhada com função no meio
        notify(detalhesDoPedido);
        resultado = false;

        // nomes ruins e mistura do português com inglês
        function notify(p) {
          console.log("cliente inadimplente", p?.cliente?.nome);
          return true;
        }
      }
    } else {
      resultado = undefined;
    }
  } else {
    resultado = null;
  }

  // código morto/confuso
  if (false) {
    console.log("nunca executa");
  }

  return resultado;

  function salva(p) {
    if (!p) return;
    if (p.total < 0) return null;
    return { ...p, salvo: true };
  }
}
```

Bom, sem condições de ver essa tortura. Por isso é bom evitar ao máximo esse tipo de código. Sei que em épocas passadas todos nós já escrevemos códigos ruins, mas hoje com o conhecimento disponível, é possível fazer melhor.

### 🚫 ANTI-PATTERNS

Os principais pontos:

1. Controle de fluxo caótico
2. Mistura de responsabilidades
3. Falta de contrato claro de dados e retorno

#### Nomes e legibilidade

- Nomes sem significado (`x`, `p`, `c`, `apply`)
- Mistura de idiomas (português + inglês)
- Falta de intenção explícita nos identificadores

#### Controle de fluxo

- Aninhamento excessivo (`if` dentro de `if`)
- Falta de early return
- Lógica condicional espalhada e difícil de seguir
- Uso de `!=` (coerção implícita)

#### Retorno e contrato

- Múltiplos tipos de retorno (`null`, `undefined`, `false`, objeto)
- Falta de contrato claro de retorno
- Fluxo baseado em `null`/`undefined`

#### Estrutura e design

- Função com múltiplas responsabilidades
- Regra de negócio misturada com persistência e log
- Funções declaradas dentro de outras sem necessidade (`apply`, `notify`, `salva`)
- Função não utilizada (dead code)
- Código inalcançável (`if (false)`)

#### Estado e mutabilidade

- Variável mutável compartilhada (`resultado`)
- Mutação direta de objeto (`p.total`, `p.desconto`)
- Acoplamento estrutural forte (`p.c.inadimplente`)

#### Side effects e imprevisibilidade

- Side effects no meio da lógica (`console.log`, `console.warn`)
- Comportamento não determinístico (`Math.random()`)

---

Abaixo mais alguns anti padrões comuns em projetos reais:

#### Modelagem e contrato de dados

- Boolean puro (`true/false`) em vez de Result estruturado
- Múltiplos tipos de retorno (null / undefined / false / objeto)
- “MegaResult” inflado com meta/status
- Campos vazios no envelope (`meta: {}`, `data: {}`)
- Misturar domínio com transporte (ex: Result + statusCode)
- `meta` como dump genérico
- Retorno com objeto anônimo sem contrato claro

#### UI / Frontend acoplado errado

- Fetch direto no componente
- API espalhada (sem `apiClient`)
- Lógica dentro de `useEffect`
- Transformação de dados dentro da UI
- `try/catch` espalhado na UI
- Result no state da UI
- Retorno inline complexo (JSX direto sem composição)
- Múltiplas fontes de verdade no state

#### Design de código

- Funções genéricas demais (`handle`, `process`, etc.)
- Funções com múltiplas responsabilidades
- ViewModel pesado / camada desnecessária
- Action redundante (CRUD simples sem valor)
- Duplicação de estrutura entre camadas
- Cache acoplado ao core
- Overengineering (abstração sem necessidade)

#### Fluxo e controle

- Exceptions como fluxo normal
- Lógica condicional caótica
- Falta de early return
- Código morto / inalcançável

#### Consistência e clareza

- Nomes sem intenção
- Mistura de idiomas
- Estruturas internas expostas (alto acoplamento)
- Side effects misturados com regra de negócio

---

## ✅ Padrões: Código limpo

As convenções, padrões e princípios são sempre melhores a longo prazo. Se foram inventados é porque faz sentido e resolvem problemas reais.

```js
// ✅ Código Narrativo
// Orquestrador no topo, detalhes agrupados (Lexical Scoping), densidade visual e nomes expressivos.

await realizaVenda(123);

async function realizaVenda(codigoDoPedido) {
  const detalhesDoPedido = buscaPedido(codigoDoPedido);
  if (pedidoInvalido(detalhesDoPedido)) return;

  const notaFiscalEmitida = emiteNotaFiscal(detalhesDoPedido);
  return notaFiscalEmitida;

  function pedidoInvalido(detalhesDoPedido) {
    if (detalhesDoPedido === null || detalhesDoPedido.itens.length === 0)
      return true;

    if (detalhesDoPedido.cliente.inadimplente)
      return notificaInadimplencia(detalhesDoPedido);

    return false;
  }

  function emiteNotaFiscal(detalhesDoPedido) {
    aplicaDescontos(detalhesDoPedido);
    const notaFiscal = salvaPedido(detalhesDoPedido);
    return notaFiscal;
  }
}
```

O mesmo código praticamente, mais facil de entender e manter. Seguir metodologias e sopa de letrinhas como DDD, TDD, BDD, SOLID, SRP, SOLID, YAGNI, etc... é importante, mas não é o foco principal. O foco principal é escrever código limpo e legível.

### ☑️ Patterns

Os principais pontos:

1. Fluxo simples e previsível
2. Separação de responsabilidades
3. Contratos claros e consistentes

#### Nomes e legibilidade

- Nomes descritivos e com intenção clara (`pedido`, `cliente`, `calcularDesconto`)
- Consistência de idioma no código
- Funções e variáveis autoexplicativas

#### Controle de fluxo

- Uso de early return para simplificar leitura
- Redução de aninhamento (flat code)
- Condições explícitas e previsíveis (`===`, `!==`)
- Fluxo linear e fácil de seguir

#### Retorno e contrato

- Retorno consistente (sempre o mesmo formato)
- Uso de Result/DTO bem definido
- Evitar `null`/`undefined` como controle de fluxo
- Contratos explícitos entre funções

#### Estrutura e design

- Funções com responsabilidade única (SRP)
- Separação clara de responsabilidades (domínio, persistência, side effects)
- Funções pequenas, reutilizáveis e testáveis
- Remoção de código morto
- Declaração de funções no nível adequado (fora quando possível)

#### Estado e mutabilidade

- Preferência por imutabilidade
- Evitar mutação direta de objetos compartilhados
- Variáveis com escopo mínimo e preferencialmente `const`
- Acesso via interfaces claras (baixo acoplamento)

#### Side effects e previsibilidade

- Side effects isolados (log, IO, etc.)
- Funções puras sempre que possível
- Comportamento determinístico (sem aleatoriedade no core)

#### Modelagem e contrato de dados

- Result estruturado e tipado
- Retorno consistente e previsível
- Separação entre domínio e transporte (ex: DTO ≠ HTTP)
- Contratos claros entre camadas
- Estruturas enxutas (sem campos vazios)
- Dados com significado (sem `meta` genérico)

#### UI / Frontend bem estruturado

- Uso de `apiClient` centralizado
- Fetch fora do componente (services/hooks)
- `useEffect` apenas para efeitos reais (não regra de negócio)
- UI focada em renderização
- Tratamento de erro centralizado
- State com única fonte de verdade
- Componentes pequenos e compostos

#### Design de código

- Funções específicas e nomeadas por intenção
- Separação clara de camadas
- Simplicidade antes de abstração
- Reutilização sem acoplamento
- Estrutura consistente entre camadas
- Cache desacoplado do core

#### Fluxo e controle

- Uso de guard clauses (early return)
- Fluxo previsível e linear
- Tratamento explícito de erros
- Eliminação de código morto

#### Consistência e clareza

- Padrão de nomenclatura definido
- Código coeso e legível
- Baixo acoplamento entre estruturas
- Side effects isolados e explícitos

Bom é isso! Agora com uma visão maior e com o foco em gestão de projetos e pessoas, vamos falar de governança no próximo tópico.

---

</details>

<details>
<summary><b>🏗️ Governança</b></summary>

### Governança Técnica

Governar significa ter o controle sobre o projeto e garantir seu ciclo de vida. Ferramentas como indicadores e monitoramento, embasam a tomada de decisões, direcionando as ações ideais no momento adequado.

Se eu tenho a visão de que algo começou a degradar e precisa de mais recursos, consigo ajustar antes que haja impacto.

Pra ter governança, aplicamos leis. As leis que considero fundamentais e procuro aplicar:

<p align="left"><img src="https://img.shields.io/badge/%F0%9F%94%92_Blindagem-Bloqueio_por_Padrão-9c4a3f?style=for-the-badge" alt="Blindagem - Bloqueio por padrão" /> <img src="https://img.shields.io/badge/%F0%9F%9A%A6_Resiliência-Falha_como_Valor-4a6b8c?style=for-the-badge" alt="Resiliência - Falha como valor" /> <img src="https://img.shields.io/badge/%F0%9F%8C%8A_A_Cascata-Código_Narrativo-5b8c6a?style=for-the-badge" alt="A Cascata - Código Narrativo" /> <img src="https://img.shields.io/badge/%F0%9F%92%8E_Excelência_Visual-Design_como_Código-6d5d83?style=for-the-badge" alt="Excelência Visual - Design como Código" /></p>

| Lei                   | Comentário Estratégico                                                          |
| :-------------------- | :------------------------------------------------------------------------------ |
| **Blindagem**         | **Segurança Profunda**: Blindagem de dados e postura _Bloqueio por Padrão_.     |
| **Resiliência**       | **Gestão de Falhas**: Centraliza e padroniza o tratamento de erros.             |
| **Narrativa**         | **Código Documentativo**: O processo codificado de forma linear, passo a passo. |
| **Excelência Visual** | **Design Intuitivo**: Interfaces bonitas e fáceis de usar.                      |

Com entendimento de governança, seguimos para o gerenciamento do **Ciclo de Vida do Desenvolvimento de Software (SDLC)**.

### Ciclo de vida do Desenvolvimento de Software - SDLC

Para um desenvolvimento saudável, precisamos distinguir dois momentos:

**Projeto: O Nascimento**
É o esforço com início, meio e fim. O foco é transformar uma ideia em um produto funcional. Um bom projeto já nasce prevendo a sustentação, evitando que a pressa de hoje vire o débito técnico e o custo excessivo de amanhã.

**Processo: A Vida Continua**
É o fluxo cíclico e permanente. Enquanto o projeto entrega a solução, o processo garante que o produto continue evoluindo e gerando valor. É a rotina que mantém o software atualizado, seguro e eficiente para o investidor e para o usuário.

Abaixo listo 8 passos que considero fundamentais para um desenvolvimento saudável:

`FUNDAÇÃO` → `SEGURANÇA` → `INTEGRAÇÃO CONTÍNUA` → `CONTROLE DE ACESSO` → `TELA DO APLICATIVO` → `DOMÍNIO` → `PRODUÇÃO` → `OPERACÕES`

**Explicando em detalhes cada passo**: [Esteira de Ciclo de Vida](docs/md/pt-br/SDLC-DETALHES.md)

Para cada etapa desse ciclo, o ideal definir uma metodologia como guia. Abaixo falo sobre a escolha do **Desenvolvimento Guiado por Especificação (SDD)**.

### Desenvolvimento Guiado por Especificação - SDD

> **"A especificação guia o código, não o contrário."**

Agora com uma visão de processos, nada melhor do que definir a metodologia de trabalho. Vejo que o mercado se move para o fluxo de trabalho voltado a **IA Nativa.** O **SDD** - Desenvolvimento Guiado por Especificação, é um caminho promissor pro Desenvolvedor atuar em parceria com Agentes de IA. Abaixo as principais fases dessa abordagem:

**Esteira com 5 Fases**:
`ESPECIFICAÇÃO` → `PLANEJAMENTO` → `PROGRAMAÇÃO` → `TESTES` → `ENTREGA`

- **Explicando em detalhes cada fase e como aplicar**: [Detalhes do SDD](docs/md/pt-br/SDD-DETALHES.md)
- **Um exemplo de Especificação**: [Exemplo de Especificação](docs/md/pt-br/SPEC-EXEMPLO.md)

O Spec-Driven é um tipo de **Harness** (Aproveitamento de conhecimento), que utiliza os conceitos das especificações para aplicação em IA Nativa. O bom desenvolvedor acompanha a evolução de metodologias e complementos. Sempre penso em adicionar ao meu fluxo de trabalho melhorias, multiplicando com outros Devs.

---

</details>

<details>
<summary><b>💻 Minha Stack</b></summary>

### Backend & Core

![.NET](https://img.shields.io/badge/.NET-7e2bb3?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-68217A?style=for-the-badge&logo=csharp&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Hono](https://img.shields.io/badge/Hono-E36002?style=for-the-badge&logo=hono&logoColor=white)
![Minimal APIs](https://img.shields.io/badge/Minimal_APIs-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity_Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Dapper](https://img.shields.io/badge/Dapper-4B32C3?style=for-the-badge&logo=dotnet&logoColor=white)

### Frontend & UI

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor-5C2D91?style=for-the-badge&logo=blazor&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### Database & Cloud

![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

### Padrões & Qualidade

![Clean Code](https://img.shields.io/badge/Clean_Code-051937?style=for-the-badge&logo=readthedocs&logoColor=61DAFB)
![SOLID](https://img.shields.io/badge/SOLID-008793?style=for-the-badge&logo=codefactor&logoColor=white)
![TDD](https://img.shields.io/badge/TDD-E34F26?style=for-the-badge&logo=testinglibrary&logoColor=white)
![Result Pattern](https://img.shields.io/badge/Result_Pattern-e94560?style=for-the-badge&logo=codefactor&logoColor=white)
![DDD](https://img.shields.io/badge/DDD-f5a623?style=for-the-badge&logo=diagram&logoColor=black)

</details>

<details>
<summary><b>🤖 IAs & Ferramentas</b></summary>

### Generative AI

[![AntiGravity](https://img.shields.io/badge/AntiGravity-000000?style=for-the-badge&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)
[![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)](https://anthropic.com/claude)
[![ChatGPT Plus](https://img.shields.io/badge/ChatGPT_Plus-10a37f?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/chatgpt)
[![DeepSeek](https://img.shields.io/badge/DeepSeek-000000?style=for-the-badge&logo=deepnote&logoColor=white)](https://www.deepseek.com/)

### Dev Tools & Terminal

[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![JetBrains Rider](https://img.shields.io/badge/JetBrains_Rider-000000?style=for-the-badge&logo=jetbrains&logoColor=white)](https://www.jetbrains.com/rider/)
[![Starship](https://img.shields.io/badge/Starship-FF4081?style=for-the-badge&logo=starship&logoColor=white)](https://starship.rs/)
[![Docker Desktop](https://img.shields.io/badge/Docker_Desktop-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/products/docker-desktop/)

</details>

<details>
<summary><b>📚 Aprendizado & Dicas</b></summary>

### Aprendizado Contínuo

- [curso.dev](https://curso.dev) → Node.js/TypeScript
- [balta.io](https://balta.io) → Universo .NET
- [Anthropic](https://www.anthropic.com/learn) → Cursos de IA

### Dicas para seu Perfil GitHub

- [Header do perfil](https://leviarista.github.io/github-profile-header-generator/)
- [Escudos de tecnologia](https://shields.io/)
- [Estatísticas e cards](https://github.com/anuraghazra/github-readme-stats)
- [Troféus & Games](https://profile-readme-generator.com/)

</details>

---

# 📫 Contato

<p align="left">
  <a href="mailto:contato@thiagocaja.dev"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMiA2YzAtMS4xLS45LTItMi0ySDRDMi45IDQgMiA0LjkgMiA2djEyYzAgMS4xLjkgMiAyIDJoMTZjMS4xIDAgMi0uOSAyLTJWNnptLTIgMC04IDUtOC01aDE2em0wIDEySDRWOGw4IDUgOC01djEweiIvPjwvc3ZnPg==&logoColor=white" alt="Email" /></a>
  <a href="https://linkedin.com/in/thiagocajadev"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUySDE2Ljg5di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzktMS44NTItMy4wMzktMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2OUgxMC4zNTRWOUgxMi4zNTRWMTBhLjA0OS4wNDkgMCAwIDAgLjA0OSAwYy40NzctLjkgMS42MzctMS44NTIgMy4zNy0xLjg1MiAzLjYwMSAwIDQuMjY4IDIuMzcgNC4yNjggNS40NTV2Ni4yODh6TTUuMzM3IDcuNDMzYy0xLjE0NCAwLTIuMDYzLS45MjYtMi4wNjMtMi4wNjUgMC0xLjEzOC45Mi0yLjA2MyAyLjA2My0yLjA2MyAxLjE0IDAgMi4wNjMuOTI1IDIuMDYzIDIuMDYzIDAgMS4xMzktLjkyMyAyLjA2NS0yLjA2MyAyLjA2NXpNNy4xMTkgMjAuNDUySDMuNTU0VjloMy41NjV2MTEuNDUyWiIvPjwvc3ZnPg==&logoColor=white" alt="LinkedIn" /></a>
</p>

# 📈 Estatísticas

<div>
  <img align="center" src="https://visitor-badge.laobi.icu/badge?page_id=thiagocajadev.thiagocajadev&left_color=dodgerblue&right_color=slategray" alt="Visitor Counter" />
</div>
<br>

<span>
  <img height="200" src="https://github-readme-stats-v1-thiagocajadev.vercel.app/api?username=thiagocajadev&include_all_commits=true&show=prs_merged_percentage&hide=contribs&show_icons=true&hide_border=true&theme=github_dark_dimmed&rank_icon=github&cache_seconds=604800" />
</span>
<span>
  <img height="200" src="https://github-readme-stats-v1-thiagocajadev.vercel.app/api/top-langs?username=thiagocajadev&layout=compact&langs_count=8&card_width=370&hide_border=true&theme=github_dark_dimmed&cache_seconds=604800" />
</span>
<br><br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/thiagocajadev/thiagocajadev/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/thiagocajadev/thiagocajadev/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/thiagocajadev/thiagocajadev/output/pacman-contribution-graph.svg">
</picture>

# 📌 Projetos em Destaque

[![SDG Agents CLI](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=sdg-agents-cli&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/sdg-agents-cli)
[![Code Conventions](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=code-conventions&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/code-conventions)
[![SQL Conventions](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=sql-conventions&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/sql-conventions)
[![PayCheck BR](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=PayCheckBR&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/PayCheckBR)
[![Clone Tabnews](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=clone-tabnews&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/clone-tabnews)
[![Starship Bash](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=terminal-bash-one-dark-starship-profile&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/terminal-bash-one-dark-starship-profile)
[![Balta IO - BlazorIBGE](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=BlazorChallengeIBGEv2&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/BlazorChallengeIBGEv2)
[![Fleet MGMT](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=FleetMGMT&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/FleetMGMT)
