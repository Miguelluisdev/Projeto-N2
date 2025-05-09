<a id="top"></a>

# Cenários e Casos de Teste RF05

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Detalhes do produto

#### Caso de Teste 01: Deve exibir corretamente todas as informações do produto.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT01 | Exibir corretamente todas as informações do produto (nome, descrição, preço, SKU, imagens, disponibilidade). |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve estar disponível na PDP.       |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário acessa a página de detalhes do produto              |
| **QUANDO** o produto for carregado                                          |
| **ENTÃO** as informações do produto devem ser exibidas corretamente (nome, descrição, preço, SKU, imagens, disponibilidade). |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O nome, descrição, preço, SKU, imagens e disponibilidade do produto devem ser exibidos corretamente. |

#### Caso de Teste 02: Deve trocar a imagem principal ao clicar nas miniaturas da galeria.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT02 | Galeria de Imagens: Trocar imagem principal ao clicar nas miniaturas.               |

| **Pré-condições**                               |
| :---------------------------------------------- |
| A PDP deve exibir uma galeria de imagens com miniaturas. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está visualizando a galeria de imagens do produto |
| **QUANDO** o usuário clica em uma miniatura de imagem                       |
| **ENTÃO** a imagem principal da PDP deve ser alterada para a imagem clicada. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| A imagem principal deve ser alterada de acordo com a miniatura selecionada. |

#### Caso de Teste 03: Deve refletir corretamente a seleção de variações do produto.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT03 | Seleção de Variações: Selecionar Tamanho e Cor e refletir alterações.                |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve ter variações de Tamanho e Cor disponíveis. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário visualiza a PDP do produto com variações             |
| **QUANDO** o usuário seleciona uma opção de Tamanho e Cor                    |
| **ENTÃO** a imagem, preço e disponibilidade do produto devem ser atualizados de acordo com as variações selecionadas. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| A PDP deve atualizar a imagem, preço e disponibilidade conforme as variações selecionadas. 

#### Caso de Teste 04: Deve permitir alterar a quantidade do produto antes da compra.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT04 | Seleção de Quantidade: Alterar a quantidade do produto a ser adquirido.            |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve estar disponível para compra.  |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário visualiza a PDP do produto                            |
| **QUANDO** o usuário altera a quantidade no campo de quantidade             |
| **ENTÃO** a quantidade selecionada deve ser atualizada corretamente.       |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| A quantidade deve ser atualizada corretamente sem erro. |

#### Caso de Teste 05: Deve adicionar o produto ao carrinho com variações selecionadas.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT05 | Adicionar ao Carrinho (Com Variações): Adicionar produto com variações selecionadas. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve ter variações (Tamanho/Cor) disponíveis. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário selecionou uma variação de Tamanho e Cor             |
| **QUANDO** o usuário clica em "Adicionar ao Carrinho"                       |
| **ENTÃO** o produto com as variações selecionadas deve ser adicionado ao carrinho. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O produto com as variações selecionadas deve ser adicionado ao carrinho. |

#### Caso de Teste 06: Deve adicionar o produto ao carrinho sem variações obrigatórias.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT06 | Adicionar ao Carrinho (Sem Variações): Adicionar produto sem variações obrigatórias. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto não deve ter variações obrigatórias. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário visualiza a PDP do produto sem variações obrigatórias |
| **QUANDO** o usuário clica em "Adicionar ao Carrinho"                        |
| **ENTÃO** o produto sem variações obrigatórias deve ser adicionado ao carrinho. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O produto deve ser adicionado ao carrinho corretamente, sem necessidade de variação. |

#### Caso de Teste 07: Deve exibir erro ao tentar adicionar ao carrinho sem selecionar variações obrigatórias.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT07 | Adicionar Sem Variação Obrigatória: Tentar adicionar sem selecionar variações obrigatórias. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve ter variações obrigatórias de Tamanho e Cor. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário não selecionou as variações obrigatórias (Tamanho/Cor) |
| **QUANDO** o usuário tenta clicar em "Adicionar ao Carrinho"                 |
| **ENTÃO** deve ser exibida uma mensagem de erro informando que as variações obrigatórias precisam ser selecionadas. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir mensagem de erro indicando que as variações obrigatórias precisam ser selecionadas. |

#### Caso de Teste 08: Deve exibir erro ao tentar adicionar produto fora de estoque.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT08 | Adicionar Produto Fora de Estoque: Tentar adicionar produto marcado como "Fora de Estoque". |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve estar fora de estoque.        |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o produto está fora de estoque                                    |
| **QUANDO** o usuário tenta adicionar o produto ao carrinho                     |
| **ENTÃO** deve ser exibida uma mensagem indicando que o produto não está disponível. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir mensagem de produto indisponível ao tentar adicionar ao carrinho. |

#### Caso de Teste 09: Deve exibir erro ao tentar adicionar quantidade inválida (0, negativa ou não numérica).

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT09 | Quantidade Inválida: Tentar adicionar quantidade inválida (0, negativa ou letras).   |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve estar disponível para compra.  |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tenta adicionar uma quantidade inválida (0, negativa ou letras) |
| **QUANDO** o usuário clica em "Adicionar ao Carrinho"                       |
| **ENTÃO** deve ser exibida uma mensagem de erro informando que a quantidade é inválida. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro ao tentar adicionar quantidade inválida. |

#### Caso de Teste 10: A alteração de variação deve atualizar corretamente preço, imagem e disponibilidade.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT10 | Atualização Dinâmica (RN17): Verificar se a alteração de variação atualiza preço/imagem/estoque. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve ter variações e estar disponível para compra. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário seleciona uma variação diferente do produto          |
| **QUANDO** a variação for alterada                                              |
| **ENTÃO** o preço, imagem e estoque devem ser atualizados automaticamente. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve atualizar as informações de preço, imagem e estoque automaticamente. |

#### Caso de Teste 11: Não deve permitir adicionar quantidade maior que o estoque disponível.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C05-CT11 | Limite de Estoque (RN21): Tentar adicionar quantidade maior que o estoque disponível. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O produto deve ter um estoque limitado.       |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o produto tem estoque limitado                                    |
| **QUANDO** o usuário tenta adicionar uma quantidade maior que o estoque disponível |
| **ENTÃO** o sistema deve impedir a adição e exibir mensagem informando o limite de estoque. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir mensagem de erro ao tentar adicionar quantidade maior que o estoque disponível. |
