<a id="top"></a>

# Cenários e Casos de Teste RF08

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Submissão com Todos os Campos Válidos

#### Caso de Teste 01: Deve permitir a submissão de um formulário com todos os campos válidos.

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C08-CT01 | Submissão com Todos os Campos Válidos: Preencher formulário com dados válidos e submeter com sucesso. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O usuário deve preencher todos os campos obrigatórios com dados válidos. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário preencheu todos os campos obrigatórios com dados válidos |
| **QUANDO** o usuário submete o formulário                                    |
| **ENTÃO** o formulário deve ser submetido com sucesso. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O formulário deve ser submetido com sucesso quando todos os campos estiverem válidos. |

#### Caso de Teste 02: Campo Obrigatório Vazio

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C08-CT02 | Campo Obrigatório Vazio: Deixar campo obrigatório em branco e tentar submeter.         |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O formulário deve ter campos obrigatórios.    |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário não preencheu um campo obrigatório                   |
| **QUANDO** o usuário tenta submeter o formulário                            |
| **ENTÃO** o sistema deve exibir uma mensagem de erro para o campo obrigatório em branco. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro quando um campo obrigatório estiver vazio. |

#### Caso de Teste 03: Formato Inválido (Email)

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C08-CT03 | Formato Inválido (Email): Inserir email sem "@" ou sem domínio e tentar submeter.     |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O campo de email deve estar presente no formulário. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário insere um email sem "@" ou domínio                 |
| **QUANDO** o usuário tenta submeter o formulário                            |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando o formato inválido do email. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro informando o formato inválido do email. |

#### Caso de Teste 04: Formato Inválido (Telefone/CEP/Outros)

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C08-CT04 | Formato Inválido (Telefone/CEP/Outros): Inserir dados em formatos incorretos e tentar submeter. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O formulário deve conter campos de telefone, CEP ou outros com validação de formato. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário insere dados em formato incorreto (telefone, CEP, etc.) |
| **QUANDO** o usuário tenta submeter o formulário                            |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando o formato inválido. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro informando o formato inválido do telefone, CEP ou outros campos. |

#### Caso de Teste 05: Validação Client-Side e Server-Side

| ID       | Descrição                                                                             |
| :------- | :------------------------------------------------------------------------------------ |
| C08-CT05 | Validação Client-Side e Server-Side: Submeter formulário com erro, verificar feedback client-side e depois desabilitar JS para verificar validação server-side. |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O formulário deve ter validações client-side e server-side implementadas. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário tenta submeter um formulário com erro de validação  |
| **QUANDO** o formulário é submetido com erro e o feedback client-side é exibido |
| **E** o JavaScript é desabilitado                                              |
| **ENTÃO** o sistema deve retornar erro via server-side para o mesmo formulário. |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| O sistema deve exibir um feedback de erro tanto client-side quanto server-side quando o formulário contiver erros. |

---

[Voltar ao topo](#top)

