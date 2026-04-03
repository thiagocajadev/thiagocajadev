# Profile Governance: Thiago Caja Dev (v2.2.0)

Este documento estabelece a **Governança Técnica** deste repositório, garantindo que cada atualização siga o ciclo de vida de alta disciplina que adoto em meus projetos de engenharia.

O perfil não é apenas um README; ele é o resultado de um processo **Spec-Driven** rigoroso.

---

## 🏗️ O Ciclo SDLC (Spec-Driven Development Lifecycle)

Adoto um fluxo de 5 fases obrigatórias que removem a incerteza e garantem a qualidade do "Output" final.

### 1. Phase: SPEC (O Contrato)

**Objetivo:** Definir _o que_ será alterado e _como_ será validado antes de qualquer edição.

- **Ação:** Criação de um rascunho de intenção (Spec).
- **Hard Rule**: O Agente de IA **deve parar** e aguardar aprovação explícita da Spec antes de prosseguir.
- **Checklist de Verificação**: Critérios binários (Passa/Falha) para o sucesso da tarefa.

### 2. Phase: PLAN (A Estratégia)

**Objetivo:** Decompor a Spec aprovada em uma sequência de tarefas atômicas e executáveis.

- **Ação**: Criação de um `task.md` temporário com o roadmap de implementação.
- **Decomposição**: Tarefas complexas são divididas para evitar perda de contexto.

### 3. Phase: CODE (A Execução)

**Objetivo:** Implementar o plano seguindo os padrões de **Visual Excellence** e **High-Level Engineering**.

- **Padrões**: Uso de HTML semântico dentro do MD, paletas de cores harmônicas (Nordic Staff) e estrutura inclusive/acessível.
- **SDD Native**: O código (Markdown) é o subproduto de uma especificação bem pensada.

### 4. Phase: TEST (A Verificação)

**Objetivo:** Garantir que a implementação respeite o **Verification Checklist** da Fase 1.

- **Ação**: Verificação visual, testes de links e responsividade mobile.
- **Refactor Loop**: Se um critério falhar, o ajuste é feito imediatamente até o "Pass".

### 5. Phase: END (A Entrega)

**Objetivo:** Finalizar a tarefa e documentar a evolução.

- **Ação**: Atualização do Walkthrough e registros de versão.
- **Git Semantic**: Commits que seguem o padrão convencional (`feat`, `fix`, `docs`).

---

## ⚖️ Princípios de Design e Estética

1. **🔒 Hardening**: Segurança de links e proteção de dados sensíveis.
2. **🚦 Resilience**: Links e assets devem ter resiliência em diferentes visualizadores de Markdown.
3. **🌊 The Cascade**: A informação flui do mais importante para o detalhamento técnico.
4. **💎 Visual Excellence**: O design não é cosmético; é o que gera autoridade técnica.

---

_Assinado: Thiago Caja - Desenvolvedor_
