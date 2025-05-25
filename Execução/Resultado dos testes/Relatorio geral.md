# 📝 Relatório Geral de Testes Manuais

## 🔗 URL Testada
https://qazando-shop.com

## 🗓️ Data dos Testes
24/05/2025

## 👤 Testador
Miguel Luis

## 💻 Ambiente de Testes

| Item                | Detalhes                                 |
|----------------------|------------------------------------------|
| Sistema Operacional  | Windows 11                               |
| Navegador            | Microsoft Edge 136.0v                    |
| Tipo de Teste        | Exploratório e Casos de Teste Manuais    |

---

## ✅ Tabela Resumo de Casos de Teste

| Cenário                                  | Total de Testes | Passaram | Falharam | Não Testados |
|-------------------------------------------|-----------------|----------|----------|---------------|
| Navegação e Estrutura do Site            | 11              | 9        | 2        | 0             |
| Pesquisa de Produtos                     | 5               | 1        | 4        | 0             |
| Listagem de Produtos                     | 7               | 4        | 3        | 0             |
| Detalhes do Produto                      | 11              | 4        | 7        | 0             |
| Visualização de Itens no Carrinho        | 11              | 8        | 1        | 2             |
| Checkout Completo (Usuário Logado)       | 4               | 2        | 2        | 0             |
| Validações no Checkout                   | 5               | 3        | 0        | 2             |
| Acesso Restrito e Confirmação Final      | 2               | 1        | 1        | 0             |
| Formulário de Contato                    | 3               | 2        | 1        | 0             |
| Newsletter e Comparação                  | 7               | 5        | 2        | 1             |
| Submissão de Formulários Gerais          | 5               | 4        | 1        | 0             |

---

## ⚠️ Principais Falhas Críticas Encontradas

| Cenário                      | Descrição                                                                                     | Severidade    |
|------------------------------|------------------------------------------------------------------------------------------------|----------------|
| Navegação e Estrutura        | Permite acesso direto a páginas internas via URL sem autenticação                             | Alta           |
| Pesquisa de Produtos         | Busca não retorna resultados relevantes e filtros estão invertidos                            | Alta           |
| Listagem de Produtos         | Ordenação de produtos está invertida e produtos fora de estoque podem ser adicionados ao carrinho | Alta         |
| Detalhes do Produto          | Falha grave ao alterar variações e falta de verificação de estoque                            | Alta           |
| Checkout Completo            | Usuário deslogado consegue concluir checkout; não permite adicionar novo endereço             | Alta           |
| Validação de Formulários     | Falta de validação para telefone e CEP                                                        | Média          |
| Página de Comparação         | Acesso difícil e apenas via URL                                                               | Média          |

---

## 🔍 Resumo de Falhas Identificadas

- 🔴 **Erro de segurança**: acesso a páginas internas e checkout sem login.
- 🔴 Falhas na ordenação e filtros (inversão high to low e low to high).
- 🔴 Produtos fora de estoque ainda podem ser adicionados ao carrinho.
- 🔴 Falhas em campos de validação de formulários (telefone/CEP).
- 🟡 Falta de acesso fácil à página de comparação de produtos.

---

## 🟢 Funcionalidades que Funcionaram Corretamente

✅ Navegação geral (home, PLP, carrinho).  
✅ Visualização rápida (Quick View).  
✅ Cadastro e envio de formulários (quando os campos são válidos).  
✅ Atualização de quantidades no carrinho.  
✅ Aplicação de cupons válidos e cálculo de subtotais.

---

## 📌 Conclusão Geral

💡 **O sistema apresenta várias funcionalidades que funcionam bem em situações básicas**, porém foram identificadas **falhas críticas de segurança e inconsistências em processos importantes (filtros, checkout e estoque)**.

🔴 **Prioridade alta**: corrigir falhas de segurança (acesso via URL e checkout sem login) e validação de estoque.  
🟡 **Prioridade média**: melhorar UX da página de comparação e adicionar validação nos campos de telefone e CEP.  
🟢 Funcionalidades básicas estão estáveis, mas exigem ajustes para assegurar maior confiabilidade.

---

### 💡 Recomendações

✅ Revisar a segurança de rotas internas (páginas acessíveis via URL).  
✅ Ajustar lógica de filtros e ordenações para listagem e pesquisa de produtos.  
✅ Incluir verificações para produtos fora de estoque em todas as etapas de compra.  
✅ Implementar validações completas de campos (telefone, CEP, e-mail).  
✅ Melhorar o caminho de navegação para a página de comparação de produtos.
