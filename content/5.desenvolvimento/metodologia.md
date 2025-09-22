---
title: Metodologia Ágil
description: Framework Scrum adaptado utilizado no desenvolvimento do MedPay Saúde
---

# Metodologia Ágil

O desenvolvimento do MedPay Saúde utilizou uma **metodologia ágil baseada em Scrum**, adaptada para as necessidades específicas de um projeto fintech no setor de saúde.

## 🎯 Framework Principal: Scrum Adaptado

### Por que Scrum?
- **Iterativo e incremental:** Entregas frequentes de valor
- **Transparência:** Visibilidade completa do progresso
- **Adaptação rápida:** Resposta ágil a mudanças
- **Foco no time:** Autonomia e responsabilidade compartilhada

### Adaptações para FinTech
- **Sprints de 2 semanas:** Ciclos mais curtos para feedback rápido
- **Dailies mais estruturados:** Foco em impedimentos técnicos
- **Definition of Done rigorosa:** Especialmente para compliance
- **Integração contínua obrigatória:** Zero tolerância a débitos técnicos

## 📅 Ritmos e Cerimônias

### Sprints de 2 Semanas
```
Semana 1: Desenvolvimento focado
Semana 2: Testes, refinamento e entrega
```

#### Planning Meeting (Segunda-feira, 2h)
**Participantes:** Product Owner, Scrum Master, Development Team
**Objetivos:**
- Refinar backlog do sprint
- Estimar esforços (story points)
- Comprometer entregas realistas
- Alinhar expectativas

#### Daily Standup (Terça-Sexta, 15min, 9h)
**Formato:** 3 perguntas clássicas + 1 técnica
- O que fiz ontem?
- O que farei hoje?
- Há impedimentos?
- **+ Status técnico:** Testes passando? Integrações funcionando?

#### Sprint Review (Sexta-feira, 1h)
**Participantes:** Stakeholders, Product Owner, Time
**Objetivos:**
- Demonstração das funcionalidades entregues
- Feedback direto dos usuários
- Validação dos critérios de aceitação
- Ajuste do product backlog

#### Sprint Retrospective (Sexta-feira, 30min)
**Participantes:** Apenas o time de desenvolvimento
**Objetivos:**
- O que funcionou bem?
- O que pode melhorar?
- Ações concretas para o próximo sprint
- Melhoria contínua da produtividade

## 📋 Ferramentas e Organização

### Jira + Confluence
**Jira para gestão:**
- Issues por funcionalidade
- Board Kanban integrado
- Relatórios de velocity
- Burndown charts automáticos

**Confluence para documentação:**
- Guias de desenvolvimento
- Documentação de APIs
- Padrões de código
- Lições aprendidas

### GitHub + Slack
**GitHub:**
- Pull requests obrigatórios
- Code review por pares
- Branches por feature
- Actions para CI/CD

**Slack:**
- Canais por domínio (frontend, backend, devops)
- Integração com Jira e GitHub
- Bots para notificações automáticas
- Arquivo de decisões técnicas

## 🏆 Definition of Done (DoD)

### Para Cada História de Usuário:
- [ ] **Código escrito** seguindo padrões estabelecidos
- [ ] **Code review aprovado** por pelo menos 1 peer
- [ ] **Testes unitários** com cobertura > 90%
- [ ] **Testes de integração** passando
- [ ] **Documentação atualizada** (APIs, guias)
- [ ] **Deploy homologação** funcionando
- [ ] **Aprovação Product Owner** nos critérios de aceitação
- [ ] **Sem bugs críticos** identificados

### Para Releases:
- [ ] **Testes E2E** passando em todos os fluxos
- [ ] **Performance validada** (métricas baseline)
- [ ] **Segurança auditada** (vulnerabilidades críticas = 0)
- [ ] **Compliance verificada** (LGPD, PCI DSS)
- [ ] **Documentação completa** para usuários e devs

## 👥 Estrutura do Time

### Product Owner (PO)
**Responsabilidades:**
- Priorização do backlog
- Validação de entregas
- Comunicação com stakeholders
- Definição de critérios de aceitação

### Scrum Master
**Responsabilidades:**
- Remoção de impedimentos
- Facilitação das cerimônias
- Coaching ágil do time
- Melhoria contínua dos processos

### Development Team (8 pessoas)
**Composição:**
- 3 Frontend Developers (React/Next.js)
- 3 Backend Developers (Node.js/Python)
- 1 DevOps Engineer
- 1 QA Engineer

**Características:**
- **Multidisciplinar:** Full-stack quando necessário
- **Autônomo:** Decisões técnicas próprias
- **Responsável:** Compromisso com entregas
- **Colaborativo:** Pair programming e code reviews

## 📊 Métricas de Agilidade

### Velocity do Time
- **Sprint 1-3:** 85 story points (aprendizado)
- **Sprint 4-6:** 95 story points (estabilidade)
- **Sprint 7-9:** 105 story points (produtividade)
- **Sprint 10-12:** 110 story points (pico)

### Qualidade de Código
- **Code coverage:** 92% médio
- **Tempo de build:** < 8 minutos
- **Tempo de deploy:** < 15 minutos
- **Bugs em produção:** 0 (meta atingida)

### Satisfação do Time
- **Retrospectives:** Ações implementadas em 100%
- **Daily standups:** 95% de participação
- **Code reviews:** Tempo médio < 4 horas
- **Pair programming:** 30% das tarefas críticas

## 🔄 Melhorias Implementadas

### Durante o Projeto
1. **Daily mais eficiente:** Foco em impedimentos técnicos
2. **Branching strategy:** Git flow adaptado para CI/CD
3. **Testing strategy:** Shift-left com TDD em componentes críticos
4. **Documentation:** Living documentation com Swagger + Confluence

### Resultados Obtidos
- **Previsibilidade:** Velocity consistente nos últimos sprints
- **Qualidade:** Zero bugs críticos em produção
- **Velocidade:** Deploy diário possível
- **Motivação:** Time engajado e produtivo

Esta metodologia ágil adaptada permitiu o desenvolvimento bem-sucedido do MedPay Saúde, entregando um produto de alta qualidade dentro do prazo e orçamento previstos.