---
title: LGPD e Privacidade
description: Implementação completa da LGPD no MedPay Saúde com foco no setor de saúde
---

# LGPD e Privacidade no Setor Saúde

O MedPay Saúde foi desenvolvido seguindo os mais rigorosos padrões de **Lei Geral de Proteção de Dados (LGPD)**, com atenção especial às particularidades do setor de saúde onde os dados são considerados de **dupla sensibilidade**.

## 🏥 Por que Saúde é Crítico para LGPD?

### Dados de Dupla Sensibilidade
Dados de saúde são classificados como **sensíveis** pela LGPD (art. 5º, II), exigindo nível máximo de proteção:

- **CPF + Dados Médicos** = Exposição legal amplificada
- **Prontuários + Transações Financeiras** = Combinação de alta criticidade
- **Histórico Clínico + Dados Pessoais** = Responsabilidade civil e criminal

### Penalidades Severas
O não cumprimento pode resultar em:
- **Multas** de até 2% do faturamento (limite R$ 50 milhões)
- **Responsabilidade civil** por danos morais e materiais
- **Risco reputacional** exponencial no setor saúde
- **Perda de confiança** de pacientes e parceiros

## 🎯 Nossa Abordagem: Privacy by Design Médico

### Pseudonimização de Dados
- **Tokenização de CPF** desde a entrada do sistema
- **Hashes irreversíveis** para dados identificadores
- **Chaves de criptografia** gerenciadas por HSM
- **Dados nunca em texto plano** no banco de dados

### Minimização de Dados
Coletamos apenas o essencial para processamento de pagamentos:
- **Dados obrigatórios:** Nome, CPF, data nascimento
- **Dados médicos mínimos:** Tipo de procedimento (não diagnóstico)
- **Dados financeiros:** Valor, forma de pagamento
- **Exclusão automática** após período de retenção

### Segregação de Bases de Dados
```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│ Dados Pessoais  │    │ Dados Médicos   │    │ Dados Financeiros│
│ (Tokenizados)   │    │ (Anonimizados)  │    │ (Criptografados) │
│ PostgreSQL      │    │ MongoDB         │    │ PostgreSQL       │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### Auditoria Completa
- **Logs imutáveis** de todas as operações
- **Rastreabilidade** durante todo ciclo de vida
- **Blockchain interno** para logs críticos
- **Relatórios de auditoria** mensais

## 📝 Consentimento Granular Inteligente

### Opt-in Específico
Para cada tipo de processamento, consentimento explícito:
- [ ] **Processamento de dados pessoais** para cadastro
- [ ] **Uso de dados médicos** para validação de procedimentos
- [ ] **Processamento financeiro** para pagamentos
- [ ] **Compartilhamento com prestadores** de saúde
- [ ] **Análise por IA** para anti-fraude

### Linguagem Clara em Português
- **Termos simplificados** sem jargões técnicos
- **Exemplos práticos** de uso dos dados
- **Consequências claras** da não autorização
- **Direito de arrependimento** explicado

### Revogação Facilitada
- **Um clique** para retirar qualquer consentimento
- **Efeito imediato** na revogação
- **Confirmação por e-mail** da alteração
- **Histórico completo** de consentimentos mantido

### Histórico de Consentimentos
Prova temporal de compliance:
- **Data e hora** de cada consentimento
- **Versão dos termos** aceita
- **IP e dispositivo** do usuário
- **Assinatura digital** do aceite

## 🔒 Controles Técnicos de Privacidade

### Criptografia Multi-Camada
- **AES-256 em repouso** para dados sensíveis
- **TLS 1.3 em trânsito** para todas as comunicações
- **Tokenização PCI DSS** para dados de cartão
- **HSMs dedicados** para gerenciamento de chaves

### Controles de Acesso
- **Princípio zero-trust** implementado
- **2FA obrigatório** para todos os usuários
- **RBAC granular** por funcionalidade específica
- **Timeouts automáticos** de sessão

### Monitoramento Proativo
- **SIEM personalizado** para detecção de anomalias
- **Machine learning** para padrões suspeitos
- **Alertas inteligentes** 24/7
- **Incident response** em menos de 4 horas

## 📋 Processo de Tratamento de Dados

### Etapas do Ciclo de Vida
1. **Coleta:** Apenas dados necessários com consentimento
2. **Processamento:** Pseudonimizado e criptografado
3. **Armazenamento:** Segregado por tipo e criticidade
4. **Uso:** Limitado ao propósito declarado
5. **Compartilhamento:** Apenas com autorização explícita
6. **Exclusão:** Automática após período definido

### Direitos dos Titulares (Art. 18 LGPD)
- ✅ **Confirmação da existência** de tratamento
- ✅ **Acesso aos dados** de forma clara
- ✅ **Correção de dados** incompletos/inaccurados
- ✅ **Anonimização/blocking** de dados desnecessários
- ✅ **Portabilidade** dos dados a outro fornecedor
- ✅ **Eliminação** de dados tratados com consentimento
- ✅ **Informação sobre compartilhamento** com terceiros
- ✅ **Revogação do consentimento** a qualquer momento

## 🏆 Certificações e Auditorias

### LGPD Compliance Auditada
- **Auditoria independente** trimestral
- **Gap analysis** anual completo
- **Penetration testing** focado em dados pessoais
- **Relatórios de conformidade** para stakeholders

### Métricas de Compliance
- **Taxa de consentimento:** 95%+ de aceitação
- **Tempo de resposta DPO:** < 24 horas
- **Incidentes de privacidade:** 0 registrados
- **Satisfação usuários:** 4.8/5 em privacidade

## 🚨 Plano de Resposta a Incidentes

### Classificação de Incidentes
- **Nível 1:** Vazamento potencial (resposta em 1h)
- **Nível 2:** Confirmação de vazamento (resposta em 4h)
- **Nível 3:** Impacto significativo (resposta em 24h)

### Comunicação Obrigatória
- **Autoridade Nacional de Proteção de Dados (ANPD)** em até 2 dias
- **Titulares afetados** de forma clara e imediata
- **Mídia e stakeholders** conforme necessário
- **Relatório detalhado** das causas e medidas

Esta implementação robusta da LGPD garante não apenas **conformidade legal**, mas também **confiança dos usuários** e **diferencial competitivo** no mercado de saúde brasileiro.