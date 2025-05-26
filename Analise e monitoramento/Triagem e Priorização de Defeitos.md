## 🐞 Triagem e Priorização de Defeitos

A triagem e priorização dos defeitos identificados no sistema foram realizadas com base na **gravidade**, **impacto no usuário final** e **urgência de correção**.

### 🎯 Critérios Utilizados para Priorização

| Critério                     | Descrição                                                 |
| ---------------------------- | --------------------------------------------------------- |
| **Gravidade**                | Grau de impacto no sistema e na experiência do usuário.   |
| **Frequência**               | Quantidade de vezes que o bug ocorre ou pode ocorrer.     |
| **Visibilidade**             | Visibilidade do bug ao usuário final.                     |
| **Complexidade da Correção** | Facilidade ou dificuldade de corrigir o defeito.          |
| **Dependências**             | Relação do bug com outras partes do sistema e/ou módulos. |

---

### 🚦 Classificação dos Defeitos

| ID do Bug | Descrição                                          | Gravidade | Prioridade | Status                |
| --------- | -------------------------------------------------- | --------- | ---------- | --------------------- |
| 01        | Ordenação invertida em lista de produtos           | Alta      | Alta       | Correção em andamento |
| 02        | Adiciona ao carrinho mesmo fora de estoque         | Alta      | Alta       | Correção em andamento |
| 03        | Falha ao alternar variações de produto             | Alta      | Alta       | Pendente              |
| 04        | Checkout permite avançar sem login ou confirmação  | Alta      | Alta       | Correção em andamento |
| 05        | Formulário aceita e-mail inválido sem mensagem     | Média     | Média      | Pendente              |
| 06        | Página de comparação difícil acesso                | Baixa     | Baixa      | A considerar          |
| 07        | Falta de validação de campos de telefone/CEP       | Média     | Média      | Pendente              |
| 08        | Erro ao tentar adicionar novo endereço no checkout | Alta      | Alta       | Pendente              |
| 09        | Falha de segurança ao pular etapas do checkout     | Alta      | Alta       | Correção em andamento |

---

### 📌 Priorização dos Defeitos

* **Prioridade Alta:** Defeitos que afetam diretamente o fluxo principal ou comprometem a segurança e confiabilidade do sistema.
* **Prioridade Média:** Defeitos que afetam a usabilidade ou funcionalidades secundárias, mas sem impedir o uso básico.
* **Prioridade Baixa:** Defeitos que impactam apenas a experiência do usuário ou são melhorias visuais/facilidade de uso.
### 🔥 Ações em Andamento

* Bugs de alta prioridade estão sendo tratados imediatamente e serão incluídos no próximo sprint de correções.
* Bugs de prioridade média estão sendo planejados para futuras releases.
* Bugs de prioridade baixa foram documentados como melhorias para futuras sprints.
