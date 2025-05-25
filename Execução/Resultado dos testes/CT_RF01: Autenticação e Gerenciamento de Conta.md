# 📝 Relatório de Testes Manuais - QAZANDO Shop E-Commerce

## 🔗 URL Testada
[[](https://automationpratice.com.br/)](https://automationpratice.com.br/)

## 🗓️ Data dos Testes
24/05/2025

## 👤 Testador
Miguel Luis

## 💻 Ambiente de Testes

| Item                | Detalhes                                 |
|----------------------|------------------------------------------|
| Sistema Operacional  | Windows 11                               |
| Navegador            | Microsoft Edge 136.0v                    |
| Tipo de Teste        | Exploratório e casos de teste manuais    |

---

## 📌 Cenário de Teste 1 - Autenticação

| Caso de Teste                                                               | Status   |
|------------------------------------------------------------------------------|----------|
| 01 - Login com credenciais válidas                                           | ✅ Passou |
| 02 - Login com senha incorreta                                               | ❌ Não Passou |
| 03 - Login com email não cadastrado                                          | ❌ Não Passou |
| 04 - Login com email em formato inválido                                     | ✅ Passou |
| 05 - Login sem fornecer e-mail e senha                                       | ✅ Passou |
| 06 - Logout realizado com sucesso                                            | ✅ Passou |

**Observações/Bugs encontrados:**
- Falha no login com senha incorreta e email não cadastrado (não exibe mensagem clara ou permanece na mesma tela sem feedback).
- Mensagens de erro inconsistentes e, em alguns casos, ausentes.
- Falhas de segurança ao tentar login sem dados ou dados inválidos.

---

## 📌 Cenário de Teste 2 - Cadastro na Plataforma

| Caso de Teste                                                               | Status         |
|------------------------------------------------------------------------------|-----------------|
| 01 - Cadastro de novo usuário com sucesso                                    | ✅ Passou       |
| 02 - Cadastro sem dados obrigatórios                                         | ✅ Passou       |
| 03 - Cadastro sem nome                                                       | ✅ Passou       |
| 04 - Cadastro sem e-mail                                                     | ✅ Passou       |
| 05 - Cadastro sem senha                                                      | ✅ Passou       |
| 09 - Cadastro duplicado do mesmo usuário                                     | ❌ Falhou       |

**Bugs encontrados:**
- Erro no input de "olho" (mostrar/ocultar senha) — botão sem funcionamento.
- Falha ao validar cadastro de usuário duplicado (não bloqueia nem exibe erro).
- Mensagens de erro não aparecem ou estão ausentes nos campos obrigatórios.

---

## 📌 Cenário de Teste 3 - Gerenciamento de Conta

| Caso de Teste                                                                                       | Status            |
|-----------------------------------------------------------------------------------------------------|--------------------|
| 01 - Redefinir senha e login com nova senha                                                         | ❌ Não Passou (usuário logou como admin indevidamente) |
| 02 - Logout de usuário                                                                              | ✅ Passou          |
| 03 - Edição de informações pessoais                                                                 | ⚠️ Passou com bug - usuário loga como admin após edição |
| 04 - Adição de novo endereço                                                                        | ❌ Não Funciona    |
| 05 - Edição de endereço existente                                                                   | ❌ Não Funciona    |
| 06 - Remoção de endereço existente                                                                  | ❌ Não Funciona    |
| 07 - Visualização de histórico de pedidos                                                           | ✅ Passou          |
| 08 - Visualização de detalhes de um pedido                                                          | ✅ Passou          |

**Bugs encontrados:**
- Falha grave: usuário loga como admin após redefinir senha ou editar informações.
- Botão de adição de novo endereço não funciona.
- Falha ao editar e remover endereço (não permitido ou inativo).
- Falta de validação de segurança ao acessar áreas sensíveis.

---

## 🚨 Bugs Críticos/Graves Encontrados

✅ Falha de segurança ao logar como admin em cenários de redefinição e edição de perfil.  
✅ Mensagens de erro não aparecem (ou aparecem parcialmente) em formulários de login/cadastro.  
✅ Falha de usabilidade e feedback em diversas etapas do cadastro e login.  
✅ Erros de UI/UX e navegabilidade, como botões inativos ou mal posicionados.

---

## 🟡 Análise Rápida

O sistema apresenta falhas significativas em segurança, inconsistências em mensagens de erro e má implementação de campos obrigatórios.  
Houve problemas críticos como:

- Acesso indevido a conta de admin.
- Cadastro duplicado não tratado.
- Falhas de UI/UX (ex.: botão de olho no campo de senha, botões de endereço inativos).
- Mensagens de erro faltando em diversos formulários.

---

## 🔍 Testes que Passaram

✅ Login válido  
✅ Login com e-mail inválido  
✅ Login sem dados  
✅ Logout  
✅ Cadastro com dados corretos e casos sem campos obrigatórios (não deveria passar em todos os casos, mas o sistema aceita)  
✅ Visualização de histórico de pedidos e detalhes do pedido  

---

## ⚙️ Conclusão

A aplicação QAZANDO Shop E-Commerce **possui diversos problemas críticos e graves** de segurança e inconsistências na experiência do usuário. É recomendado um ciclo completo de correção e reteste, com foco em:

- Mensagens de erro consistentes e visíveis.
- Validação adequada de dados de cadastro e login.
- Correção de falhas de segurança e acesso indevido.
- Melhoria nos fluxos de cadastro, login e gerenciamento de conta.

---

## ✍️ Observações Finais

✅ Testes realizados de forma **exploratória** e documentados manualmente.  
✅ Relatório inicial, análise mais detalhada será feita posteriormente com vídeos e prints dos erros.  
✅ Ambiente de testes: Windows 11 + Microsoft Edge 136.0v.  
✅ Importante para futuras correções e melhoria contínua do produto.
