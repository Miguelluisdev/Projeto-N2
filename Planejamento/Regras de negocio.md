# 📘 Regras de Negócio (RN) - automationpractice.com.br

As Regras de Negócio (RN) ditam as **políticas**, **restrições** e **lógicas operacionais** que o sistema deve seguir. Elas são fundamentais para validar o comportamento esperado do sistema além da interface, garantindo a aderência às expectativas do negócio.

---

## 🧑‍💼 RN - Usuário e Conta

- **RN01**: Cada conta de usuário deve ser associada a um endereço de email único no sistema.
- **RN02**: Um endereço de email deve ter um formato válido (contendo "@" e um domínio) para ser aceito no cadastro ou login.
- **RN03**: (Se aplicável) As senhas de usuário devem atender a critérios mínimos de complexidade definidos (ex: comprimento mínimo, caracteres especiais, etc.).
- **RN04**: O login no sistema só é permitido mediante a combinação correta de um email registrado e sua senha correspondente.
- **RN05**: Um usuário logado tem permissão para visualizar e gerenciar suas informações pessoais, endereços e histórico de pedidos na área "Minha Conta".
- **RN06**: A alteração de informações pessoais sensíveis (como senha, talvez nome/email) pode exigir a confirmação da senha atual do usuário.
- **RN07**: O acesso à área "Minha Conta" e ao processo de checkout (após o carrinho inicial) é restrito a usuários autenticados (logados).
- **RN08**: Um usuário pode ter múltiplos endereços cadastrados (faturamento e entrega).
- **RN09**: Pelo menos um endereço de entrega e um de faturamento devem ser definidos para concluir um pedido.
- **RN10**: O sistema deve permitir a recuperação de senha associada a um email cadastrado, através de um processo de verificação por email.

---

## 🛒 RN - Produto e Catálogo

- **RN11**: Cada produto pertence a pelo menos uma categoria principal exibida no menu.
- **RN12**: As páginas de listagem de produtos (PLP) devem exibir apenas os produtos associados à categoria ou resultado de busca/filtro correspondente.
- **RN13**: A lista de produtos em uma PLP pode ser ordenada por critérios pré-definidos (Preço, Nome, Relevância, Estoque, etc.).
- **RN14**: A lista de produtos em uma PLP pode ser filtrada por atributos pré-definidos do produto (Tamanho, Cor, Composição, Preço, etc.).
- **RN15**: Produtos podem ter variações (como Tamanho e Cor).
- **RN16**: Se um produto possui variações obrigatórias, o usuário deve selecionar uma opção válida para cada variação antes de poder adicioná-lo ao carrinho a partir da PDP.
- **RN17**: O preço, a imagem principal e a disponibilidade de um produto podem variar de acordo com a variação selecionada (Tamanho/Cor).
- **RN18**: A disponibilidade de estoque (em estoque / fora de estoque) deve ser claramente indicada para cada produto ou variação selecionável na PDP.
- **RN19**: Apenas produtos (ou variações específicas) que estão "Em estoque" podem ser adicionados ao carrinho de compras.
- **RN20**: A quantidade de um produto a ser adicionada ao carrinho deve ser um número inteiro positivo (maior que zero).
- **RN21**: (Implícita, comum) A quantidade adicionada ao carrinho pode ser limitada pela quantidade disponível em estoque para aquele produto/variação.
- **RN22**: (Se aplicável) Usuários logados podem adicionar produtos a uma Lista de Desejos (Wishlist) pessoal.
- **RN23**: (Se aplicável) Produtos podem ser selecionados para uma ferramenta de comparação, que exibirá atributos chave lado a lado.

---

## 💳 RN - Carrinho de Compras e Checkout

- **RN24**: O carrinho de compras deve calcular o subtotal de cada item (preço unitário * quantidade).
- **RN25**: O carrinho de compras deve calcular o valor total dos produtos (soma dos subtotais dos itens).
- **RN26**: O carrinho de compras deve exibir o custo de frete (uma vez calculado/selecionado no checkout) e impostos (se aplicáveis).
- **RN27**: O carrinho de compras deve exibir o valor TOTAL final do pedido (produtos + frete + impostos - descontos).
- **RN28**: A quantidade de um item no carrinho pode ser alterada pelo usuário, o que deve automaticamente recalcular os totais.
- **RN29**: Itens podem ser removidos do carrinho pelo usuário, o que deve automaticamente recalcular os totais.
- **RN30**: (Se aplicável) Cupons de desconto válidos podem ser aplicados no carrinho ou checkout.
- **RN31**: O sistema deve validar a existência, validade (datas, limites de uso) e aplicabilidade de um cupom antes de aplicar o desconto.
- **RN32**: A aplicação de um cupom deve reduzir o valor TOTAL do pedido.
- **RN33**: (Implícita, comum) Pode haver um limite de quantos cupons podem ser usados por pedido (geralmente apenas um).
- **RN34**: O processo de checkout só pode ser iniciado se houver pelo menos um item no carrinho.
- **RN35**: O cálculo do custo de frete é baseado no endereço de entrega selecionado e na opção de transportadora escolhida.
- **RN36**: O usuário deve selecionar explicitamente uma opção de frete disponível para prosseguir no checkout.
- **RN37**: O usuário deve aceitar os Termos de Serviço do site para prosseguir do estágio de Frete para Pagamento no checkout.
- **RN38**: O usuário deve selecionar explicitamente um dos métodos de pagamento disponíveis (ex: Transferência Bancária, Cheque) para concluir o pedido.
- **RN39**: Um pedido só é considerado confirmado e registrado no sistema após a ação explícita do usuário na última etapa do checkout ("Confirmar meu pedido").

---

## ⚙️ RN - Gerais e Validação

- **RN40**: Campos marcados como obrigatórios em qualquer formulário do site devem ser preenchidos pelo usuário para que o formulário seja submetido com sucesso.
- **RN41**: O envio do formulário de contato requer um Assunto selecionado, um Email válido e uma Mensagem preenchida.
- **RN42**: As mensagens enviadas pelo formulário de contato devem gerar uma notificação interna para a equipe responsável.
- **RN43**: A inscrição na newsletter requer um endereço de email válido e único na lista de assinantes.
- **RN44**: Todo tráfego em páginas sensíveis (login, cadastro, checkout, minha conta) deve ocorrer sobre conexão segura (HTTPS).

---

Estas regras de negócio definem as restrições e lógicas fundamentais que governam o funcionamento do e-commerce *automationpractice.com.br*, servindo como guia tanto para o desenvolvimento quanto para a criação de cenários de teste que verifiquem a conformidade do sistema com as expectativas do negócio.
