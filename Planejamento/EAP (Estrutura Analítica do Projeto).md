# 📚 EAP - Estrutura Analítica do Projeto
## Projeto de Testes Automatizados e Manuais – *AutomationPractice*

---

## 🧩 Nível 0: Projeto de Testes Automatizados e Manuais AutomationPractice

---

### 1.0 Fase de Planejamento e Iniciação

- **1.1** Definição dos Objetivos e Escopo do Projeto (manual vs. automatizado)
- **1.2** Seleção Final das Ferramentas e Tecnologias (automação e gestão manual)
- **1.3** Elaboração da Documentação Inicial do Projeto
  - 1.3.1 Análise de Requisitos (RF, RNF)
  - 1.3.2 Critérios de Aceite (AC)
  - 1.3.3 Regras de Negócio (RN)
  - 1.3.4 User Stories (US)
  - 1.3.5 Análise de Recursos
  - 1.3.6 Estrutura Analítica do Projeto (EAP)
  - 1.3.7 (Opcional) Cronograma Preliminar
- **1.4** Configuração Inicial da Ferramenta de Gestão (Jira, Trello ou Planilha)
  - 1.4.1 Criação do Projeto/Board
  - 1.4.2 Cadastro das User Stories / Tarefas Iniciais

---

### 2.0 Fase de Configuração do Ambiente

- **2.1** Instalação das Ferramentas de Desenvolvimento
  - 2.1.1 Linguagem de Programação
  - 2.1.2 IDE (ex: VS Code)
  - 2.1.3 Git
  - 2.1.4 Navegadores Adicionais (Chrome, Firefox)
- **2.2** Configuração do Projeto de Automação
  - 2.2.1 Estrutura Base de Pastas
  - 2.2.2 Gerenciador de Dependências
  - 2.2.3 Framework de Automação
  - 2.2.4 Bibliotecas Auxiliares
- **2.3** Configuração do Controle de Versão
  - 2.3.1 Repositório Git Local
  - 2.3.2 Repositório Remoto
  - 2.3.3 Conexão Git Local ↔ Remoto
- **2.4** (Opcional) Ferramenta de Gestão de Testes Manuais (ex: TestLink)

---

### 3.0 Fase de Design e Estruturação dos Testes

- **3.1** Definição da Estratégia de Testes (manuais, automatizados, exploratórios)
- **3.2** Arquitetura da Automação
- **3.3** Casos de Teste Manuais
  - 3.3.1 Escrita dos Passos
  - 3.3.2 Definição dos Resultados Esperados
- **3.4** Casos de Teste Automatizados (mapeamento US → casos)
- **3.5** Planejamento e Preparação da Massa de Dados
- **3.6** Estrutura de Relatórios (automação + execuções manuais)

---

### 4.0 Fase de Desenvolvimento da Automação

- **4.1** Implementação da Estrutura Base do Framework
- **4.2** Scripts de Teste Automatizados por Módulo:
  - 4.2.1 Autenticação e Conta (RF01)
  - 4.2.2 Navegação e Estrutura (RF02)
  - 4.2.3 Pesquisa de Produtos (RF03)
  - 4.2.4 Listagem de Produtos (PLP) (RF04)
  - 4.2.5 Detalhes do Produto (PDP) (RF05)
  - 4.2.6 Carrinho de Compras (RF06)
  - 4.2.7 Checkout (RF07)
  - 4.2.8 Outras Funcionalidades (RF09)
  - 4.2.9 Testes de Validação de Formulários (RF08 - Transversal)
- **4.3** Asserções e Validações
- **4.4** Integração da Massa de Dados
- **4.5** Revisão e Refatoração
- **4.6** (Opcional) Checklists de Testes Exploratórios

---

### 5.0 Fase de Execução dos Testes

- **5.1** Preparação do Ambiente (drivers, navegadores, massa)
- **5.2** Execução dos Testes Manuais
  - 5.2.1 Casos de Teste Manuais Pré-definidos
  - 5.2.2 Testes Exploratórios (com ou sem checklist)
  - 5.2.3 Registro dos Resultados e Evidências
- **5.3** Execução dos Testes Automatizados
  - 5.3.1 Criação das Suítes de Teste
  - 5.3.2 Execução Local das Suítes
  - 5.3.3 Coleta de Logs e Monitoramento

---

### 6.0 Fase de Análise e Relatórios

- **6.1** Análise Consolidada dos Resultados (Manuais e Automatizados)
- **6.2** Investigação e Documentação de Falhas (Causa Raiz)
- **6.3** Geração de Relatórios (automação e execução manual)
- **6.4** Registro e Priorização de Defeitos (via Jira/Trello/Planilha)

---

### 7.0 Fase de Gerenciamento e Encerramento

- **7.1** Acompanhamento Contínuo do Progresso (atualizações de tarefas)
- **7.2** Documentação Final (Readme, Lições Aprendidas, Sumário de Cobertura)
- **7.3** Revisão Final (código, casos manuais, resultados)
- **7.4** Arquivamento do Projeto (backup de scripts, documentos, evidências)

---

## 📝 Observações e Adições Estratégicas

- **1.1 / 1.2**: Reforço no escopo manual vs. automatizado e escolha das ferramentas.
- **3.3**: Casos de teste manuais como entregável separado.
- **4.6**: Checklists opcionais para testes exploratórios.
- **5.2**: Bloco exclusivo para execução de testes manuais.
- **6.1 / 6.3 / 6.4**: Integração dos relatórios manuais com a automação.
- **7.3 / 7.4**: Inclusão dos artefatos manuais no encerramento.

---

> Esta EAP serve como guia mestre para **organizar, planejar, executar e encerrar** o projeto com clareza e rastreabilidade, atendendo a escopos **manuais e automatizados**.
