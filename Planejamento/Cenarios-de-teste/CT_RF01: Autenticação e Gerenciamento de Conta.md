<a id="top"></a>

# Cenários e Casos de Teste RF01

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Login na plataforma.

#### Caso de Teste 01: Login com as credenciais de e-mail e senha válidas.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT01 | O login será realizado com um e-mail e uma senha válida. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| As credenciais fornecidas (e-mail e senha) devem ser válidas. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login da Automation-Pratice                |
| **E** preenchemos "testedesite@gmail.com" no campo e-mail               |
| **E** preenchemos "qa@1334" no campo senha                         |
| **QUANDO** clicarmos no botão "Acessar"                           |
| **ENTÃO** seremos redirecionados para a página inicial do cliente |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Deve haver o redirecionamento para a página inicial do cliente. |

#### Caso de Teste 02: Login com senha incorreta.

| ID       | Descrição                                     |
| :------- | :-------------------------------------------- |
| C01-CT02 | Tentativa de login com senha incorreta.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O e-mail fornecido deve estar cadastrado no sistema.          |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login da Automation-Pratice               |
| **E** preenchemos testedesite@gmail.com" no campo e-mail               |
| **E** preenchemos "senhaErrada" no campo senha                    |
| **QUANDO** clicarmos no botão "Acessar"                           |
| **ENTÃO** uma mensagem de erro deverá ser exibida na tela         |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| A mensagem "Usuário ou senha inválido" deve ser exibida. |

#### Caso de Teste 03: Login com email não cadastrado.

| ID       | Descrição                                        |
| :------- | :----------------------------------------------- |
| C01-CT03 | Tentativa de login com e-mail não cadastrado.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O e-mail informado não deve estar registrado no sistema.      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login da Automation-Pratice                   |
| **E** preenchemos "naocadastrado@teste.com" no campo e-mail       |
| **E** preenchemos "senha123" no campo senha                       |
| **QUANDO** clicarmos no botão "Acessar"                           |
| **ENTÃO** uma mensagem de erro deverá ser exibida na tela         |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| A mensagem "Usuário ou senha inválido" deve ser exibida. |

#### Caso de Teste 04: Login com email em formato inválido.

| ID       | Descrição                                    |
| :------- | :------------------------------------------- |
| C01-CT04 | Tentativa de login com e-mail em formato inválido. |

| **Pré-condições**                                            |
| :----------------------------------------------------------- |
| O campo de e-mail deve aceitar apenas formatos válidos.      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login da Automation-Pratice                   |
| **E** preenchemos "email-invalido" no campo e-mail                |
| **E** preenchemos "senha123" no campo senha                       |
| **QUANDO** clicarmos no botão "Acessar"                           |
| **ENTÃO** uma mensagem de erro deverá ser exibida na tela         |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| A mensagem "Formato de e-mail inválido" deve ser exibida. |

#### Caso de Teste 05: Login sem fornecer e-mail e senha.

| ID       | Descrição                                      |
| :------- | :--------------------------------------------- |
| C01-CT05 | Tentativa de login sem fornecer e-mail e senha.|

| **Pré-condições**                                     |
| :---------------------------------------------------- |
| Nenhum campo deve estar preenchido ao tentar logar.   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login da Automation-Pratice                   |
| **E** deixamos os campos de e-mail e senha em branco              |
| **QUANDO** clicarmos no botão "Acessar"                           |
| **ENTÃO** uma mensagem de erro deverá ser exibida na tela         |

| **Critérios de aceitação**                                          |
| :----------------------------------------------------------------- |
| A mensagem "Campos obrigatórios não preenchidos" deve ser exibida. |

#### Caso de Teste 06: Deve realizar o Logout com sucesso.

| ID       | Descrição                             |
| :------- | :------------------------------------ |
| C01-CT06 | O usuário deve conseguir fazer logout.|

| **Pré-condições**                                      |
| :----------------------------------------------------- |
| O usuário deve estar autenticado/logado no sistema.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está logado no sistema                     |
| **QUANDO** clicar na opção "Sign out"                             |
| **ENTÃO** deve ser deslogado e redirecionado à tela de login      |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------ |
| O usuário não deve mais ter acesso às áreas restritas do sistema.   |

## Cenário 02: Cadastro na plataforma.

#### Caso de Teste 01: Cadastrar um novo usuário com sucesso.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C02-CT01 | Cadastrar um novo usuário com sucesso. |

| **Pré-condições**                                            |
| :----------------------------------------------------------- |
| O usuário não deve estar cadastrado anteriormente.           |

| **Passos**                                                                    |
| :---------------------------------------------------------------------------- |
| **DADO** que estamos na página de cadastro da Automation-Pratice                      |
| **E** preenchemos "Nome: João Silva", "Email: joao@email.com"                |
| **E** preenchemos "Senha: senha123" e "Confirmação de Senha: senha123"       |
| **E** desmarcamos a opção "Criar conta com saldo"                            |
| **QUANDO** clicarmos no botão "Cadastrar"                                    |
| **ENTÃO** a conta deve ser criada e o usuário redirecionado à tela de login  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A conta deve ser criada com sucesso e sem saldo inicial.        |

#### Caso de Teste 02: Cadastrar sem fornecer os dados obrigatórios.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C02-CT03 | Tentativa de cadastro sem fornecer os dados obrigatórios.|

| **Pré-condições**                                      |
| :----------------------------------------------------- |
| Os campos obrigatórios devem estar vazios.             |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que estamos na página de cadastro da BugBank              |
| **E** deixamos todos os campos vazios                              |
| **QUANDO** clicarmos no botão "Cadastrar"                          |
| **ENTÃO** mensagens de erro devem ser exibidas em todos os campos  |

| **Critérios de aceitação**                                          |
| :----------------------------------------------------------------- |
| Mensagens de "campo obrigatório" devem ser exibidas em cada campo. |

#### Caso de Teste 03: Cadastrar sem fornecer a informação de Nome.

| ID       | Descrição                                   |
| :------- | :------------------------------------------ |
| C02-CT04 | Tentativa de cadastro sem fornecer o nome.  |

| **Pré-condições**                               |
| :---------------------------------------------- |
| O campo de nome deve estar vazio.               |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que estamos na página de cadastro da BugBank              |
| **E** deixamos o campo "Nome" em branco                            |
| **E** preenchemos os demais campos corretamente                    |
| **QUANDO** clicarmos no botão "Cadastrar"                          |
| **ENTÃO** uma mensagem de erro deve ser exibida no campo Nome      |

| **Critérios de aceitação**                                  |
| :----------------------------------------------------------- |
| A mensagem "Nome é obrigatório" deve ser exibida.            |

#### Caso de Teste 04: Cadastrar sem fornecer a informação de Email.

| ID       | Descrição                                    |
| :------- | :------------------------------------------- |
| C02-CT05 | Tentativa de cadastro sem fornecer o e-mail. |

| **Pré-condições**                              |
| :--------------------------------------------- |
| O campo de e-mail deve estar vazio.            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de cadastro da BugBank            |
| **E** deixamos o campo "Email" em branco                         |
| **E** preenchemos os demais campos corretamente                  |
| **QUANDO** clicarmos no botão "Cadastrar"                        |
| **ENTÃO** uma mensagem de erro deve ser exibida no campo Email   |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| A mensagem "E-mail é obrigatório" deve ser exibida.     |

#### Caso de Teste 05: Cadastrar sem fornecer a informação de Senha.

| ID       | Descrição                                    |
| :------- | :------------------------------------------- |
| C02-CT06 | Tentativa de cadastro sem fornecer a senha.  |

| **Pré-condições**                              |
| :--------------------------------------------- |
| O campo de senha deve estar vazio.             |

| **Passos**                                                         |
| :----------------------------------------------------------------- |
| **DADO** que estamos na página de cadastro da BugBank             |
| **E** deixamos o campo "Senha" em branco                          |
| **E** preenchemos os demais campos corretamente                   |
| **QUANDO** clicarmos no botão "Cadastrar"                         |
| **ENTÃO** uma mensagem de erro deve ser exibida no campo Senha    |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| A mensagem "Senha é obrigatória" deve ser exibida.      |

#### Caso de Teste 09: Cadastrar novamente o mesmo usuário.

| ID       | Descrição                                     |
| :------- | :-------------------------------------------- |
| C02-CT09 | Tentativa de cadastrar um usuário já existente.|

| **Pré-condições**                                               |
| :-------------------------------------------------------------- |
| O usuário já deve estar cadastrado no sistema com o mesmo e-mail.|

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que estamos na página de cadastro da BugBank                      |
| **E** preenchemos todos os campos com os mesmos dados já cadastrados       |
| **QUANDO** clicarmos no botão "Cadastrar"                                  |
| **ENTÃO** uma mensagem de erro deve ser exibida na tela                    |

| **Critérios de aceitação**                                     |
| :------------------------------------------------------------- |
| A mensagem "E-mail já cadastrado" deve ser exibida.            |

## ⚙️ Cenário 03: Gerenciamento de Conta

#### Caso de Teste 01: Redefinir senha com sucesso e realizar login com nova senha.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C03-CT01 | Usuário redefine a senha com sucesso e realiza login.      |

| **Pré-condições**                                                      |
| :--------------------------------------------------------------------- |
| O usuário deve estar cadastrado e ter acesso ao e-mail vinculado.     |

| **Passos**                                                                               |
| :---------------------------------------------------------------------------------------- |
| **DADO** que estamos na página de login da BugBank                                      |
| **E** clicamos em "Esqueci minha senha"                                                 |
| **E** preenchemos o e-mail "usuario@email.com"                                          |
| **QUANDO** recebermos o e-mail e redefinirmos a senha para "novaSenha123"               |
| **E** realizarmos login com a nova senha                                                |
| **ENTÃO** o login deve ser realizado com sucesso                                         |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A senha deve ser alterada e o login com a nova senha deve funcionar. |

#### Caso de Teste 02: Logout de usuário.

| ID       | Descrição                                  |
| :------- | :----------------------------------------- |
| C03-CT02 | Usuário logado realiza logout com sucesso. |

| **Pré-condições**                                   |
| :-------------------------------------------------- |
| O usuário deve estar autenticado no sistema.        |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na área logada da BugBank                   |
| **QUANDO** clicarmos em "Sign out"                               |
| **ENTÃO** o usuário deve ser deslogado e redirecionado à tela de login |

| **Critérios de aceitação**                                |
| :-------------------------------------------------------- |
| O usuário não deve ter mais acesso às áreas restritas.    |

#### Caso de Teste 03: Edição de informações pessoais.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C03-CT03 | Usuário edita informações pessoais com sucesso.               |

| **Pré-condições**                                                 |
| :---------------------------------------------------------------- |
| O usuário deve estar autenticado e saber sua senha atual.         |

| **Passos**                                                                             |
| :------------------------------------------------------------------------------------- |
| **DADO** que estamos na página de perfil do usuário autenticado                       |
| **E** alteramos o nome para "Carlos A. Souza"                                         |
| **E** informamos a senha atual "senha123" para confirmar a alteração                   |
| **QUANDO** clicarmos em "Salvar"                                                      |
| **ENTÃO** os dados devem ser atualizados com sucesso                                  |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| As novas informações devem ser salvas e exibidas.       |

#### Caso de Teste 04: Adição de novo endereço.

| ID       | Descrição                                               |
| :------- | :------------------------------------------------------ |
| C03-CT04 | Usuário adiciona novo endereço de entrega/faturamento. |

| **Pré-condições**                                |
| :----------------------------------------------- |
| O usuário deve estar autenticado no sistema.     |

| **Passos**                                                                 |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na seção de endereços da conta do usuário           |
| **E** clicamos em "Adicionar novo endereço"                              |
| **E** preenchemos corretamente os campos (rua, número, cidade, CEP etc.) |
| **QUANDO** clicarmos em "Salvar endereço"                                |
| **ENTÃO** o novo endereço deve ser salvo e listado                       |

| **Critérios de aceitação**                                       |
| :---------------------------------------------------------------- |
| O novo endereço deve ser salvo com sucesso e listado na conta.   |

#### Caso de Teste 05: Edição de endereço existente.

| ID       | Descrição                                     |
| :------- | :-------------------------------------------- |
| C03-CT05 | Usuário edita um endereço existente com sucesso. |

| **Pré-condições**                                        |
| :------------------------------------------------------- |
| O usuário deve estar autenticado e ter pelo menos um endereço salvo. |

| **Passos**                                                                  |
| :--------------------------------------------------------------------------- |
| **DADO** que estamos na lista de endereços salvos do usuário                |
| **E** clicamos em "Editar" no endereço desejado                             |
| **E** alteramos o número do endereço de "100" para "150"                    |
| **QUANDO** clicarmos em "Salvar alterações"                                 |
| **ENTÃO** o endereço deve ser atualizado na lista                          |

| **Critérios de aceitação**                                   |
| :------------------------------------------------------------ |
| O endereço deve refletir as novas informações inseridas.      |

#### Caso de Teste 06: Remoção de endereço existente.

| ID       | Descrição                                       |
| :------- | :---------------------------------------------- |
| C03-CT06 | Usuário remove um endereço existente com sucesso. |

| **Pré-condições**                                        |
| :------------------------------------------------------- |
| O usuário deve estar autenticado e possuir endereço salvo. |

| **Passos**                                                                  |
| :--------------------------------------------------------------------------- |
| **DADO** que estamos na lista de endereços salvos do usuário                |
| **E** clicamos em "Remover" no endereço desejado                            |
| **E** confirmamos a exclusão do endereço                                    |
| **QUANDO** o sistema processar a remoção                                    |
| **ENTÃO** o endereço não deve mais aparecer na lista                       |

| **Critérios de aceitação**                                       |
| :---------------------------------------------------------------- |
| O endereço removido deve ser excluído com sucesso da conta.       |

#### Caso de Teste 07: Visualização de histórico de pedidos.

| ID       | Descrição                                          |
| :------- | :------------------------------------------------- |
| C03-CT07 | Usuário visualiza a lista de seus pedidos anteriores. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e ter ao menos um pedido realizado. |

| **Passos**                                                               |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na área logada da conta do usuário                  |
| **E** acessamos a aba "Histórico de pedidos"                            |
| **QUANDO** a página carregar                                              |
| **ENTÃO** deve ser exibida uma lista com os pedidos anteriores do usuário |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Todos os pedidos anteriores devem estar listados corretamente. |

#### Caso de Teste 08: Visualização de detalhes de um pedido.

| ID       | Descrição                                             |
| :------- | :---------------------------------------------------- |
| C03-CT08 | Usuário visualiza os detalhes de um pedido específico. |

| **Pré-condições**                                                    |
| :------------------------------------------------------------------- |
| O usuário deve estar autenticado e possuir pelo menos um pedido listado. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na página de "Histórico de pedidos" do usuário      |
| **E** clicamos no botão "Ver detalhes" de um dos pedidos listados         |
| **QUANDO** a nova página/carregamento de detalhes for exibida             |
| **ENTÃO** devem ser apresentados os dados completos do pedido (itens, preço, status, etc.) |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Todos os dados do pedido devem ser exibidos corretamente.       |

