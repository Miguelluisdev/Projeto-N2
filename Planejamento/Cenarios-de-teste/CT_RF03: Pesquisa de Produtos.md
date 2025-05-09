<a id="top"></a>

# Cenários e Casos de Teste RF03

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 03: Pesquisa de Produtos

#### Caso de Teste 01: Deve exibir produtos relevantes ao pesquisar por um termo existente (ex: "notebook").

| ID       | Descrição                                                                     |
| :------- | :------------------------------------------------------------------------------ |
| C03-CT01 | Deve exibir produtos relevantes ao pesquisar por um termo existente (ex: "notebook"). |

| **Pré-condições**                             |
| :-------------------------------------------- |
| O termo pesquisado deve corresponder a produtos cadastrados no sistema. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na Homepage                                    |
| **E** preenche "notebook" no campo de busca                                |
| **QUANDO** clicar no botão de pesquisa                                     |
| **ENTÃO** deve ser exibida uma lista de produtos relevantes relacionados ao termo |

| **Critérios de aceitação**                                                      |
| :------------------------------------------------------------------------------- |
| A lista de produtos deve conter ao menos um item relacionado ao termo buscado.  |
| Os produtos exibidos devem conter o termo “notebook” no nome ou descrição.      |

#### Caso de Teste 02: Deve encontrar o produto ao pesquisar por parte do nome ou SKU

| ID       | Descrição                                                               |
| :------- | :------------------------------------------------------------------------ |
| C03-CT02 | Deve encontrar o produto ao pesquisar por parte do nome ou SKU. |

| **Pré-condições**                                     |
| :---------------------------------------------------- |
| O produto deve estar cadastrado com o nome ou SKU buscado. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na Homepage                                    |
| **E** preenche "smart" ou parte do SKU no campo de busca                   |
| **QUANDO** clicar no botão de pesquisa                                     |
| **ENTÃO** o sistema deve listar os produtos correspondentes à busca parcial |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O(s) produto(s) retornado(s) devem conter o trecho pesquisado no nome ou no SKU. |

#### Caso de Teste 03: Deve aplicar ordenação e/ou filtros com sucesso após uma busca.

| ID       | Descrição                                                                   |
| :------- | :-------------------------------------------------------------------------- |
| C03-CT03 | Deve aplicar ordenação e/ou filtros com sucesso após uma busca.             |

| **Pré-condições**                                     |
| :---------------------------------------------------- |
| A busca deve retornar múltiplos produtos.             |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário realizou uma busca por "tablet"                     |
| **E** a página exibe resultados                                            |
| **QUANDO** selecionar o filtro "Preço: menor para maior"                  |
| **ENTÃO** os produtos devem ser reordenados corretamente                   |

| **Critérios de aceitação**                                                  |
| :--------------------------------------------------------------------------- |
| A ordem dos produtos deve refletir o filtro/ordenação escolhido.            |

#### Caso de Teste 04: Deve exibir mensagem "Nenhum resultado encontrado" ao pesquisar por termo inexistente (ex: "xyz123abc").

| ID       | Descrição                                                                         |
| :------- | :-------------------------------------------------------------------------------- |
| C03-CT04 | Deve exibir mensagem "Nenhum resultado encontrado" ao pesquisar termo inexistente. |

| **Pré-condições**                             |
| :-------------------------------------------- |
| O termo pesquisado não deve estar associado a nenhum produto no sistema. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na Homepage                                    |
| **E** preenche "xyz123abc" no campo de busca                               |
| **QUANDO** clicar no botão de pesquisa                                     |
| **ENTÃO** deve ser exibida a mensagem "Nenhum resultado encontrado"       |

| **Critérios de aceitação**                                                 |
| :-------------------------------------------------------------------------- |
| Nenhum produto deve ser exibido.                                            |
| Deve aparecer a mensagem clara de que não houve resultados.                 |

#### Caso de Teste 05: Deve lidar corretamente com tentativa de busca com campo vazio.

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C03-CT05 | Deve lidar corretamente com tentativa de busca com campo vazio.        |

| **Pré-condições**                     |
| :------------------------------------ |
| O campo de busca deve estar em branco. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na Homepage                                    |
| **E** o campo de busca está vazio                                          |
| **QUANDO** clicar no botão de pesquisa                                     |
| **ENTÃO** o sistema deve exibir um alerta ou impedir a ação                |

| **Critérios de aceitação**                                                     |
| :------------------------------------------------------------------------------ |
| O sistema não deve realizar a busca.                                            |
| Uma mensagem de erro ou alerta deve ser exibida para o usuário.                |
