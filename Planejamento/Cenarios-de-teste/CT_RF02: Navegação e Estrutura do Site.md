<a id="top"></a>

# Cenários e Casos de Teste RF01

**Software:** Automation-Pratice

**QA responsável:** Miguel Luis

**Data:** 8/05/2025

<a id="index"></a>

## Cenário 01: Navegação e Estrutura do Site

#### Caso de Teste 01: Deve navegar para a PLP de Mulheres pelo menu principal.

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C02-CT01 | Clicar em "Mulheres" no menu principal redireciona para a PLP de Eletronicos. |

| **Pré-condições**                          |
| :----------------------------------------- |
| O usuário deve estar na Homepage do site.  |

| **Passos**                                                         |
| :----------------------------------------------------------------- |
| **DADO** que estamos na Homepage                                    |
| **QUANDO** clicarmos em "Mulheres" no menu principal                |
| **ENTÃO** devemos ser redirecionados para a página de listagem de produtos (PLP) de Eletronicos|

| **Critérios de aceitação**                                                |
| :------------------------------------------------------------------------ |
| A PLP de Mulheres deve ser carregada corretamente com produtos visíveis.  |

#### Caso de Teste 02: Deve retornar à Homepage ao clicar no logo.

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C02-CT04 | Clicar no logo em qualquer página deve redirecionar à Homepage.     |

| **Pré-condições**                                |
| :----------------------------------------------- |
| O usuário deve estar em qualquer página do site. |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que estamos em uma página qualquer (PLP, PDP, etc.)         |
| **QUANDO** clicarmos no logo no cabeçalho                            |
| **ENTÃO** devemos ser redirecionados para a Homepage                 |

| **Critérios de aceitação**                          |
| :-------------------------------------------------- |
| A Homepage deve ser carregada corretamente.         |

#### Caso de Teste 05: Deve acessar a página de Contato pelo cabeçalho.

| ID       | Descrição                                                       |
| :------- | :-------------------------------------------------------------- |
| C02-CT05 | Clicar em "Contato" deve redirecionar para a página de contato. |

| **Pré-condições**                          |
| :----------------------------------------- |
| O link de "Contato" deve estar visível no cabeçalho. |

| **Passos**                                                       |
| :--------------------------------------------------------------- |
| **DADO** que estamos na Homepage                                 |
| **QUANDO** clicarmos em "Contato" no cabeçalho                   |
| **ENTÃO** devemos ser redirecionados para a página de contato    |

| **Critérios de aceitação**                          |
| :-------------------------------------------------- |
| A página de contato deve ser carregada corretamente. |

#### Caso de Teste 06: Deve realizar o Login (deslogado) ou Logout (logado) corretamente.

| ID       | Descrição                                                                   |
| :------- | :-------------------------------------------------------------------------- |
| C02-CT06 | Clicar em "Login" ou "Logout" deve redirecionar para autenticação ou deslogar. |

| **Pré-condições**                                                  |
| :----------------------------------------------------------------- |
| O botão "Login" (deslogado) ou "Logout" (logado) deve estar visível. |

| **Passos**                                                                        |
| :--------------------------------------------------------------------------------- |
| **DADO** que estamos na Homepage                                                  |
| **QUANDO** clicarmos em "Login" estando deslogado                                 |
| **ENTÃO** devemos ser redirecionados para a página de autenticação                |
| **E** quando estivermos logados e clicarmos em "Logout"                           |
| **ENTÃO** o usuário deve ser deslogado e redirecionado para a Homepage            |

| **Critérios de aceitação**                                                    |
| :----------------------------------------------------------------------------- |
| Login deve levar à tela de autenticação. Logout deve encerrar sessão e voltar à Homepage. |

#### Caso de Teste 07: Deve acessar a página do Carrinho pelo cabeçalho.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C02-CT07 | Clicar em "Carrinho" redireciona o usuário para a página do carrinho. |

| **Pré-condições**                         |
| :---------------------------------------- |
| O botão "Carrinho" deve estar visível no cabeçalho. |

| **Passos**                                                    |
| :------------------------------------------------------------ |
| **DADO** que estamos na Homepage                              |
| **QUANDO** clicarmos em "Carrinho" no cabeçalho               |
| **ENTÃO** devemos ser redirecionados para a página do carrinho |

| **Critérios de aceitação**                          |
| :-------------------------------------------------- |
| A página do carrinho deve ser exibida corretamente. |

#### Caso de Teste 08: Deve acessar os links informativos no rodapé corretamente

| ID       | Descrição                                                                |
| :------- | :----------------------------------------------------------------------- |
| C02-CT08 | Clicar nos links "Sobre Nós" e "Termos" no rodapé redireciona corretamente. |

| **Pré-condições**                              |
| :--------------------------------------------- |
| Os links devem estar visíveis no rodapé.       |

| **Passos**                                                               |
| :------------------------------------------------------------------------ |
| **DADO** que estamos em qualquer página                                  |
| **QUANDO** clicarmos em "Sobre Nós" ou "Termos" no rodapé                |
| **ENTÃO** devemos ser redirecionados para a respectiva página de conteúdo |

| **Critérios de aceitação**                                |
| :-------------------------------------------------------- |
| As páginas devem ser carregadas com o conteúdo esperado.  |

#### Caso de Teste 09: Deve acessar “Meus Pedidos” com comportamento correto logado/deslogado

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C02-CT09 | Clicar em "Meus Pedidos" leva para histórico (logado) ou login (deslogado). |

| **Pré-condições**                                         |
| :-------------------------------------------------------- |
| O link "Meus Pedidos" deve estar visível no rodapé.       |

| **Passos**                                                                   |
| :--------------------------------------------------------------------------- |
| **DADO** que estamos deslogados                                              |
| **QUANDO** clicarmos em "Meus Pedidos"                                      |
| **ENTÃO** devemos ser redirecionados para a página de login                 |
| **E** quando estivermos logados e clicarmos em "Meus Pedidos"               |
| **ENTÃO** devemos ver o histórico de pedidos                                |

| **Critérios de aceitação**                                                       |
| :-------------------------------------------------------------------------------- |
| Usuário deslogado deve ser levado ao login. Usuário logado deve ver seus pedidos. |

#### Caso de Teste 11: Deve acessar a página correta ao clicar em banner promocional.

| ID       | Descrição                                                                      |
| :------- | :----------------------------------------------------------------------------- |
| C02-CT11 | Clicar em um banner promocional leva à página correta da promoção.             |

| **Pré-condições**                                       |
| :------------------------------------------------------ |
| Deve haver um banner promocional visível na Homepage.   |

| **Passos**                                                              |
| :---------------------------------------------------------------------- |
| **DADO** que estamos na Homepage                                        |
| **QUANDO** clicarmos no banner promocional de "30% OFF em Camisetas"   |
| **ENTÃO** devemos ser redirecionados para a PLP de Camisetas em promoção |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------- |
| O link deve levar exatamente à página relacionada à promoção exibida. |

#### Caso de Teste 12: Deve validar que todos os links clicáveis não estão quebrados

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C02-CT12 | Verificar se todos os links clicáveis não estão quebrados.     |

| **Pré-condições**                           |
| :------------------------------------------ |
| Todos os links do site devem estar acessíveis. |

| **Passos**                                                      |
| :-------------------------------------------------------------- |
| **DADO** que percorremos todas as páginas com links (menu, rodapé, banners) |
| **QUANDO** clicarmos em todos os links visíveis                           |
| **ENTÃO** todos devem levar a uma página válida, sem erro 404             |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| Nenhum link deve retornar erro (404, 500, redirecionamento incorreto). |
