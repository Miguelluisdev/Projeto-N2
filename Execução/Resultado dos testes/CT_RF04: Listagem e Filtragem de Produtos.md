# 📝 Relatório de Testes Manuais - Cenário 01: Listagem de Produtos

## 🔗 URL Testada
[https://qazando-shop.com](https://automationpratice.com.br/)

## 🗓️ Data dos Testes
24/05/2025

## 👤 Testador
Miguel Luis

## 💻 Ambiente de Testes

| Item                | Detalhes                                 |
|----------------------|------------------------------------------|
| Sistema Operacional  | Windows 11                               |
| Navegador            | Microsoft Edge 136.0v                    |
| Tipo de Teste        | Exploratório e casos de teste manuais    |

---

## 📌 Casos de Teste Executados

| Caso de Teste                                                                                           | Status    |
|----------------------------------------------------------------------------------------------------------|-----------|
| 01 - Deve exibir corretamente os produtos de uma categoria acessada                                       | ❌ Não Passou - Ao acessar a PLP, nomes digitados não alteram resultados, mas exibe preço e imagem |
| 02 - Deve permitir navegação entre páginas da PLP (paginação)                                            | ✅ Passou  |
| 03 - Deve ordenar os produtos corretamente por critérios selecionados                                     | ❌ Não Passou - Filtros estão invertidos ("High to Low" exibe itens baratos e "Low to High" exibe caros) |
| 05 - Deve exibir corretamente a visualização rápida de um produto (Quick View)                            | ✅ Passou  |
| 06 - Deve permitir adicionar ao carrinho diretamente da PLP                                               | ✅ Passou  |
| 07 - Deve bloquear adição ao carrinho diretamente da PLP caso o produto esteja fora de estoque            | ❌ Não Passou - Permite adicionar produtos fora de estoque ao carrinho |

---

## 🚨 Bugs e Falhas Encontrados

✅ **Busca de produtos sem efeito visível**: Mesmo digitando o nome de produtos na categoria acessada, a listagem permanece a mesma (não filtra corretamente).

✅ **Erro de ordenação/filtro**: Filtros de preço estão invertidos — "High to Low" exibe o mais barato primeiro, e "Low to High" exibe o mais caro primeiro. Outros itens não alteram nada.

✅ **Falha em bloqueio de estoque**: Permite adicionar produtos fora de estoque ao carrinho diretamente da PLP, causando problemas de integridade no pedido.

---

## 🟡 Análise Rápida

O módulo de **listagem de produtos** apresenta falhas críticas em funcionalidades essenciais:  
- **Busca por nome não filtra resultados**: impacta diretamente a experiência do usuário.  
- **Ordenação invertida**: gera confusão e desconfiança na plataforma.  
- **Bloqueio de estoque falho**: representa um erro grave de fluxo de vendas e de controle de inventário.

---

## 🔍 Testes que Passaram

✅ Paginação entre páginas da PLP funciona corretamente.  
✅ Visualização rápida do produto funciona normalmente.  
✅ Adição ao carrinho de produtos disponíveis funciona corretamente.

---

## 🚧 Testes que Falharam

❌ Busca por nome não afeta a listagem de produtos.  
❌ Ordenação e filtros apresentam resultados invertidos.  
❌ Produtos fora de estoque são adicionados ao carrinho sem bloqueio.  

---

## ⚙️ Conclusão

O módulo de listagem precisa de ajustes críticos para:  
- Corrigir o filtro e ordenação de produtos.  
- Garantir bloqueio de itens fora de estoque.  
- Revisar a busca/filtragem por nome na PLP para evitar confusão do usuário.
