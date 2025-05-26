# 🐞 Análise de Relatório de Bugs 

## 📊 Resumo Geral

- **Total de Bugs Encontrados**: 12
- **Total de Melhorias Identificadas**: 2

---

## 🚦 Prioridade dos Bugs

| Prioridade | Quantidade | Descrição                                                                                                 |
|------------|------------|-----------------------------------------------------------------------------------------------------------|
| Alta       | 7          | Falhas críticas de segurança, processos de checkout, filtros e ordenação, e controle de estoque.          |
| Média      | 3          | Falhas em validações de formulários e dificuldade de acesso à comparação.                                 |
| Baixa      | 2          | Falhas menores de interface e pequenos erros de fluxo.                                                    |

---

## 🔍 Lista de Bugs Encontrados

| ID    | Descrição                                                                                         | Prioridade | Urgência    | Correção Recomendada                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------|------------|-------------|-----------------------------------------------------------------------------------------------------------------------|
| BUG-01 | Acesso direto a páginas internas via URL, sem autenticação.                                        | Alta       | Imediata    | Implementar autenticação obrigatória em rotas restritas.                                                              |
| BUG-02 | Checkout concluído por usuários deslogados.                                                       | Alta       | Imediata    | Validar estado de login antes de permitir a conclusão de compra.                                                      |
| BUG-03 | Falta de verificação de estoque ao adicionar ao carrinho.                                         | Alta       | Alta        | Incluir verificação de estoque em todas as etapas de compra.                                                          |
| BUG-04 | Filtros e ordenação de produtos invertidos (high to low e low to high).                            | Alta       | Alta        | Corrigir lógica de ordenação e filtros na listagem de produtos.                                                       |
| BUG-05 | Alterar variações de produtos carrega itens errados ou não carrega corretamente.                    | Alta       | Alta        | Corrigir lógica de carregamento de variações no backend e frontend.                                                   |
| BUG-06 | Falha de segurança no checkout ao pular etapas via URL.                                           | Alta       | Imediata    | Implementar controle de fluxo e sessões para forçar a ordem correta de etapas.                                         |
| BUG-07 | Campos de telefone/CEP não possuem validação.                                                     | Média      | Média       | Implementar validação de campos no frontend (client-side) e backend (server-side).                                     |
| BUG-08 | Falta de opção para adicionar novo endereço no checkout.                                          | Alta       | Alta        | Incluir funcionalidade de adicionar novo endereço.                                                                    |
| BUG-09 | Página de comparação difícil de acessar (apenas por URL ou footer).                               | Média      | Média       | Melhorar a UX: adicionar botão de comparação mais visível na interface.                                               |
| BUG-10 | Email inválido aceito no formulário de contato sem aviso ou mensagem obrigatória.                   | Alta       | Alta        | Adicionar validação de e-mail e obrigatoriedade de mensagem antes de permitir envio.                                  |
| BUG-11 | Falha na confirmação final de pedido - não existe confirmação de sucesso.                          | Alta       | Alta        | Implementar página de confirmação final após checkout.                                                                |
| BUG-12 | Falta de validação de quantidade ao adicionar ao carrinho (0, negativa ou não numérica).            | Baixa      | Baixa       | Adicionar validação de quantidade no frontend e backend.                                                              |

---

## ✨ Melhorias Identificadas

| ID        | Descrição                                                       | Urgência    | Sugestão                                                                                                 |
|-----------|------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------|
| MELH-01   | Tornar a página de comparação de produtos mais acessível.        | Média       | Adicionar botão de comparação direto na página de listagem e produto.                                   |
| MELH-02   | Melhorar feedback de erros de formulários (mensagens claras).    | Média       | Exibir mensagens de erro claras e amigáveis para os usuários ao preencher campos incorretos.             |

---

## ⚠️ Falha, Erro e Defeito

- **Falha (Failure)**: Comportamento observado que não atende ao comportamento esperado (ex.: checkout sem login, ordenação invertida).
- **Erro (Error)**: Falha de lógica ou omissão no código (ex.: falta de verificação de login, ausência de validação nos formulários).
- **Defeito (Bug)**: Resultado de erros no código que causam falhas nos testes (ex.: produtos fora de estoque sendo adicionados ao carrinho).

---

## 🔎 Causa Raiz dos Bugs

| Área                     | Causa Raiz                                                               |
|--------------------------|--------------------------------------------------------------------------|
| Segurança e Autenticação | Falta de autenticação e controle de sessão em rotas críticas.            |
| Validações               | Ausência de validação nos formulários e campos obrigatórios.              |
| Lógica de Produto        | Falha na lógica de variações, filtros e controle de estoque.              |
| UX e Navegação           | Interface com caminhos não intuitivos (ex.: comparação).                  |

---

## 🏷️ Urgência e Correção

- 🚨 **Urgência Imediata**: Bugs de segurança e processos de checkout (ex.: BUG-01, BUG-02, BUG-06).  
- 🛠️ **Correção Alta**: Lógica de filtros, ordenação e controle de estoque (ex.: BUG-03, BUG-04, BUG-05).  
- ⚙️ **Correção Média**: Melhorias de UX e validação de formulários (ex.: BUG-07, MELH-01).  

---

## 🟩 Conclusão

O sistema precisa de **ações prioritárias de correção em segurança e lógica de processos de compra**. Além disso, melhorias na UX e validações em campos de formulários vão aumentar a confiabilidade e a satisfação dos usuários. 🚀
