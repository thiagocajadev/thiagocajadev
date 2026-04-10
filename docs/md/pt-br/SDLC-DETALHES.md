# Minha Esteira de Desenvolvimento (8 Passos)

Esse guia documenta como organizo um projeto de software do início à operação contínua. Não é receita de bolo, é o padrão que me ajuda a não esquecer o que importa.

A ordem tem lógica. Cada passo cria a base para o próximo funcionar com segurança. Mas todo projeto tem contexto: uma CLI não precisa de controle de acesso; um SaaS precisa do pipeline completo. Use o que faz sentido, na ordem que faz sentido.

`FUNDAÇÃO` → `SEGURANÇA` → `CI/CD` → `CONTROLE DE ACESSO` → `DESIGN SYSTEM` → `DOMÍNIO` → `PRODUÇÃO` → `OPERAÇÕES`

> Obs: a ordem pode variar conforme o tipo de projeto, escopo e divisão de equipes. O importante é ter clareza sobre cada etapa e garantir que todas sejam executadas.

---

## 01 — Fundação

Antes de qualquer código de negócio, o projeto precisa ter uma estrutura que qualquer desenvolvedor — inclusive eu daqui a seis meses — consiga entender e rodar sem precisar perguntar nada.

- `.editorconfig` e linter configurados. Nada de "funciona na minha máquina".
- `README.md` com instruções reais de setup — não a versão de vitrine, a versão funcional.
- `.gitignore` blindado: `.env*`, artefatos de build, pastas de IDE. Nenhum segredo entra no histórico.
- Variáveis de ambiente centralizadas em `.env` com validação na inicialização.
- Rota `/health` desde o primeiro commit. Se não sobe limpo, já sei onde olhar.
- Arquivo de entrada (`Program.cs`, `main.ts` ou equivalente) como orquestrador — mostra o fluxo, não implementa detalhes.
- Scripts de setup que rodam com um único comando (`npm run dev`, `dev.sh`). Reduz fricção e padroniza o fluxo.

**Pronto quando:** qualquer pessoa do time consegue clonar, configurar e rodar o projeto em menos de 5 minutos.

---

## 02 — Observabilidade e Segurança

Segurança não é feature. É a camada que protege tudo que vem depois.

Essa fase existe porque já vi projetos quebrarem em produção sem deixar rastro. Log sem contexto é inútil. Request sem ID é um pesadelo de diagnóstico.

- Validação de todos os inputs externos na borda (body, query params, headers). Dados inválidos são rejeitados antes de entrar no sistema.
- Logs estruturados em JSON com request ID, timestamp e severidade. Nunca logar secrets ou dados pessoais.
- Rota `/health` validando a conectividade com dependências (banco, cache, serviços externos).
- Headers de segurança: HSTS, CSP, rate limiting. Proteção antes de precisar, não depois.
- Se aplicável: tracing distribuído (OpenTelemetry) para seguir um request entre serviços.

**Pronto quando:** consigo responder "a aplicação está saudável?" e "o que aconteceu com o request X?" sem abrir o código.

---

## 03 — Pipeline de CI/CD

Entregar código com segurança não é sorte. É automação bem configurada.

O objetivo é simples: código quebrado não chega em produção. Review humano é para lógica de negócio, não para verificar se o build passa.

- Ambientes definidos: local, staging, produção. As diferenças entre eles documentadas.
- Segredos gerenciados no lugar certo (CI secrets, vault). Nada hardcoded no código.
- CI ativo em todo PR: linter + testes + build. PR bloqueado se qualquer gate falhar.
- CD definido: como o código vai do PR para staging e, depois, para produção. Staging automatizado, produção com aprovação quando necessário.

**Pronto quando:** um PR não pode ser mergeado sem passar por todos os gates. Deploy em staging é uma ação.

---

## 04 — Controle de Acesso (quando aplicável)

Autenticação e autorização definem quem vê o quê. Isso não é detalhe de implementação — é decisão arquitetural que afeta tudo que vem depois.

Antes de construir qualquer feature que dependa de permissões, preciso saber: quem pode fazer o quê e por quê.

- Estratégia de identidade definida para o contexto: Magic Link para baixa fricção, OAuth para B2B, passkeys para segurança crítica.
- Papéis e permissões modelados desde o início. Começo simples (admin/usuário) e expando quando necessário. Padrão: bloqueio por padrão.
- Tokens seguros: cookies HttpOnly para web, JWTs de curta duração com refresh rotation. Proteção contra XSS e CSRF.
- CRUD de usuário como primeira feature real — a que exercita o pipeline completo de ponta a ponta.

**Pronto quando:** consigo criar usuário, autenticar, acessar uma rota protegida e ser rejeitado em uma rota sem permissão.

---

## 05 — Design System e Interface (quando aplicável)

Interface inconsistente passa uma mensagem clara para o usuário: ninguém revisou isso com cuidado.

Design System não é frescura de frontend, é o que evita que cada desenvolvedor invente um botão diferente.

- Tokens de design definidos: cores, espaçamento (sistema de 4/8px), tipografia, bordas.
- Tema claro e escuro. Variáveis CSS ou sistema utilitário (ex: Tailwind).
- Contraste WCAG garantido. Acessibilidade não é opcional, é respeito ao usuário.
- Componentes base (Button, Input, Card, Modal) construídos antes das telas específicas.

**Pronto quando:** uma nova tela pode ser construída com tokens e componentes existentes, sem estilização ad-hoc.

---

## 06 — Evolução de Features (Domínio)

Aqui entra o código de negócio de verdade. E é onde a maioria dos projetos acumula débito técnico quando não há disciplina.

Nenhuma lógica complexa é codificada sem uma especificação prévia que valide as regras de negócio. O código segue a spec, não o contrário.

- Modelagem de domínio primeiro: entidades, objetos de valor, agregados. Nomes em linguagem de negócio, não jargão técnico.
- Casos de uso como orquestradores: chamam validadores, lógica de domínio e repositórios. Sem detalhes de implementação misturados.
- Feature flags para qualquer coisa arriscada ou incompleta. Vai para produção desabilitado, valida, habilita.
- Refatoração contínua: se um módulo cresceu além da responsabilidade dele, divide agora. Não existe "sprint de refatoração" que resolve depois.

**Pronto quando:** cada feature é isolada, testável e pode ser revertida ou desabilitada de forma independente.

---

## 07 — Prontidão para Produção

Antes de ir ao ar, tem uma checklist que precisa ser verificada. Sempre.

Deploy na sexta à noite sem plano de rollback não é coragem, é imprudência.

- Checklist pré-deploy: variáveis de ambiente configuradas, secrets rotacionados, dependências atualizadas, flags de debug removidas.
- Migrations testadas no staging com plano de rollback documentado. Integridade dos dados validada.
- Smoke tests no staging: fluxo principal, fluxos de erro, casos de borda.
- Estratégia de deploy definida: blue/green, canary ou rolling. Rollback planejado para menos de 5 minutos.

**Pronto quando:** produção está no ar, monitorada, e existe uma forma documentada de reverter em menos de 5 minutos.

---

## 08 — Governança Operacional

O sistema foi para produção. Agora começa a parte que dura para sempre.

Monitoramento não é opcional, é o que diferencia um sistema profissional de um que "a gente descobre quando cai".

- Monitoramento ativo nas primeiras 24-48h após o deploy: taxa de erro, latência, uso de recursos.
- Protocolo de incidente definido: quem é acionado, como é a triagem, onde comunicar.
- Para problemas críticos: correção rápida se pequeno, rollback se grande. A decisão, documentada.
- CHANGELOG atualizado com o que mudou e por quê. Facilita auditorias e a comunicação com quem depende do sistema.
- Post-mortems focados no sistema, nunca em culpar pessoas. O que aconteceu, por quê aconteceu, o que muda.

**Pronto quando:** o time responde a um problema em produção sem entrar em pânico. Cada incidente deixa o sistema mais robusto.

---

_Assinado por: Thiago Cajaíba - Desenvolvedor_
