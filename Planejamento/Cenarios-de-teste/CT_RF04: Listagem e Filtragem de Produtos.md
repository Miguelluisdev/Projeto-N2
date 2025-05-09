<a id="top"></a>

# Cenários e Casos de Teste RF04

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01 Listagem de produtos

#### Caso de Teste 01: Deve exibir corretamente os produtos de uma categoria acessada.

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C04-CT01 | Deve exibir corretamente os produtos de uma categoria acessada.          |

| **Pré-condições**                                       |
| :------------------------------------------------------ |
| A categoria selecionada deve conter produtos cadastrados. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário acessa a categoria "Notebooks"                      |
| **QUANDO** a página de listagem de produtos for carregada                  |
| **ENTÃO** os produtos exibidos devem pertencer à categoria e mostrar imagem, nome e preço |

| **Critérios de aceitação**                                                              |
| :--------------------------------------------------------------------------------------- |
| Todos os produtos devem exibir imagem, nome e preço.                                     |
| Todos os produtos devem pertencer à categoria acessada.                                 |

#### Caso de Teste 02: Deve permitir navegação entre páginas da PLP (paginação).

| ID       | Descrição                                                                    |
| :------- | :--------------------------------------------------------------------------- |
| C04-CT02 | Deve permitir navegação entre páginas da PLP (paginação).                     |

| **Pré-condições**                                           |
| :---------------------------------------------------------- |
| A categoria deve ter mais produtos do que os exibidos por página. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na página 1 da categoria "Smartphones"         |
| **QUANDO** clicar em "Próxima Página"                                      |
| **ENTÃO** a próxima página de produtos deve ser carregada                  |
| **E** deve haver opção de voltar ou navegar por número da página          |

| **Critérios de aceitação**                                                                 |
| :------------------------------------------------------------------------------------------ |
| A navegação entre páginas deve ser funcional (próxima, anterior e número da página).       |
| Os produtos devem mudar conforme a página acessada.                                         |

#### Caso de Teste 03: Deve ordenar os produtos corretamente por critérios selecionados.

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C04-CT03 | Deve ordenar os produtos corretamente por critérios selecionados.         |

| **Pré-condições**                            |
| :------------------------------------------- |
| A PLP deve conter múltiplos produtos com variações de nome e preço. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na PLP da categoria "Acessórios"               |
| **QUANDO** selecionar "Preço: do menor para o maior"                       |
| **ENTÃO** os produtos devem ser reordenados corretamente                   |
| **E** deve ser possível escolher outras ordenações como "Nome A-Z" ou "Estoque" |

| **Critérios de aceitação**                                                          |
| :----------------------------------------------------------------------------------- |
| A ordenação deve refletir fielmente o critério selecionado.                         |
| A PLP deve atualizar os produtos exibidos de forma dinâmica e sem falhas.           |

#### Caso de Teste 05: Deve exibir corretamente a visualização rápida de um produto (Quick View).

| ID       | Descrição                                                               |
| :------- | :---------------------------------------------------------------------- |
| C04-CT05 | Deve exibir corretamente a visualização rápida de um produto (Quick View). |

| **Pré-condições**                         |
| :---------------------------------------- |
| O recurso de Quick View deve estar implementado na PLP. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na PLP                                         |
| **QUANDO** clicar no botão de visualização rápida de um produto            |
| **ENTÃO** uma janela/modal deve abrir com informações resumidas do produto |
| **E** deve haver botão para adicionar ao carrinho                          |

| **Critérios de aceitação**                                                         |
| :---------------------------------------------------------------------------------- |
| A visualização rápida deve exibir imagem, nome, preço, descrição e botão de compra.|
| A adição ao carrinho via Quick View deve funcionar corretamente (se aplicável).    |

### Caso de Teste 06: Deve permitir adicionar ao carrinho diretamente da PLP.

| ID       | Descrição                                                                     |
| :------- | :---------------------------------------------------------------------------- |
| C04-CT06 | Deve permitir adicionar ao carrinho diretamente da PLP (quando aplicável).    |

| **Pré-condições**                                        |
| :-------------------------------------------------------- |
| O produto não deve requerer seleção de variação obrigatória (ex: cor, tamanho). |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário visualiza um produto simples na PLP                 |
| **QUANDO** clicar no botão "Adicionar ao carrinho"                        |
| **ENTÃO** o produto deve ser adicionado ao carrinho diretamente            |

| **Critérios de aceitação**                                               |
| :------------------------------------------------------------------------ |
| O produto deve aparecer no carrinho com a quantidade atualizada.          |
| A interface deve confirmar visualmente a adição (ex: mensagem ou modal).  |

#### Caso de Teste 07: Deve bloquear adição ao carrinho diretamente da PLP caso o produto esteja fora de estoque.

| ID       | Descrição                                                                                   |
| :------- | :------------------------------------------------------------------------------------------ |
| C04-CT07 | Deve bloquear adição ao carrinho diretamente da PLP caso o produto esteja fora de estoque.  |

| **Pré-condições**                         |
| :---------------------------------------- |
| O produto exibido na PLP deve estar sem estoque. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário visualiza um produto esgotado na PLP               |
| **QUANDO** tentar clicar em "Adicionar ao carrinho"                       |
| **ENTÃO** o botão deve estar desabilitado ou deve ser exibida uma mensagem de indisponibilidade |

| **Critérios de aceitação**                                                             |
| :-------------------------------------------------------------------------------------- |
| Produtos fora de estoque não devem ser adicionáveis diretamente da PLP.                |
| Uma mensagem clara de "Produto indisponível" deve ser exibida ou o botão deve estar inativo. |

