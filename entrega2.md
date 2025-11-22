# Plano de Experimento – Scoping e Planejamento

## 1. Identificação Básica

### 1.1 Título do experimento
**Avaliação da Efetividade da Revisão de Código Assistida por IA em Comparação com Revisão Humana Tradicional**

### 1.2 ID / código
**EXP-REV-IA-2025**

### 1.3 Versão do documento e histórico de revisão
- **v1.0 (19/11/2025)** — Criação inicial do plano.
- **v1.1 (22/11/2025)** — Inclusão completa do escopo, GQM, métricas, riscos e critérios.

### 1.4 Datas (criação, última atualização)
- **Criação:** 19/11/2025  
- **Última atualização:** 22/11/2025

### 1.5 Autores (nome, área, contato)
- **Maisa Pires** — Engenharia de Software — maisa.andrade@sga.pucminas.br

### 1.6 Responsável principal (PI / dono do experimento)
**Maisa Pires (Engenharia de Software)**

### 1.7 Projeto / produto / iniciativa relacionada
**Iniciativa de Melhoria de Qualidade de Código e Produtividade de Revisões do time de desenvolvimento web.**

---

## 2. Contexto e Problema

### 2.1 Descrição do problema / oportunidade
O time de desenvolvimento tem enfrentado aumento no volume de código entregue por sprint, tornando a revisão manual lenta, inconsistente e sujeita a falhas. Ferramentas de IA prometem automatizar parte da análise, reduzir retrabalho e aumentar a detecção de defeitos.  
O experimento avaliará se a revisão assistida por IA traz benefícios reais de qualidade e eficiência em comparação ao processo tradicional.

### 2.2 Contexto organizacional e técnico
O estudo ocorrerá em uma empresa de médio porte, com foco em aplicações web.  
- **Tecnologias predominantes:** Node.js, React, TypeScript  
- **Ferramentas:** GitHub, GitHub Actions, solução de revisão por IA  
- **Processo:** Scrum, sprints de 2 semanas  
- **Ambiente:** pipelines automatizados, PRs obrigatórias

### 2.3 Trabalhos e evidências prévias (internos e externos)
**Internos:**
- Aumento de bugs em produção apontado pela equipe de QA.
- Teste exploratório inicial mostrou sugestões relevantes da IA.

**Externos:**
- Estudos recentes indicam que LLMs aumentam produtividade de revisão.
- Relatórios da indústria destacam redução de carga cognitiva ao usar IA.

### 2.4 Referencial teórico e empírico essencial
- **Modelo GQM (Goal–Question–Metric)**
- Literatura de **Code Review** (Fagan; Bacchelli & Bird)
- Estudos sobre **LLMs aplicados à Engenharia de Software**
- Categorias do **ISO/IEC 25010**

---

# 3. Objetivos e Questões (GQM)

## 3.1 Objetivo geral (Goal Template)
**Analisar** a efetividade das revisões de código assistidas por IA  
**com o propósito de** comparar sua qualidade e eficiência  
**sob a perspectiva de** desenvolvedores e do time de engenharia  
**no contexto de** revisões de Pull Requests em um projeto web corporativo.

---

## 3.2 Objetivos específicos

- **O1:** Comparar a eficiência (tempo, volume processado) entre revisão humana e revisão assistida por IA.  
- **O2:** Avaliar o impacto da IA na detecção de defeitos e problemas de qualidade.  
- **O3:** Medir a consistência das revisões (variação por revisor, tipo de problema, repetição).  
- **O4:** Analisar a percepção dos desenvolvedores quanto à utilidade, clareza e confiabilidade das sugestões da IA.

---

## 3.3 Questões de pesquisa

### **O1 – Eficiência**
- **Q1.1:** A IA reduz o tempo total de revisão de Pull Requests?  
- **Q1.2:** A IA aumenta o número de arquivos/linhas revisados por unidade de tempo?  
- **Q1.3:** A IA reduz o tempo até a aprovação final da PR?

### **O2 – Detecção de defeitos**
- **Q2.1:** A IA identifica mais problemas de código do que revisões humanas?  
- **Q2.2:** A IA identifica problemas diferentes dos detectados por humanos?  
- **Q2.3:** As sugestões geradas pela IA resultam em mais correções efetivas?

### **O3 – Consistência**
- **Q3.1:** A IA produz revisões mais consistentes (menor variância entre revisões)?  
- **Q3.2:** A IA mantém consistência em diferentes tipos de mudanças?  
- **Q3.3:** A IA reduz divergências entre revisores humanos?

### **O4 – Percepção dos desenvolvedores**
- **Q4.1:** Desenvolvedores consideram as sugestões da IA úteis?  
- **Q4.2:** Desenvolvedores consideram as explicações claras?  
- **Q4.3:** Desenvolvedores confiam na revisão assistida por IA?

---

## 3.4 Tabela GQM (Objetivo – Perguntas – Métricas)

| Objetivo | Pergunta | Métricas Associadas |
|---------|----------|----------------------|
| O1 | Q1.1 | M1 – Tempo total de revisão; M2 – Tempo até primeira resposta |
| O1 | Q1.2 | M3 – Linhas revisadas por minuto; M4 – Arquivos revisados por PR |
| O1 | Q1.3 | M1 – Tempo total de revisão; M5 – Tempo até aprovação final |
| O2 | Q2.1 | M6 – Nº de defeitos identificados; M7 – Taxa de cobertura de problemas |
| O2 | Q2.2 | M8 – Diversidade de categorias de defeitos; M6 – Nº de defeitos identificados |
| O2 | Q2.3 | M9 – Nº de correções aplicadas; M10 – Taxa de aceitação das sugestões |
| O3 | Q3.1 | M11 – Variância entre revisões; M6 – Nº de defeitos |
| O3 | Q3.2 | M12 – Consistência por tipo de mudança; M7 – Cobertura de problemas |
| O3 | Q3.3 | M11 – Variância; M13 – Divergência entre revisores |
| O4 | Q4.1 | M14 – Índice de utilidade percebida; M15 – NPS interno |
| O4 | Q4.2 | M16 – Clareza percebida; M14 – Utilidade |
| O4 | Q4.3 | M17 – Índice de confiança; M15 – NPS interno |

---

## Tabela completa de métricas (nome, descrição e unidade)

| Métrica | Descrição | Unidade |
|--------|-----------|---------|
| M1 | Tempo total da revisão de uma PR | minutos |
| M2 | Tempo até a primeira resposta | minutos |
| M3 | Linhas revisadas por minuto | linhas/min |
| M4 | Arquivos revisados por PR | quantidade |
| M5 | Tempo até aprovação final da PR | minutos |
| M6 | Número total de defeitos identificados | contagem |
| M7 | Cobertura de problemas em relação ao total conhecido | % |
| M8 | Diversidade de categorias de defeitos | número de categorias |
| M9 | Quantidade de correções aplicadas após sugestões | contagem |
| M10 | Taxa de aceitação das sugestões da IA | % |
| M11 | Variância entre revisões (consistência) | índice |
| M12 | Consistência por tipo de mudança | índice |
| M13 | Divergência entre revisores | índice |
| M14 | Utilidade percebida (survey) | escala Likert |
| M15 | NPS interno sobre a ferramenta | escore |
| M16 | Clareza percebida das explicações | escala Likert |
| M17 | Índice de confiança dos desenvolvedores | escala Likert |

*(Total: 17 métricas, atendendo ao requisito de mínimo 10.)*

---

# 4. Escopo e contexto do experimento

## 4.1 Escopo funcional / de processo (incluído e excluído)

**Incluído:**
- Revisão de PRs de backend e frontend.
- Sugestões da IA dentro da plataforma GitHub.
- Comparação direta entre revisões humanas e IA.
- Coleta automática e manual de métricas.

**Excluído:**
- Avaliação de qualidade de testes automatizados.
- Análise de performance de runtime.
- Repositórios externos.
- Projetos mobile nativos.

---

## 4.2 Contexto do estudo
- Empresa de médio porte
- Time com experiência variada (junior a sênior)
- Projeto web corporativo, crítico para operações internas
- Uso consolidado de PRs e pipelines de CI

---

## 4.3 Premissas
- A ferramenta de IA estará operacional durante todo o período.
- Participantes seguirão o processo de revisão normalmente.
- Haverá volume suficiente de PRs para comparação.

---

## 4.4 Restrições
- Tempo limitado (jan–mar/2026)
- Ferramentas já definidas pela empresa
- Acesso somente a repositórios internos

---

## 4.5 Limitações previstas
- Generalização limitada a projetos web semelhantes.
- Resultados podem variar por perfil dos revisores.
- Ferramenta de IA usada pode não representar todas as soluções do mercado.

---

# 5. Stakeholders e impacto esperado

## 5.1 Stakeholders principais
- Desenvolvedores
- QA
- Tech Leads
- Gestores de Produto
- Engenharia de Plataforma

## 5.2 Interesses e expectativas
- **Devs:** reduzir carga de revisão e retrabalho  
- **QA:** diminuir bugs escapados  
- **Tech Leads:** padronização e consistência  
- **Gestão:** avaliar custo–benefício da IA  
- **Plataforma:** validar integração e impacto em pipelines  

## 5.3 Impactos potenciais
- Possível redução do tempo de ciclo das PRs  
- Melhoria na qualidade de código  
- Aumento temporário de carga de coleta/validação de métricas  
- Mudança futura do processo de revisão  

---

# 6. Riscos de alto nível, premissas e critérios de sucesso

## 6.1 Riscos de alto nível
- Falha ou instabilidade da ferramenta de IA  
- Baixa adesão dos desenvolvedores  
- Volume insuficiente de PRs  
- Mudanças de prioridade da empresa  

## 6.2 Critérios de sucesso (go/no-go)
- Coleta de dados completa e válida  
- Diferenças claras entre revisão humana e IA  
- Aceitação mínima da ferramenta pelos desenvolvedores  
- Evidências úteis para tomada de decisão  

## 6.3 Critérios de parada antecipada
- Falha crítica da ferramenta de IA  
- Impossibilidade de obter métricas essenciais  
- Bloqueio organizacional ou mudança de escopo do produto  

