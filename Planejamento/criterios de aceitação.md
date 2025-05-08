# 📘 Critérios de Aceite - automationpractice.com.br

## RF01: Autenticação e Gerenciamento de Conta

### RF01.1: Registro de Novo Usuário

**Deve Conter / Deve Fazer:**
- Um formulário de registro acessível.
- Campos para informações pessoais obrigatórias (nome, email, senha, etc.).
- Validação do formato do campo de email.
- Verificação se o email informado já existe no sistema.
- Validação de complexidade de senha (se regras forem definidas).
- Mensagens de erro claras e específicas exibidas próximas aos campos com dados inválidos ou faltantes.
- Criação da conta de usuário no banco de dados após submissão com dados válidos e únicos.
- Redirecionamento do usuário para a página "Minha Conta" após registro bem-sucedido.
- Exibição do nome do usuário logado no cabeçalho do site após registro bem-sucedido.

**Não Deve Conter / Não Deve Fazer:**
- Permitir o registro com um formato de email inválido.
- Permitir o registro com um email que já está cadastrado.
- Permitir o registro se as regras de complexidade de senha (se houver) não forem atendidas.
- Permitir a submissão do formulário se campos obrigatórios estiverem vazios.
- Exibir mensagens de erro genéricas ou confusas.
- Falhar em criar a conta se todos os dados válidos foram fornecidos.
- Manter o usuário na página de registro após um registro bem-sucedido.

### RF01.2: Login de Usuário Existente

**Deve Conter / Deve Fazer:**
- Um formulário de login com campos para email e senha.
- Validação das credenciais (email e senha) contra os dados registrados.
- Mensagem de erro clara em caso de credenciais inválidas (ex: "Authentication failed.").
- Mensagens de erro específicas se o campo email ou senha estiverem vazios na submissão.
- Redirecionamento do usuário para a página "Minha Conta" após login bem-sucedido.
- Exibição do nome do usuário logado no cabeçalho do site após login bem-sucedido.

**Não Deve Conter / Não Deve Fazer:**
- Permitir o login com email correto mas senha incorreta (ou vice-versa).
- Permitir o login com campos de email ou senha vazios.
- Exibir informações sensíveis na mensagem de erro (ex: "Senha incorreta", diferenciando do erro de email inexistente).
- Manter o usuário na página de login após um login bem-sucedido.

### RF01.3: Recuperação de Senha

**Deve Conter / Deve Fazer:**
- Um link "Esqueceu sua senha?" na página de login.
- Uma página/formulário para solicitar a recuperação, pedindo o email do usuário.
- Validação se o email fornecido está cadastrado.
- Mensagem de confirmação após solicitação bem-sucedida, informando que um email foi enviado.
- Envio de um email real para o endereço fornecido (se cadastrado) contendo um link seguro para redefinição.
- Mensagem de erro se o email fornecido não estiver cadastrado.
- Uma página segura (acessada via link do email) para definir a nova senha (com campo de confirmação).
- Atualização da senha do usuário no sistema após confirmação bem-sucedida.
- Mensagem de sucesso após a senha ser redefinida.

**Não Deve Conter / Não Deve Fazer:**
- Enviar email de recuperação para um endereço não cadastrado.
- Expor senhas ou links de redefinição inseguros.
- Permitir a redefinição sem confirmação de senha.
- Falhar em atualizar a senha no sistema após processo bem-sucedido.

### RF01.4: Logout de Usuário

**Deve Conter / Deve Fazer:**
- Um link/botão "Sign out" visível para usuários logados (geralmente no cabeçalho).
- Encerramento da sessão do usuário ao clicar em "Sign out".
- Redirecionamento para uma página pública (login ou homepage) após logout.
- Remoção do nome do usuário do cabeçalho e exibição do link "Sign in".

**Não Deve Conter / Não Deve Fazer:**
- Manter o usuário logado após clicar em "Sign out".
- Permitir acesso a páginas restritas (como "Minha Conta") após o logout (deve redirecionar para login).

### RF01.5: Gerenciamento da Conta

**Deve Conter / Deve Fazer:**
- Acesso à página "Minha Conta" somente para usuários logados.
- Seção para visualizar e editar informações pessoais (nome, email, etc.).
- Exigência da senha atual para confirmar alterações nas informações pessoais.
- Seção para gerenciar endereços (visualizar, adicionar, editar, remover).
- Seção para visualizar o histórico de pedidos (ID, data, total, status).
- Link para visualizar detalhes completos de cada pedido.
- Seção para gerenciar listas de desejos (se aplicável).
- Mensagens de sucesso após salvar alterações.
- Mensagens de erro claras se a validação falhar.

**Não Deve Conter / Não Deve Fazer:**
- Permitir acesso à "Minha Conta" sem estar logado.
- Permitir a edição de informações críticas sem validação adequada.
- Excluir endereços sem confirmação.
- Exibir dados incorretos no histórico ou pedidos.
- Salvar alterações com dados inválidos.
## RF02: Navegação e Estrutura do Site

**Deve Conter / Deve Fazer:**
- Menu principal claro com categorias de produtos (Mulheres, Vestidos, Camisetas).
- Links do menu principal direcionando corretamente para as PLPs correspondentes.
- Logo do site no cabeçalho sendo um link funcional para a Homepage.
- Links funcionais no cabeçalho para "Contato", "Login/Logout", "Carrinho".
- Links informativos funcionais no rodapé (Sobre Nós, Termos, Política de Privacidade).
- Links relacionados à conta no rodapé (Minha Conta, Meus Pedidos) direcionando para login se não estiver logado.
- Breadcrumbs exibidos em páginas internas (PLP, PDP) mostrando o caminho de navegação.
- Links nos breadcrumbs funcionando corretamente.
- Todos os links internos (banners, promoções) direcionando para os locais corretos.

**Não Deve Conter / Não Deve Fazer:**
- Links quebrados (erro 404) no menu, cabeçalho, rodapé, breadcrumbs ou conteúdo.
- Redirecionamentos incorretos a partir dos links de navegação.
- Ausência de breadcrumbs em páginas internas profundas.
- Logo não clicável ou levando para página errada.

---

## RF03: Pesquisa de Produtos

**Deve Conter / Deve Fazer:**
- Um campo de busca visível (geralmente no cabeçalho).
- Funcionalidade de busca que retorna produtos baseados em palavras-chave.
- Uma página de resultados de pesquisa exibindo os produtos encontrados.
- Exibição do termo pesquisado na página de resultados.
- Mensagem clara indicando "Nenhum resultado encontrado" quando a busca não retorna produtos.
- Opções de ordenação e filtragem na página de resultados (similar a uma PLP).

**Não Deve Conter / Não Deve Fazer:**
- Falhar em retornar produtos relevantes que correspondem à palavra-chave.
- Retornar erro ou página em branco ao buscar.
- Não exibir mensagem clara quando nenhum produto é encontrado.
- Exibir resultados de busca sem o termo pesquisado ou opções de refinar.

---

## RF04: Listagem e Filtragem de Produtos (PLP)

**Deve Conter / Deve Fazer:**
- Exibição de produtos pertencentes à categoria selecionada.
- Informações essenciais por produto: imagem, nome, preço.
- Link funcional da imagem/nome do produto para a PDP correspondente.
- Paginação funcional se houver muitos produtos (links Anterior, Próxima, números de página).
- Dropdown/Controles para ordenar produtos por critérios relevantes (Preço, Nome, etc.).
- Opções de filtro por atributos relevantes (Categoria, Tamanho, Cor, etc.).
- Atualização dinâmica da lista de produtos ao aplicar/remover filtros ou mudar ordenação.
- Indicação visual dos filtros ativos.
- (Opcional) Botão "Quick View" ao passar o mouse, abrindo modal com detalhes básicos e botão Add to Cart.
- (Opcional) Botão "Add to Cart" diretamente na PLP (para produtos sem variações obrigatórias).

**Não Deve Conter / Não Deve Fazer:**
- Exibir produtos de categorias erradas.
- Links quebrados para as PDPs.
- Paginação que não funciona ou leva para páginas erradas.
- Ordenação que não ordena corretamente os produtos.
- Filtros que não atualizam a lista ou exibem produtos incorretos.
- Falha ao adicionar produto ao carrinho via "Quick View" ou botão direto na PLP.

---

## RF05: Detalhes do Produto (PDP)

**Deve Conter / Deve Fazer:**
- Exibição completa das informações do produto (nome, descrição, preço, SKU, imagens, etc.).
- Galeria de imagens com thumbnails clicáveis para trocar a imagem principal (se houver múltiplas imagens).
- Controles (dropdown, swatches) para seleção de variações (Tamanho, Cor), se aplicável.
- Campo para definir a quantidade desejada (com valor padrão 1).
- Botão claro "Adicionar ao Carrinho".
- Feedback visual claro após adicionar ao carrinho (ex: popup de confirmação com opções).
- Incremento correto do contador do carrinho no cabeçalho após adicionar.
- Indicação clara de disponibilidade ("Em estoque" ou "Fora de estoque").
- (Opcional) Botões "Adicionar à Wishlist", compartilhamento social, avaliações, produtos relacionados.

**Não Deve Conter / Não Deve Fazer:**
- Informações de produto incorretas ou ausentes.
- Imagens que não carregam ou não correspondem ao produto/variação.
- Permitir adicionar ao carrinho sem selecionar variações obrigatórias.
- Permitir adicionar ao carrinho quantidade inválida (0, negativa, maior que estoque se validado).
- Botão "Adicionar ao Carrinho" desabilitado para produto em estoque ou habilitado para produto fora de estoque (para a variação selecionada).
- Falha em adicionar o produto ao carrinho após clique no botão com dados válidos.
- Não fornecer feedback ao usuário após adicionar ao carrinho.

---

## RF06: Carrinho de Compras

**Deve Conter / Deve Fazer:**
- Acesso fácil à página do carrinho (ícone/link no cabeçalho).
- Funcionalidade para alterar a quantidade de cada item.
- Recálculo automático do subtotal do item e do total do carrinho ao alterar quantidade.
- Funcionalidade para remover itens individualmente do carrinho.
- Recálculo automático do total do carrinho ao remover item.
- Exibição clara dos totais: subtotal produtos, frete (mesmo que estimado ou zero inicialmente), impostos (se houver), total geral.
- Campo para inserir código de cupom/voucher (se a funcionalidade existir).
- Validação do código do cupom e aplicação do desconto (recalculando o total) se válido.
- Mensagem de erro clara para cupons inválidos/expirados.
- Botão/Link claro para "Continuar Comprando".
- Botão claro para "Finalizar Compra" (Proceed to checkout).
- Mensagem indicando que o carrinho está vazio se não houver itens.

**Não Deve Conter / Não Deve Fazer:**
- Itens no carrinho que o usuário não adicionou ou removeu.
- Cálculos incorretos de subtotais ou total geral.
- Falha ao atualizar quantidade ou remover itens.
- Aplicar desconto de cupom inválido ou não aplicar de cupom válido.
- Botão "Finalizar Compra" habilitado se o carrinho estiver vazio.

---

## RF07: Processo de Checkout

**Deve Conter / Deve Fazer:**
- Divisão clara do processo em etapas lógicas (Resumo, Login, Endereço, Frete, Pagamento).
- Indicação visual da etapa atual.
- Se não logado, opção de login ou registro na etapa apropriada.
- Permitir selecionar/adicionar/editar endereços de faturamento e entrega.
- Opção para usar o mesmo endereço para faturamento e entrega.
- Exibição das opções de frete disponíveis com custos baseados no endereço.
- Exigência de seleção de uma opção de frete.
- Exigência de aceitação dos Termos de Serviço (checkbox).
- Exibição dos métodos de pagamento aceitos (Transferência, Cheque, etc.).
- Exigência de seleção de um método de pagamento.
- Exibição de um resumo final completo do pedido antes da confirmação.
- Um botão final claro para confirmar o pedido.
- Registro do pedido no sistema após confirmação.
- Exibição de uma página de sucesso com o número do pedido e confirmação.
- Envio de um email de confirmação do pedido para o usuário.

**Não Deve Conter / Não Deve Fazer:**
- Permitir avançar no checkout sem completar etapas obrigatórias.
- Cálculos incorretos de frete ou total final no resumo.
- Opções de frete/pagamento inválidas para o contexto.
- Permitir confirmar o pedido sem selecionar método de pagamento ou frete.
- Falhar em registrar o pedido no sistema após confirmação bem-sucedida.
- Falhar em enviar o email de confirmação.
- Expor dados sensíveis desnecessariamente.

---

## RF08: Validação de Campos de Formulário

**Deve Conter / Deve Fazer:**
- Validação de obrigatoriedade para todos os campos marcados como tal em todos os formulários.
- Validação de formato para campos específicos (Email, Telefone, CEP, etc.).
- Mensagens de erro claras, específicas e posicionadas próximas aos campos inválidos.
- Validação ocorrendo tanto no lado do cliente quanto no lado do servidor.

**Não Deve Conter / Não Deve Fazer:**
- Permitir a submissão de formulários com campos obrigatórios vazios.
- Permitir a submissão com formatos inválidos.
- Exibir mensagens de erro genéricas ou longe do campo com problema.
- Confiar apenas na validação do lado do cliente.

---

## RF09: Outras Funcionalidades

### RF09.1: Formulário de Contato

**Deve Conter / Deve Fazer:**
- Um formulário na página de Contato com campos (Assunto, Email, Mensagem).
- Validação dos campos obrigatórios.
- Validação do formato do email.
- Mensagem de sucesso clara após envio bem-sucedido.
- Envio real da mensagem para o destinatário interno.

**Não Deve Conter / Não Deve Fazer:**
- Permitir envio com campos obrigatórios vazios ou email inválido.
- Não exibir confirmação de sucesso após envio válido.
- Falhar em entregar a mensagem internamente.

---

### RF09.2: Inscrição em Newsletter

**Deve Conter / Deve Fazer:**
- Campo para inserir email (geralmente no rodapé).
- Validação do formato do email inserido.
- Mensagem de sucesso clara após inscrição bem-sucedida.
- Mensagem clara se o email já estiver inscrito.
- Adição do email à lista de newsletter no backend (se aplicável).

**Não Deve Conter / Não Deve Fazer:**
- Permitir inscrição com email inválido.
- Exibir mensagem de erro quando a inscrição é bem-sucedida (ou vice-versa).
- Falhar em registrar o email na lista.

---

### RF09.3: Comparação de Produtos (Se existir)

**Deve Conter / Deve Fazer:**
- Botão "Adicionar à Comparação" nas PLPs e/ou PDPs.
- Feedback visual que o produto foi adicionado.
- Link/Botão para acessar a página de comparação.
- Página de comparação exibindo produtos lado a lado.
- Exibição de atributos comparáveis.
- Botão para remover produtos da comparação.
- Botão "Adicionar ao Carrinho" por produto.

**Não Deve Conter / Não Deve Fazer:**
- Falha ao adicionar/remover produtos da lista.
- Contador de comparação incorreto.
- Página de comparação com falhas ou links quebrados.
