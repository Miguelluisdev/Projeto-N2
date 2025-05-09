<a id="top"></a>

# Cenários e Casos de Teste RF07

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Checkout Completo (Usuário Logado)

#### Caso de Teste 01: Usuário logado deve completar o processo de checkout.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT01 | Checkout Completo (Usuário Logado): Passar por todas as etapas do checkout e finalizar o pedido. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar logado na conta.          |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está logado na conta                                |
| **QUANDO** o usuário completa as etapas do checkout (Resumo, Endereços, Frete, Pagamento, Confirmação) |
| **ENTÃO** o usuário deve visualizar a página de sucesso e receber um e-mail de confirmação. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O checkout deve ser concluído com sucesso, e o usuário deve receber um e-mail de confirmação. |

#### Caso de Teste 02: Checkout Completo (Usuário Novo - Registro no Checkout)

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT02 | Checkout Completo (Usuário Novo): Criar conta durante o checkout e finalizar o pedido. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve não estar logado.               |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário não está logado                                            |
| **QUANDO** o usuário inicia o checkout e cria uma conta durante a etapa de login |
| **ENTÃO** o usuário deve completar o checkout com sucesso e visualizar a página de sucesso. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O checkout deve ser concluído com sucesso, e o usuário deve ser registrado e redirecionado para a página de sucesso. |

#### Caso de Teste 03: Checkout - Usar Endereço de Faturamento Diferente

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT03 | Checkout - Usar Endereço de Faturamento Diferente: Selecionar endereço de faturamento diferente. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar no passo de Endereços do checkout. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na etapa de Endereços do checkout                  |
| **QUANDO** o usuário desmarca a opção "usar o mesmo endereço" e seleciona ou preenche um endereço de faturamento diferente |
| **ENTÃO** o sistema deve exibir o endereço de faturamento correto.           |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve permitir a seleção de um endereço de faturamento diferente. |

#### Caso de Teste 04: Checkout - Adicionar Novo Endereço

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT04 | Checkout - Adicionar Novo Endereço: Adicionar um novo endereço durante o checkout.  |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar no passo de Endereços do checkout. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na etapa de Endereços do checkout                  |
| **QUANDO** o usuário adiciona um novo endereço de entrega ou faturamento      |
| **ENTÃO** o sistema deve permitir a adição do novo endereço.                  |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve permitir a adição de um novo endereço e salvá-lo corretamente. |

## Cenário 02: Validações no Checkout

#### Caso de Teste 05: Tentar Avançar Sem Selecionar Endereço

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT05 | Tentar Avançar Sem Selecionar Endereço: Não selecionar/confirmar endereço e tentar prosseguir. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar na etapa de Endereços.   |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na etapa de Endereços do checkout               |
| **QUANDO** o usuário tenta avançar sem selecionar um endereço               |
| **ENTÃO** o sistema deve impedir o avanço e exibir uma mensagem de erro.   |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir um erro e impedir o avanço se o endereço não for selecionado. |

#### Caso de Teste 06: Tentar Avançar Sem Selecionar Frete

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT06 | Tentar Avançar Sem Selecionar Frete: Não escolher opção de frete e tentar prosseguir. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar na etapa de Frete.        |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na etapa de Frete do checkout                   |
| **QUANDO** o usuário tenta avançar sem selecionar uma opção de frete       |
| **ENTÃO** o sistema deve impedir o avanço e exibir uma mensagem de erro.   |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir um erro e impedir o avanço se a opção de frete não for escolhida. |

#### Caso de Teste 07: Tentar Avançar Sem Aceitar Termos

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT07 | Tentar Avançar Sem Aceitar Termos: Não marcar "Termos de Serviço" e tentar prosseguir. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar na etapa de Frete do checkout. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na etapa de Frete do checkout                    |
| **QUANDO** o usuário tenta avançar sem aceitar os termos de serviço         |
| **ENTÃO** o sistema deve impedir o avanço e exibir uma mensagem de erro.   |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir um erro e impedir o avanço se os termos de serviço não forem aceitos. |

#### Caso de Teste 08: Tentar Avançar Sem Selecionar Pagamento

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT08 | Tentar Avançar Sem Selecionar Pagamento: Não escolher método de pagamento e tentar prosseguir. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar na etapa de Pagamento.    |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está na etapa de Pagamento do checkout               |
| **QUANDO** o usuário tenta avançar sem escolher um método de pagamento      |
| **ENTÃO** o sistema deve impedir o avanço e exibir uma mensagem de erro.   |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir um erro e impedir o avanço se o método de pagamento não for escolhido. |

#### Caso de Teste 09: Validação de Campos em Novos Endereços

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT09 | Validação de Campos: Erros ao preencher novo endereço durante o checkout.            |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve estar na etapa de Endereços do checkout. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário está adicionando um novo endereço                     |
| **QUANDO** o usuário preenche os campos com dados inválidos (ex: campo vazio, CPF incorreto) |
| **ENTÃO** o sistema deve exibir mensagens de erro para os campos inválidos. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve validar os campos corretamente e exibir mensagens de erro quando os dados forem inválidos. |

## Cenário 03: Acesso Restrito e Confirmação Final

#### Caso de Teste 10: Tentar Pular Etapas do Checkout via URL

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT10 | Acesso Restrito: Tentar pular etapas do checkout via URL sem ter passado pelas anteriores. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário não deve ter completado todas as etapas do checkout. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tenta acessar uma etapa do checkout diretamente via URL |
| **QUANDO** o usuário tenta pular uma etapa                               |
| **ENTÃO** o sistema deve redirecioná-lo para a etapa correta.             |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve redirecionar o usuário para a etapa correta e impedir o avanço. |

#### Caso de Teste 11: Confirmação Final de Pedido

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C07-CT11 | Confirmação Final: O pedido só deve ser finalizado após o clique no botão de confirmação final. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve ter completado todas as etapas do checkout. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário completou todas as etapas do checkout               |
| **QUANDO** o usuário clica em "Confirmar Pedido"                           |
| **ENTÃO** o pedido só deve ser finalizado após o clique na confirmação final. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O pedido só pode ser finalizado após o clique no botão de confirmação final. A confirmação final não pode ser ignorada. |

