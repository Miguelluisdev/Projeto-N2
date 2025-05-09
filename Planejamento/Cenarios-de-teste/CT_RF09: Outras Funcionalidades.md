<a id="top"></a>

# Cenários e Casos de Teste RF09

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Formulário de Contato

#### Caso de Teste 01: Envio com Sucesso

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT01 | Envio com Sucesso: Preencher todos os campos do formulário de contato com dados válidos e enviar, recebendo mensagem de sucesso. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve preencher todos os campos obrigatórios com dados válidos. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário preencheu todos os campos do formulário com dados válidos |
| **QUANDO** o usuário submete o formulário                                    |
| **ENTÃO** o sistema deve exibir uma mensagem de sucesso confirmando o envio. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O formulário deve ser submetido com sucesso e uma mensagem de sucesso deve ser exibida. |

#### Caso de Teste 02: Envio - Campos Obrigatórios Vazios

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT02 | Envio - Campos Obrigatórios Vazios: Tentar enviar sem Assunto, Email ou Mensagem.    |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O formulário de contato deve ter campos obrigatórios como Assunto, Email e Mensagem. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário deixa um dos campos obrigatórios em branco (Assunto, Email ou Mensagem) |
| **QUANDO** o usuário tenta submeter o formulário                            |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando que o campo obrigatório está vazio. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro quando um campo obrigatório estiver vazio. |

#### Caso de Teste 03: Envio - Email Inválido

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT03 | Envio - Email Inválido: Tentar enviar com formato de email incorreto.                |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O campo de email deve estar presente no formulário. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário insere um email com formato incorreto (ex: sem "@" ou domínio) |
| **QUANDO** o usuário tenta submeter o formulário                            |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando que o formato do email é inválido. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro informando que o email é inválido. |

## Cenário 02: Newsletter

#### Caso de Teste 04: Inscrição com Sucesso

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT04 | Inscrição com Sucesso: Inscrever email válido e receber mensagem de sucesso.         |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve inserir um email válido.         |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário insere um email válido para inscrição              |
| **QUANDO** o usuário clica em "Inscrever"                                    |
| **ENTÃO** o sistema deve exibir uma mensagem de sucesso confirmando a inscrição. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de sucesso quando o email é válido. |

#### Caso de Teste 05: Inscrição - Email Inválido

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT05 | Inscrição - Email Inválido: Tentar inscrever email com formato incorreto.            |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve tentar inscrever um email inválido (ex: sem "@" ou domínio). |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário insere um email com formato incorreto              |
| **QUANDO** o usuário clica em "Inscrever"                                    |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando que o email é inválido. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro quando o email é inválido. |

#### Caso de Teste 06: Inscrição - Email Duplicado

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT06 | Inscrição - Email Duplicado: Tentar inscrever email já existente.                   |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O email que o usuário tenta inscrever já está cadastrado. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tenta inscrever um email já existente               |
| **QUANDO** o usuário clica em "Inscrever"                                    |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando que o email já está cadastrado. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro quando o email já estiver cadastrado. |

## Cenário 03: Comparação de Produtos

#### Caso de Teste 07: Adicionar Produtos à Comparação

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT07 | Adicionar Produtos à Comparação: Adicionar 2 ou mais produtos à lista de comparação. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar na página de comparação. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de comparação de produtos           |
| **QUANDO** o usuário adiciona 2 ou mais produtos à comparação             |
| **ENTÃO** os produtos devem ser adicionados corretamente à lista de comparação. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve permitir adicionar 2 ou mais produtos à comparação. |

#### Caso de Teste 08: Visualizar Página de Comparação

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT08 | Visualizar Página de Comparação: Acessar a página e verificar se os produtos e atributos são exibidos corretamente. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter produtos adicionados à lista de comparação. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem produtos na lista de comparação                 |
| **QUANDO** o usuário acessa a página de comparação                          |
| **ENTÃO** os produtos e seus atributos devem ser exibidos corretamente. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| A página de comparação deve exibir todos os produtos e seus atributos corretamente. |

#### Caso de Teste 09: Remover Produto da Comparação

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT09 | Remover Produto da Comparação: Remover um produto da lista de comparação.             |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter produtos na lista de comparação. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem produtos na lista de comparação                 |
| **QUANDO** o usuário remove um produto da comparação                       |
| **ENTÃO** o produto deve ser removido da lista de comparação. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O produto deve ser removido corretamente da lista de comparação. |

#### Caso de Teste 10: Adicionar ao Carrinho da Comparação

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C09-CT10 | Adicionar ao Carrinho da Comparação: Adicionar produto da comparação ao carrinho.     |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter produtos na lista de comparação. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tem produtos na lista de comparação                 |
| **QUANDO** o usuário clica em "Adicionar ao Carrinho" para um produto da comparação |
| **ENTÃO** o produto deve ser adicionado ao carrinho corretamente. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O produto deve ser adicionado corretamente ao carrinho. |

---

[Voltar ao topo](#top)

