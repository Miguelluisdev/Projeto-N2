# 📝 Relatório de Testes Manuais - Cenário 01: Detalhes do Produto

## 🔗 URL Testada
[https://qazando-shop.com
](https://automationpratice.com.br/)

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
| 01 - Deve exibir corretamente todas as informações do produto                                            | ✅ Passou  |
| 02 - Deve trocar a imagem principal ao clicar nas miniaturas da galeria                                   | ❌ Não Passou - Erro grave: miniaturas não alteram a imagem principal |
| 03 - Deve refletir corretamente a seleção de variações do produto                                         | ❌ Não Passou - Alteração de cor troca para outro produto e tamanho não funciona |
| 04 - Deve permitir alterar a quantidade do produto antes da compra                                        | ✅ Passou  |
| 05 - Deve adicionar o produto ao carrinho com variações selecionadas                                      | ❌ Não Passou - Não existem variações, apenas adiciona ao carrinho |
| 06 - Deve adicionar o produto ao carrinho sem variações obrigatórias                                      | ✅ Passou  |
| 07 - Deve exibir erro ao tentar adicionar ao carrinho sem selecionar variações obrigatórias                | ❌ Não Passou - Não existem variações a serem validadas |
| 08 - Deve exibir erro ao tentar adicionar produto fora de estoque                                         | ❌ Não Passou - Produtos fora de estoque são adicionados sem validação |
| 09 - Deve exibir erro ao tentar adicionar quantidade inválida (0, negativa ou não numérica)               | ✅ Passou  |
| 10 - A alteração de variação deve atualizar corretamente preço, imagem e disponibilidade                   | ❌ Não Passou - Não existem variações, sem efeito |
| 11 - Não deve permitir adicionar quantidade maior que o estoque disponível                                 | ❌ Não Passou - Estoque não é verificado |

---

## 🚨 Bugs e Falhas Encontrados

✅ **Miniaturas não alteram a imagem principal**: UX ruim e confusão para o usuário.

✅ **Seleção de variações falha**: alterar cor/tamanho troca para outro produto ou não funciona.

✅ **Adição de itens fora de estoque**: sem verificação, permitindo adicionar ao carrinho.

✅ **Estoque não é respeitado**: não limita a quantidade máxima, sem erro ao exceder estoque.

---

## 🟡 Análise Rápida

O módulo de **detalhes do produto** apresenta falhas críticas em:  
- Interação visual com a galeria (miniaturas).  
- Falta de verificação de estoque, permitindo inconsistências no pedido.  
- Ausência ou falha no controle de variações.  

Essas falhas impactam diretamente a confiabilidade do site e a experiência do usuário, podendo gerar pedidos inconsistentes ou enganosos.

---

## 🔍 Testes que Passaram

✅ Exibição completa das informações do produto.  
✅ Alteração de quantidade do produto antes da compra.  
✅ Adição ao carrinho sem necessidade de variações (quando não existem).  
✅ Mensagem de erro ao tentar adicionar quantidade inválida.

---

## 🚧 Testes que Falharam

❌ Alteração da imagem principal via miniaturas.  
❌ Seleção de variações (não existem ou não funcionam).  
❌ Falha no bloqueio de itens fora de estoque.  
❌ Estoque máximo não respeitado.

---

## ⚙️ Conclusão

A tela de detalhes do produto precisa de correções importantes para:  
- Implementar corretamente a troca de imagens nas miniaturas.  
- Corrigir ou implementar as variações e suas interações (cor, tamanho).  
- Verificar e bloquear produtos fora de estoque.  
- Impedir adição de quantidades superiores ao estoque.
