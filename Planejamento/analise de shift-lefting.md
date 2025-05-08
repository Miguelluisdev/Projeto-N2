# Atividades de Teste (Shift-Left)

## 1. Revisão Estática dos Artefatos (Fase de Planejamento/Design)

### Atividade:
Revisar criticamente os documentos de Requisitos Funcionais (RFs), Não Funcionais (RNFs), Critérios de Aceite (ACs), User Stories (US) e Regras de Negócio (RNs).

### Objetivo:
- **Identificar Ambiguidade**: Encontrar declarações vagas, contraditórias ou que permitam múltiplas interpretações nos requisitos e regras.  
  Exemplo: O RF01.1 diz "regras de complexidade de senha (se definidas)" - Precisamos confirmar se SÃO definidas ou não para testar corretamente.
  
- **Verificar Completude**: Checar se falta alguma informação essencial para entender ou testar uma funcionalidade.  
  Exemplo: O RF07.5 menciona pagamentos, mas foca em transferência/cheque. A US/AC cobre claramente o fluxo desses métodos específicos?

- **Garantir Testabilidade**: Avaliar se cada requisito, critério de aceite e regra de negócio pode ser efetivamente verificado por um teste (manual ou automatizado).  
  Exemplo: RNF01.1 menciona "menos de X segundos" - O valor 'X' precisa ser definido para ser testável.

- **Assegurar Consistência**: Verificar se os diferentes artefatos (RF, AC, US, RN) estão alinhados e não se contradizem.  
  Exemplo: A User Story reflete corretamente o detalhe descrito no RF e no AC? A RN não impede o fluxo descrito no RF?

### Como Fazer:
- Ler atentamente cada documento, questionando cada afirmação.
- Usar os ACs para validar a clareza dos RFs/USs.
- Usar as RNs para verificar as restrições nos fluxos.
- Anotar dúvidas, inconsistências ou pontos de melhoria.

---

## 2. Derivação Antecipada de Cenários de Teste (Alto Nível) (Fase de Planejamento/Design)

### Atividade:
Esboçar os principais cenários de teste (positivos, negativos, exceções) diretamente a partir dos Requisitos Funcionais, User Stories e Regras de Negócio, antes mesmo de detalhar os casos de teste formais.

### Objetivo:
- **Validar Entendimento**: Confirmar o entendimento dos fluxos principais e alternativos.
- **Identificar Lacunas**: Descobrir fluxos ou condições não explicitamente cobertos pelos requisitos, mas que são logicamente possíveis ou importantes (baseado nas RNs).
- **Estimar Esforço**: Ter uma ideia inicial da complexidade e quantidade de testes necessários para cada funcionalidade.

### Como Fazer:
Para cada RF/US, pensar:
- Qual o caminho feliz (happy path)?
- Quais os erros mais comuns (dados inválidos, campos obrigatórios)?  
  Exemplo: Baseado no RF08 e ACs de erro.
- Quais regras de negócio (RNs) impõem restrições que geram cenários alternativos ou de erro?  
  Exemplo: RN01 - tentar cadastrar email duplicado; RN19 - tentar comprar produto fora de estoque.
- Existem condições de limite?  
  Exemplo: Quantidade máxima/mínima no carrinho.

---

## 3. Modelagem de Fluxo e Decisão (Fase de Design)

### Atividade:
Criar diagramas de fluxo simples ou tabelas de decisão para funcionalidades mais complexas, como o processo de Checkout (RF07) ou o registro com múltiplas validações (RF01.1).

### Objetivo:
- **Visualizar Complexidade**: Entender claramente todas as ramificações, condições e dependências do fluxo.
- **Identificar Caminhos**: Garantir que todos os caminhos lógicos possíveis sejam considerados para teste.
- **Otimizar Testes**: Identificar condições que podem ser combinadas ou priorizadas.

### Como Fazer:
- Usar ferramentas simples (desenho, planilhas) para mapear as etapas do checkout, as decisões (login/registro, seleção de endereço, frete, pagamento) e os diferentes resultados possíveis com base nas regras de negócio e validações.

---

## 4. Prototipagem/Revisão da Estrutura da Automação (Fase de Design/Configuração)

### Atividade:
Antes de codificar todos os scripts, definir e revisar a arquitetura da automação (ex: Page Objects, Screenplay). Criar protótipos de algumas classes Page Object ou componentes reutilizáveis.

### Objetivo:
- **Garantir Testabilidade do Código de Teste**: Verificar se a estrutura escolhida facilita a escrita, manutenção e leitura dos scripts.
- **Promover Reutilização**: Identificar componentes comuns (login, menu, rodapé) que podem ser encapsulados cedo.
- **Antecipar Desafios**: Identificar elementos complexos de interagir ou validar na UI e pensar em estratégias antes da codificação em massa.

### Como Fazer:
- Esboçar a estrutura de pastas.
- Criar a classe base para as páginas, implementar um ou dois Page Objects simples (ex: HomePage, LoginPage) e revisar se o padrão funciona bem e é claro.

---

## 5. Preparação Antecipada da Massa de Dados (Fase de Design/Configuração)

### Atividade:
Identificar e, se possível, preparar (ou planejar a criação) da massa de dados necessária para os cenários de teste identificados, antes de executar os testes.

### Objetivo:
- **Garantir Disponibilidade**: Assegurar que os dados necessários (usuários válidos/inválidos, produtos com/sem estoque, cupons válidos/inválidos) existirão quando os testes forem executados/automatizados.
- **Evitar Bloqueios**: Não ser impedido de testar/automatizar por falta de dados adequados.

### Como Fazer:
- Listar os tipos de dados necessários com base nos cenários (derivados no passo 2).
- Criar contas de teste no site, identificar produtos com características específicas, anotar ou criar códigos de cupom (se o site permitir ou você tiver controle sobre isso - o que não é o caso aqui, então seria mais identificar).

---

# Benefícios da Antecipação (Shift-Left)

- **Detecção Precoce de Defeitos**: Encontrar problemas nos próprios requisitos e no design antes que virem código (seja do sistema ou da automação).
- **Redução de Custos**: Corrigir um requisito ambíguo é muito mais barato do que corrigir um bug em produção derivado dessa ambiguidade.
- **Melhor Compreensão**: O processo de revisão e derivação antecipada força um entendimento mais profundo do sistema.
- **Automação Mais Eficaz**: Scripts de automação construídos sobre requisitos claros e uma boa arquitetura são mais robustos e fáceis de manter.
