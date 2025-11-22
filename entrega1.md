# Plano de Experimento – Scoping e Planejamento

## 1. Identificação Básica

### 1.1 Título do experimento
**Avaliação da Efetividade da Revisão de Código Assistida por IA em Comparação com Revisão Humana Tradicional**

### 1.2 ID / código
**EXP-REV-IA-2025**

### 1.3 Versão do documento e histórico de revisão
- **v1.0 (19/11/2025)** — Criação inicial do plano.

### 1.4 Datas (criação, última atualização)
- **Criação:** 19/11/2025  
- **Última atualização:** 19/11/2025

### 1.5 Autores (nome, área, contato)
- **Maisa Pires** — Engenharia de Software — maisa.andrade@sga.pucminas.br

### 1.6 Responsável principal (PI / dono do experimento)
**Maisa Pires (Engenharia de Software)**

### 1.7 Projeto / produto / iniciativa relacionada
**Iniciativa de Melhoria de Qualidade de Código e Produtividade de Revisões do time de desenvolvimento web.**

---

## 2. Contexto e Problema

### 2.1 Descrição do problema / oportunidade
O time de desenvolvimento tem enfrentado um crescimento constante no volume de código entregue por sprint, tornando a revisão manual mais lenta, inconsistente e sujeita a falhas. Ferramentas de IA voltadas para revisão de código prometem automatizar parte da análise, reduzir retrabalho e aumentar a detecção de defeitos.

O experimento busca responder se revisões assistidas por IA realmente trazem benefícios mensuráveis em termos de qualidade e eficiência quando comparadas à revisão humana tradicional.

### 2.2 Contexto organizacional e técnico
O estudo será conduzido em uma empresa de médio porte focada em desenvolvimento de aplicações web.  
- **Tecnologias predominantes:** Node.js, React, TypeScript.  
- **Repositórios e ferramentas:** GitHub, GitHub Actions, ferramenta de revisão por IA integrada.  
- **Processo:** Scrum com sprints de 2 semanas.  
- **Ambiente:** pipelines automatizados, branches padronizadas, PRs obrigatórias.

### 2.3 Trabalhos e evidências prévias (internos e externos)
**Internos:**
- Relatórios da equipe de QA indicam aumento de bugs escapados para produção no último trimestre.
- Teste preliminar exploratório mostrou que a IA sugeriu algumas melhorias relevantes, mas sem coleta sistemática.

**Externos:**
- Estudos acadêmicos recentes analisam o uso de LLMs em revisão de código e apontam benefícios em produtividade.
- Relatórios do GitHub e Microsoft destacam aumento de velocidade e redução de carga cognitiva ao usar IA em revisões.

### 2.4 Referencial teórico e empírico essencial
O experimento se baseia em:
- **Modelo GQM (Goal–Question–Metric)** para alinhamento entre objetivo, perguntas e métricas.
- Literatura de **Code Review** (Fagan, Bacchelli & Bird).
- Pesquisas sobre **LLMs aplicados à Engenharia de Software** e automação de tarefas cognitivas.
- Estruturas de categorização de defeitos baseadas no **ISO/IEC 25010**.
