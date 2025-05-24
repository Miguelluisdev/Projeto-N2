# 🧪 Teste Exploratórios - E-commerce de Eletrônicos

## 🔗 URL Testada
[https://automationpratice.com.br/](https://automationpratice.com.br/)

## 🗓️ Data do Teste
24/05/2025

## 👤 Testador
Miguel Luis

## 🎯 Objetivo
Explorar livremente o sistema para identificar comportamentos inesperados, bugs, entender o fluxo do sistema e mapear as principais funcionalidades para posterior documentação e elaboração de casos de teste.

> **Nota:** O teste exploratório é fundamental em contextos onde não há documentação formal do sistema. Ele ajuda a compreender a lógica de funcionamento, mapear áreas críticas e detectar problemas de UI/UX, segurança e inconsistências de fluxo.

---

## 🔍 Áreas Navegadas

- Página Inicial (Home)
- Sessão de Produtos em Destaque (Top Product e Weekly Deal)
- Página de Produto Único
- Sessão Shop (Catálogo de Produtos)
- Carrinho de Compras
- Checkout
- Footer e Links de Redes Sociais

---

## ✅ Funcionalidades Identificadas

| Funcionalidade             | Descrição Rápida                                                              |
|-----------------------------|-------------------------------------------------------------------------------|
| Top Product                 | Sessão destacada de produtos em oferta.                                       |
| Weekly Deal Product         | Ofertas semanais destacadas na página inicial.                                |
| Sessão Shop                 | Listagem completa de produtos disponíveis.                                    |
| Página de Produto           | Página dedicada com detalhes de cada produto (cor, tamanho, preço, etc).      |
| Carrinho de Compras         | Adicionar/remover produtos ao carrinho e ver detalhes da compra.              |
| Checkout                    | Processo de finalização de compra, incluindo login e confirmação de pedido.   |
| Footer                      | Links para redes sociais (Instagram, Facebook, etc.).                         |

---

## 🐛 Erros e Bugs Encontrados

| Área                            | Descrição Detalhada                                                                                                                                                      |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessão Home                    | Erros de digitação, imagens incorretas e nomes diferentes; mistura de português e inglês.                                                                                 |
| Instagram - Home               | Links para Instagram não funcionam.                                                                                                                                       |
| Footer (todas as páginas)      | Ícones das redes sociais não funcionam, não redirecionam corretamente.                                                                                                   |
| Sessão Shop                    | Bugs em imagens e textos; botão "Add to Cart" deveria ter outra cor.                                                                                                      |
| Modal do Produto               | Não funciona ao clicar na cor; ao tentar adicionar mais de um produto, surge mensagem de erro.                                                                             |
| Página de Produto Único        | Tamanho do produto não altera; nome do produto incorreto; não consigo adicionar review; ao clicar na cor, muda a imagem de outro produto.                                  |
| Checkout                       | Não deveria permitir acesso sem login (erro crítico de segurança); preço exibido está errado; outros dados sensíveis aparecem indevidamente.                               |
| Crash de Navegador             | Navegador travou em uma tela de compra; na mesma tela ocorre bug da cor, tamanho e imagens dos itens.                                                                      |
| Segurança e Acesso             | Falta de segurança na navegação: telas que não deveriam ser acessadas (ex.: dashboard) estão disponíveis; outros erros graves de segurança detectados.                     |
| Pesquisa Global                | Input de pesquisa não funciona corretamente, retorna qualquer coisa ou resultados irrelevantes.                                                                            |
| Formulários de Cadastro/Login  | Mensagens de erro claras em alguns casos, mas em outros os formulários falham sem aviso; erros de UX ao preencher dados.                                                   |
| UI/UX Geral                    | Muitas falhas de consistência, navegação confusa em alguns fluxos, cores de botões inconsistentes, e erros de digitação.                                                    |

---

## ⚠️ Falhas Críticas de Segurança

- Acesso ao checkout sem login obrigatório.
- Dados sensíveis (como endereço e e-mail) de outros usuários visíveis.
- Falta de verificação ao adicionar ou remover itens do carrinho.
- Falta de restrição em áreas que deveriam ser protegidas (ex.: dashboard).
- Crash do navegador em situações específicas, causando perda de sessão e dados.

---

## 💡 Ideias para Testes Futuros

- Testar fluxo completo de checkout (com login obrigatório e validação de dados).
- Verificar consistência dos dados exibidos após login/logout.
- Explorar limites de campos nos formulários (como inputs de texto e campos de pesquisa).
- Testar navegação com múltiplas abas e usuários simultâneos.
- Avaliar responsividade em dispositivos móveis (celulares e tablets).
- Simular perda de conexão durante o checkout e análise de persistência de dados.

---

## 📋 Observações Gerais

- O site apresenta falhas de UX em quase todas as sessões, o que pode afetar a confiança do usuário.
- Falhas críticas de segurança podem expor dados sensíveis dos clientes, devendo ser priorizadas.
- Erros de imagens, links quebrados e navegação inconsistente afetam a credibilidade do e-commerce.
- Apesar disso, as mensagens de erro são claras em algumas áreas, mas faltam em outras (como formulários).

---

## 📌 Conclusão

O teste exploratório revelou diversas falhas graves e superficiais no sistema. Problemas de segurança e UX são prioritários e devem ser corrigidos para garantir a integridade e usabilidade do e-commerce. Recomenda-se a realização de testes formais (manuais e automatizados) para validar as correções e assegurar a confiabilidade antes de liberar para produção.

---

### 🖥️ Ambiente de Teste

- **Sistema Operacional:** Windows 11
- **Navegador:** Microsoft Edge 136.0v
- **Abordagem:** Teste exploratório e reteste

