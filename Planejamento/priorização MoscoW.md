# 📊 Tabela de Priorização MoSCoW — Projeto de Testes *AutomationPractice*

> **Legenda MoSCoW:**
>
> * **M (Must have)** – Essencial: sem isso o projeto não pode ser entregue.
> * **S (Should have)** – Importante: deve estar presente se possível, mas não é crítico.
> * **C (Could have)** – Desejável: valor agregado com baixo impacto se ausente.
> * **W (Won’t have)** – Fora do escopo atual; possível para versões futuras.

---

## 🔧 1.0 Fase de Planejamento e Iniciação

| Item                                                        | Prioridade | Justificativa                                        | Priorização de Testes |
| ----------------------------------------------------------- | ---------- | ---------------------------------------------------- | --------------------- |
| Definição dos Objetivos e Escopo                            | M          | Direcionamento estratégico do projeto.               | N/A                   |
| Seleção de Ferramentas e Tecnologias                        | M          | Fundamenta toda a automação e gestão.                | N/A                   |
| Documentação Inicial (RF, AC, RN, US, EAP, Plano de Testes) | M          | Essencial para entendimento e execução.              | Revisão Estática = M  |
| Configuração de Ferramenta de Gestão                        | S          | Melhora organização; possível iniciar com planilhas. | N/A                   |

---

## 🖥️ 2.0 Fase de Configuração do Ambiente

| Item                                            | Prioridade | Justificativa                                                   | Priorização de Testes |
| ----------------------------------------------- | ---------- | --------------------------------------------------------------- | --------------------- |
| Instalação de Ferramentas (IDE, Git, Linguagem) | M          | Necessário para desenvolvimento.                                | N/A                   |
| Configuração do Framework de Automação          | M          | Estrutura base dos testes automatizados.                        | N/A                   |
| Controle de Versão (Git Local/Remoto)           | S          | Boas práticas, mas não obrigatório para um projeto educacional. | N/A                   |

---

## 🧩 3.0 Fase de Design e Estruturação dos Testes

| Item                                | Prioridade | Justificativa                                | Priorização de Testes |
| ----------------------------------- | ---------- | -------------------------------------------- | --------------------- |
| Estratégia de Testes                | M          | Define o escopo e abordagem de testes.       | N/A                   |
| Arquitetura da Automação (POM)      | M          | Base para manutenibilidade e escalabilidade. | N/A                   |
| Casos de Teste Manuais (Core)       | M          | Para fluxos críticos.                        | Testes Core = M       |
| Casos de Teste Manuais (Adicionais) | S          | Ampliam cobertura e exploram o sistema.      | Testes Adicionais = S |
| Design dos Casos Automatizados      | M          | Base para scripts futuros.                   | N/A                   |
| Massa de Dados                      | M          | Essencial para execução dos testes.          | N/A                   |

---

## 🧪 4.0 Fase de Desenvolvimento da Automação

| Item                        | Prioridade | Justificativa                | Priorização de Testes |
| --------------------------- | ---------- | ---------------------------- | --------------------- |
| Estrutura Base do Framework | M          | Necessária para codificação. | Testes de Unidade = S |

---

### 🔐 Módulo: Autenticação e Conta (RF01)

| Funcionalidade                            | Prioridade | Justificativa               | Priorização de Testes  |
| ----------------------------------------- | ---------- | --------------------------- | ---------------------- |
| Registro, Login, Logout                   | M          | Fluxos críticos.            | Testes Auto/Manual = M |
| Recuperação de Senha                      | S          | Relevante para UX.          | Testes Auto/Manual = S |
| Minha Conta (dados, endereços, histórico) | M          | Core para usuários logados. | Testes Auto/Manual = M |
| Wishlist                                  | C          | Não essencial.              | Testes Auto/Manual = C |

---

### 🧭 Módulo: Navegação e Estrutura (RF02)

| Funcionalidade               | Prioridade | Justificativa          | Priorização de Testes  |
| ---------------------------- | ---------- | ---------------------- | ---------------------- |
| Menu, Cabeçalho, Breadcrumbs | M          | Navegação fundamental. | Testes Auto/Manual = M |
| Rodapé (Links, Conta)        | S          | Complementar.          | Testes Manuais = S     |

---

### 🔎 Módulo: Pesquisa de Produtos (RF03)

| Funcionalidade             | Prioridade | Justificativa                | Priorização de Testes  |
| -------------------------- | ---------- | ---------------------------- | ---------------------- |
| Campo e lógica de pesquisa | M          | Facilita acesso ao conteúdo. | Testes Auto/Manual = M |

---

### 📃 Módulo: Listagem de Produtos (PLP) (RF04)

| Funcionalidade                               | Prioridade | Justificativa                         | Priorização de Testes  |
| -------------------------------------------- | ---------- | ------------------------------------- | ---------------------- |
| Exibição, Paginação, Ordenação               | M          | Essencial para navegação de catálogo. | Testes Auto/Manual = M |
| Filtros Principais (Categoria, Tamanho, Cor) | M          | Refina busca.                         | Testes Auto/Manual = M |
| Filtros Secundários (Composição, Estilo)     | S          | Valor agregado.                       | Testes Manual/Auto = S |
| Quick View                                   | C          | Comodidade.                           | Testes Manual/Auto = C |

---

### 🧾 Módulo: Detalhes do Produto (PDP) (RF05)

| Funcionalidade                              | Prioridade | Justificativa                      | Priorização de Testes  |
| ------------------------------------------- | ---------- | ---------------------------------- | ---------------------- |
| Imagens, Variações, Quantidade, Add to Cart | M          | Necessário para decisão de compra. | Testes Auto/Manual = M |

---

### 🛒 Módulo: Carrinho de Compras (RF06)

| Funcionalidade                    | Prioridade | Justificativa                             | Priorização de Testes  |
| --------------------------------- | ---------- | ----------------------------------------- | ---------------------- |
| Visualização, Atualização, Totais | M          | Parte vital do fluxo de compra.           | Testes Auto/Manual = M |
| Aplicação de Cupom                | S          | Depende da existência de cupons de teste. | Testes Manual/Auto = S |

---

### 💳 Módulo: Checkout (RF07)

| Funcionalidade                                            | Prioridade | Justificativa                 | Priorização de Testes  |
| --------------------------------------------------------- | ---------- | ----------------------------- | ---------------------- |
| Todas as Etapas (Endereço, Frete, Pagamento, Confirmação) | M          | Clímax do processo de compra. | Testes Auto/Manual = M |

---

### ✍️ Módulo: Validação de Formulários (RF08)

| Funcionalidade                             | Prioridade | Justificativa                 | Priorização de Testes  |
| ------------------------------------------ | ---------- | ----------------------------- | ---------------------- |
| Campos obrigatórios, mensagens de erro, UX | M          | Garante integridade de dados. | Testes Auto/Manual = M |

---

### 🧰 Módulo: Outras Funcionalidades (RF09)

| Funcionalidade         | Prioridade | Justificativa           | Priorização de Testes  |
| ---------------------- | ---------- | ----------------------- | ---------------------- |
| Formulário de Contato  | S          | Comunicação essencial.  | Testes Manual/Auto = S |
| Newsletter             | C          | Marketing, não crítico. | Testes Manuais = C     |
| Comparação de Produtos | C          | Recurso adicional.      | Testes Manual/Auto = C |

---

## 🧭 5.0 Fase de Execução dos Testes

| Item                                        | Prioridade | Justificativa                    | Priorização de Testes |
| ------------------------------------------- | ---------- | -------------------------------- | --------------------- |
| Execução de Testes Manuais (M e S)          | M          | Validação inicial e ampla.       | —                     |
| Testes Exploratórios                        | S          | Identifica falhas não previstas. | —                     |
| Execução de Testes Automatizados (Suítes M) | M          | Regressão crítica.               | —                     |
| Execução de Testes Automatizados (Suítes S) | S          | Ampliam cobertura.               | —                     |

---

## 📈 6.0 Fase de Análise e Relatórios

| Item                               | Prioridade | Justificativa                    |
| ---------------------------------- | ---------- | -------------------------------- |
| Análise de Resultados              | M          | Entendimento da qualidade final. |
| Investigação de Falhas             | M          | Necessário para correção.        |
| Registro e Priorização de Defeitos | M          | Planejamento da correção.        |

---

## 📦 7.0 Fase de Gerenciamento e Encerramento

| Item                          | Prioridade | Justificativa                   |
| ----------------------------- | ---------- | ------------------------------- |
| Acompanhamento do Progresso   | M          | Visibilidade contínua.          |
| Documentação Final do Projeto | S          | Registro de aprendizados.       |
| Arquivamento do Projeto       | S          | Boas práticas de ciclo de vida. |

---

## 🧪 Testes Não Funcionais e Complementares

| Item                          | Prioridade | Justificativa                     | Priorização de Testes  |
| ----------------------------- | ---------- | --------------------------------- | ---------------------- |
| Testes Visuais / RNFs Básicos | S          | Verifica aparência e experiência. | Testes Manuais = S     |
| Cross-Browser Básico          | S          | Compatibilidade essencial.        | Testes Manual/Auto = S |
| Performance (Observação)      | C          | Subjetivo, sem ferramenta.        | Observação Manual = C  |
| Segurança Básica (HTTPS)      | S          | Proteção mínima esperada.         | Verificação Manual = S |
