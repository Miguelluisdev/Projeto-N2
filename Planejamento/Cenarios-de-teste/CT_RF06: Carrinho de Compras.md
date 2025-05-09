<a id="top"></a>

# Cenários e Casos de Teste RF06

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Visualização de Itens no Carrinho

#### Caso de Teste 01: Deve exibir corretamente múltiplos itens no carrinho com detalhes e subtotais.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT01 | Visualização de Itens: Adicionar múltiplos itens diferentes e com variações ao carrinho. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter itens diferentes (com ou sem variações) no carrinho. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário adicionou múltiplos itens ao carrinho               |
| **QUANDO** o usuário visualiza o carrinho                                  |
| **ENTÃO** todos os itens devem ser listados corretamente com suas variações, detalhes e subtotais. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O carrinho deve exibir corretamente os itens, suas variações (se houver), preço, quantidade e subtotais. |

#### Caso de Teste 02: Deve atualizar a quantidade do item corretamente.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT02 | Atualização de Quantidade: Aumentar/diminuir quantidade de item e recalcular subtotal. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O item deve estar presente no carrinho.       |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem um item no carrinho                               |
| **QUANDO** o usuário aumenta ou diminui a quantidade do item                  |
| **ENTÃO** o subtotal do item e o total do carrinho devem ser recalculados corretamente. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O subtotal do item e o total do carrinho devem ser atualizados corretamente. |

#### Caso de Teste 03: Deve permitir a remoção de um item do carrinho.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT03 | Remoção de Item: Remover um item e recalcular o total.                             |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O item deve estar presente no carrinho.       |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem um item no carrinho                               |
| **QUANDO** o usuário remove o item do carrinho                               |
| **ENTÃO** o item deve ser removido da lista e o total do carrinho recalculado. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O item deve ser removido corretamente e o total recalculado. |

#### Caso de Teste 04: Deve permitir a remoção de todos os itens do carrinho.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT04 | Remoção de Todos os Itens: Remover todos os itens e mostrar mensagem apropriada. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O carrinho deve conter múltiplos itens.       |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem múltiplos itens no carrinho                      |
| **QUANDO** o usuário remove todos os itens                                      |
| **ENTÃO** o carrinho deve ficar vazio e exibir a mensagem "Carrinho vazio". |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O carrinho deve ser esvaziado corretamente e a mensagem apropriada exibida. |

#### Caso de Teste 05: Deve aplicar cupom válido e recalcular o total.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT05 | Aplicação de Cupom Válido: Inserir cupom válido e recalcular total.                |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O cupom deve ser válido e aplicável.          |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem um cupom válido                                    |
| **QUANDO** o usuário insere o cupom no campo de cupom e clica em aplicar      |
| **ENTÃO** o desconto do cupom deve ser aplicado e o total recalculado.       |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O total do carrinho deve ser recalculado corretamente com o desconto do cupom. |

#### Caso de Teste 06: Deve navegar para a página "Continuar Comprando".

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT06 | Navegação "Continuar Comprando": Deve navegar para a página de compras ao clicar.   |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar no carrinho.             |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho                           |
| **QUANDO** o usuário clica no botão "Continuar Comprando"                  |
| **ENTÃO** o sistema deve levar o usuário de volta à página de categorias ou homepage. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O botão deve redirecionar corretamente o usuário para a página de compras. |

#### Caso de Teste 07: Deve navegar para a página de "Finalizar Compra".

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT07 | Navegação "Finalizar Compra": Deve navegar para a página de finalização ao clicar.    |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter itens no carrinho.         |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem itens no carrinho                                 |
| **QUANDO** o usuário clica no botão "Finalizar Compra"                      |
| **ENTÃO** o sistema deve levar o usuário à página de finalização de compra. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O botão "Finalizar Compra" deve redirecionar corretamente para a página de checkout. |

#### Caso de Teste 08: Deve exibir erro ao tentar atualizar quantidade para valor inválido.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT08 | Atualizar Quantidade para Inválida: Tentar atualizar quantidade para 0, negativa ou não numérica. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O item deve estar presente no carrinho.       |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tenta atualizar a quantidade para 0, valor negativo ou não numérico |
| **QUANDO** o usuário clica em "Atualizar"                                    |
| **ENTÃO** deve ser exibida uma mensagem de erro ou o item deve ser removido. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro ou remover o item caso a quantidade seja inválida. |

#### Caso de Teste 09: Deve exibir erro ao tentar aplicar um cupom inválido ou expirado.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT09 | Aplicar Cupom Inválido/Expirado: Tentar usar cupom inválido ou expirado.            |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O cupom deve ser inválido ou expirado.        |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tenta aplicar um cupom inválido ou expirado         |
| **QUANDO** o usuário insere o cupom no campo e clica em aplicar            |
| **ENTÃO** deve ser exibida uma mensagem de erro informando que o cupom não pode ser usado. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro informando que o cupom é inválido ou expirado. |

#### Caso de Teste 10: Deve verificar precisão dos cálculos de subtotais e totais.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT10 | Cálculos de Subtotais e Totais: Verificar precisão dos cálculos em diversas situações. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O carrinho deve conter itens com preços e descontos aplicados. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o carrinho contém itens com descontos e variáveis de preço |
| **QUANDO** o usuário visualiza o total do carrinho                         |
| **ENTÃO** o subtotal e o total final devem ser calculados corretamente.   |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| Os cálculos de subtotais e totais devem ser precisos e refletir todas as mudanças. |

#### Caso de Teste 11: Deve impedir a aplicação de múltiplos cupons, se a regra for permitir apenas um.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C06-CT11 | Limite de Cupons: Impedir aplicação de mais de um cupom.                            |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter cupons válidos disponíveis. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o sistema permite apenas um cupom por compra                   |
| **QUANDO** o usuário tenta aplicar um segundo cupom                         |
| **ENTÃO** o sistema deve exibir uma mensagem indicando que apenas um cupom pode ser usado. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve impedir a aplicação de mais de um cupom. |
