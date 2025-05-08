**Plano de Testes - Projeto de Testes AutomationPractice**

**Versão:** 1.0
**Data:** 05 de mai. de 2025
**Autor:** Miguel Luis

---

### 1. **Introdução**

Este documento descreve o plano para a execução de testes manuais e automatizados no site [automationpractice.com.br](http://automationpractice.com.br) (referido como AUT - Application Under Test). O objetivo principal deste projeto é educacional, visando aplicar e aprimorar conhecimentos em análise de requisitos, planejamento, execução e automação de testes de software, utilizando as funcionalidades de e-commerce do AUT como base. Este plano orientará todas as atividades de teste subsequentes.

---

### 2. **Referências**

* Análise Detalhada de Requisitos (RF, RNF) V1.0
* Critérios de Aceite (AC) V1.0
* Regras de Negócio (RN) V1.0
* User Stories (US) V1.0
* Estrutura Analítica do Projeto (EAP) V1.0
* Análise de Recursos (Orçamento, Alocação, Aquisição) V1.0

---

### 3. **Objetivos do Teste**

* Verificar se as funcionalidades implementadas no AUT atendem aos Requisitos Funcionais (RFs) e Critérios de Aceite (ACs) definidos.
* Validar se o sistema adere às Regras de Negócio (RNs) estabelecidas.
* Avaliar a usabilidade e a experiência do usuário (UX) em fluxos chave (Navegação, Compra).
* Identificar e documentar defeitos, inconsistências ou comportamentos inesperados.
* Verificar a compatibilidade básica do site nos navegadores definidos (Cross-Browser).
* Avaliar aspectos Não Funcionais básicos (RNFs) como feedback visual e tratamento de erros.
* Desenvolver uma suíte de testes automatizados reutilizável para os principais fluxos de regressão.
* Obter experiência prática na aplicação de um processo de teste estruturado.

---

### 4. **Escopo do Teste**

#### 4.1 **Funcionalidades em Escopo**

Baseado nos RFs definidos, as seguintes áreas funcionais serão testadas:

* **RF01:** Autenticação e Gerenciamento de Conta (Registro, Login, Logout, Recuperação Senha, Gestão "Minha Conta")
* **RF02:** Navegação e Estrutura do Site (Menu, Cabeçalho, Rodapé, Breadcrumbs, Links Internos)
* **RF03:** Pesquisa de Produtos
* **RF04:** Listagem e Filtragem de Produtos (PLP) (Exibição, Paginação, Ordenação, Filtros, Quick View)
* **RF05:** Detalhes do Produto (PDP) (Exibição, Imagens, Variações, Quantidade, Add to Cart)
* **RF06:** Carrinho de Compras (Visualização, Atualização Qtd, Remoção, Totais, Cupom - se aplicável)
* **RF07:** Processo de Checkout (Etapas, Endereços, Frete, Termos, Pagamento, Confirmação, Email)
* **RF08:** Validação de Campos de Formulário (Obrigatoriedade, Formato)
* **RF09:** Outras Funcionalidades (Formulário de Contato, Newsletter, Comparação - se aplicável)

#### 4.2 **Tipos de Teste em Escopo**

* **Testes Funcionais**: Verificar se cada função opera conforme especificado nos RFs e ACs.

  * **Testes Manuais:**

    * Testes Exploratórios
    * Testes de Usabilidade
    * Testes de Casos de Uso
    * Verificação de Requisitos Não Funcionais visuais (Consistência, Legibilidade, Feedback)

  * **Testes Automatizados:**

    * Testes de Regressão
    * Testes de Validação Funcional
    * Testes de Compatibilidade (Cross-Browser)

#### 4.3 **Fora de Escopo**

* Testes de Performance, Carga e Estresse.
* Testes de Segurança Aprofundados (Pen Tests, análise de vulnerabilidades complexas).
* Teste de APIs backend.
* Teste da integração real com gateways de pagamento.
* Teste do painel de administração do site.
* Teste de acessibilidade formal (WCAG).
* Teste de banco de dados direto.
* Tradução e localização.

---

### 5. **Estratégia / Abordagem de Teste**

* **Combinação Manual e Automatizada**: Utilizar uma abordagem híbrida, com testes manuais para exploração, usabilidade e cenários complexos, e testes automatizados focados na regressão de fluxos críticos e validação repetitiva de funcionalidades chave.

* **Base em Requisitos**: Todos os casos de teste serão rastreáveis aos Requisitos Funcionais, User Stories e Critérios de Aceite.

* **Automação:**

  * **Framework:** \[Especificar framework escolhido: Ex: Selenium WebDriver, Cypress, Playwright]
  * **Linguagem:** JavaScript
  * **Padrão de Design:** Page Object Model (POM) ou similar
  * **Execução:** Inicialmente local nos navegadores definidos.
  * **Relatórios:** ExtentReports, Allure, ou relatórios nativos do framework.

* **Testes Manuais:**

  * Casos de Teste baseados nos ACs e USs.
  * Sessões de Testes Exploratórios com checklists ou charters focados em áreas específicas ou riscos.

* **Gestão de Defeitos:** Defeitos serão registrados com informações claras (passos para reproduzir, resultado esperado vs. atual, severidade/prioridade).

---

### 6. **Ambiente de Teste**

* **Aplicação Alvo (AUT):** [automationpractice.com](http://automationpractice.com)

* **Ambiente Cliente:**

  * **Hardware:** Acer Nitro 5
  * **Sistema Operacional:** \[Especificar: Ex: Windows 11]
  * **Navegadores Alvo:**

    * **Primário:** Microsoft Edge (Última Versão Estável)
    * **Secundários:** Google Chrome, Mozilla Firefox

* **Ferramentas de Teste:** IDE, Git, Framework, etc.

---

### 7. **Cronograma (Estimativa de Alto Nível por Fase da EAP)**

* **Fase 1 (Planejamento):** Concluída
* **Fase 2 (Configuração Ambiente):** \[Estimar duração, ex: 1-2 dias]
* **Fase 3 (Design Testes):** \[Estimar duração, ex: 3-5 dias]
* **Fase 4 (Desenvolvimento Automação):** \[Estimar duração, ex: 10-15 dias]
* **Fase 5 (Execução Testes):** \[Estimar duração, ex: 3-5 dias]
* **Fase 6 (Análise e Relatórios):** \[Estimar duração, ex: 1-2 dias]
* **Fase 7 (Gerenciamento e Encerramento):** Contínuo

---

### 8. **Recursos e Responsabilidades**

* **Responsável:** Miguel Luis

---

### 9. **Entregáveis do Teste**

* Plano de Testes (este documento)
* Casos de Teste Manuais
* Scripts de Teste Automatizados
* Massa de Dados de Teste
* Relatórios de Execução de Testes
* Relatórios de Defeitos

---

### 10. **Critérios de Entrada e Saída**

**Critérios de Entrada:**

* Plano de Testes aprovado
* Ambiente de teste acessível e estável
* Casos de Teste escritos e revisados
* Scripts de Teste Automatizados prontos
* Massa de dados preparada
* Ferramentas de teste instaladas

**Critérios de Saída:**

* Todos os casos de teste executados
* Resultados documentados e analisados
* Defeitos críticos registrados
* Cobertura de requisitos atingida
* Entregáveis produzidos e revisados

---

### 11. **Riscos e Mitigações**

| **Risco**                            | **Probabilidade** | **Impacto** | **Mitigação**                                          |
| ------------------------------------ | ----------------- | ----------- | ------------------------------------------------------ |
| Instabilidade do AUT                 | Média             | Alto        | Monitorar disponibilidade, reexecutar testes falhos    |
| Mudanças inesperadas no AUT          | Média             | Alto        | Manter scripts modulares, adaptar rapidamente          |
| Falta de dados de teste adequados    | Baixa             | Médio       | Criar contas/dados manualmente no AUT                  |
| Limitações das ferramentas gratuitas | Baixa             | Baixo       | Adaptar estratégia conforme limitações conhecidas      |
| Subestimação do esforço de automação | Média             | Médio       | Priorizar fluxos essenciais, ser realista com o escopo |

---

### 12. **Métricas de Teste**

* Número de Casos de Teste Planejados vs. Executados
* Percentual de Casos de Teste Aprovados / Reprovados
* Número de Defeitos Registrados
* Cobertura de Requisitos
* Tempo médio de execução da suíte automatizada

---

### 13. **Aprovações**

Este plano de teste serve como guia para as atividades de teste a serem realizadas neste projeto educacional. Nenhuma aprovação formal externa é necessária.
