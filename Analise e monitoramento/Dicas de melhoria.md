# 📈 Dicas de Melhoria e Causa Raiz dos Bugs

## Visão Geral
Este documento lista as principais **dicas de melhoria** identificadas durante os testes realizados no projeto, com base nos **12 bugs** encontrados. Cada melhoria foca em resolver a causa raiz para garantir a qualidade e estabilidade do sistema.

---

## 🐞 Lista de Bugs, Causas e Melhorias

### 1️⃣ Bug: **Campo de busca não exibe corretamente nomes digitados**
- **Causa raiz:** Falta de ligação entre o input de busca e a base de dados de produtos.
- **Dica de melhoria:** Corrigir a funcionalidade de busca para que exiba resultados baseados nos nomes dos produtos digitados.

---

### 2️⃣ Bug: **Ordenação de produtos incorreta**
- **Causa raiz:** Algoritmo de ordenação invertido (High to Low / Low to High).
- **Dica de melhoria:** Revisar a lógica de ordenação para ordenar corretamente os produtos.

---

### 3️⃣ Bug: **Adiciona ao carrinho mesmo fora de estoque**
- **Causa raiz:** Falta de verificação de estoque antes de adicionar ao carrinho.
- **Dica de melhoria:** Implementar checagem de estoque no momento da adição ao carrinho.

---

### 4️⃣ Bug: **Troca de imagem principal falha**
- **Causa raiz:** Falta de evento de clique nas miniaturas.
- **Dica de melhoria:** Vincular corretamente as miniaturas à troca da imagem principal.

---

### 5️⃣ Bug: **Seleção de variações troca de produto**
- **Causa raiz:** Associação incorreta entre variações e produto final.
- **Dica de melhoria:** Corrigir a lógica de variações para que mantenha o produto correto.

---

### 6️⃣ Bug: **Erro ao adicionar ao carrinho sem variações obrigatórias**
- **Causa raiz:** Falta de validação de variações antes de adicionar.
- **Dica de melhoria:** Validar seleção de variações obrigatórias antes de permitir a adição ao carrinho.

---

### 7️⃣ Bug: **Erro ao tentar adicionar quantidade inválida (0 ou negativa)**
- **Causa raiz:** Validação de quantidade ausente ou incorreta.
- **Dica de melhoria:** Adicionar verificação para impedir quantidades inválidas.

---

### 8️⃣ Bug: **Página de comparação de produtos de difícil acesso**
- **Causa raiz:** Falta de links claros e visíveis para a página de comparação.
- **Dica de melhoria:** Adicionar botões ou links visíveis em áreas como cabeçalho ou página de produto.

---

### 9️⃣ Bug: **Checkout permite finalização sem login**
- **Causa raiz:** Falta de validação do estado de login antes de finalizar a compra.
- **Dica de melhoria:** Bloquear finalização do checkout para usuários não logados.

---

### 🔟 Bug: **Erro de segurança ao pular etapas via URL**
- **Causa raiz:** Falta de controle de etapas do checkout.
- **Dica de melhoria:** Implementar validação de etapas para evitar bypass por URL.

---

### 1️⃣1️⃣ Bug: **Campo de email inválido não gera erro**
- **Causa raiz:** Falta de validação de formato de email no formulário.
- **Dica de melhoria:** Adicionar validação de email no client-side e server-side.

---

### 1️⃣2️⃣ Bug: **Validação ausente para campos de telefone/CEP**
- **Causa raiz:** Falta de regras de validação nesses campos.
- **Dica de melhoria:** Implementar validação de telefone, CEP e outros campos numéricos.

---

## 📌 Priorização de Melhorias
Com base na gravidade e impacto, as dicas de melhoria podem ser priorizadas em três categorias:

- **Alta prioridade (Urgente)**  
  - Bugs 3, 5, 9, 10 (impactam a finalização de pedidos e segurança)

- **Média prioridade**  
  - Bugs 1, 2, 4, 6, 11 (impactam a experiência do usuário)

- **Baixa prioridade**  
  - Bugs 7, 8, 12 (não impedem compra, mas afetam a usabilidade)

---

## 🛠️ Próximos Passos
- Revisar cada causa raiz em conjunto com a equipe de desenvolvimento.
- Priorizar as correções e criar **tarefas de melhoria** nos quadros do projeto.
- Realizar novos testes após cada correção para garantir que as falhas foram resolvidas.

---

📄 **Este documento faz parte da fase de análise e monitoramento do projeto.**  
💡 Para mais detalhes, consulte o arquivo `BUG_REPORT.md`.

---
