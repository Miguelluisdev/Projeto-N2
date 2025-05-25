# 📝 Relatório de Testes Manuais - Checkout

## 🔗 URL Testada
[https://qazando-shop.com](https://automationpratice.com.br/)

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

## 📌 Casos de Teste Executados

### 🟢 Cenário 01: Checkout Completo (Usuário Logado)

| Caso de Teste                                                                                       | Status                       |
|------------------------------------------------------------------------------------------------------|------------------------------|
| 01 - Usuário logado deve completar o processo de checkout                                           | ✅ Passou                    |
| 02 - Checkout Completo (Usuário Novo - Registro no Checkout)                                        | ❌ Não Passou - Erro de segurança: checkout possível mesmo deslogado ou logado |
| 03 - Checkout - Usar Endereço de Faturamento Diferente                                              | ✅ Passou, mas não altera nada |
| 04 - Checkout - Adicionar Novo Endereço                                                              | ❌ Não Passou - Não permite adicionar novo endereço |

---

### 🟡 Cenário 02: Validações no Checkout

| Caso de Teste                                                                                       | Status                       |
|------------------------------------------------------------------------------------------------------|------------------------------|
| 05 - Tentar Avançar Sem Selecionar Endereço                                                          | ✅ Passou                    |
| 06 - Tentar Avançar Sem Selecionar Frete                                                             | ⏳ Não Testado               |
| 07 - Tentar Avançar Sem Aceitar Termos                                                               | ✅ Passou                    |
| 08 - Tentar Avançar Sem Selecionar Pagamento                                                         | ✅ Passou                    |
| 09 - Validação de Campos em Novos Endereços                                                          | ❌ Não Passou - Não há opção para novo endereço |

---

### 🟠 Cenário 03: Acesso Restrito e Confirmação Final

| Caso de Teste                                                                                       | Status                       |
|------------------------------------------------------------------------------------------------------|------------------------------|
| 10 - Tentar Pular Etapas do Checkout via URL                                                         | ❌ Não Passou - Erro grave de segurança: etapas puladas via URL |
| 11 - Confirmação Final de Pedido                                                                     | ❌ Não Passou - Não existe confirmação final |

---

## 🚨 Bugs e Falhas Críticas Encontradas

- ❌ **Checkout possível mesmo deslogado:** vulnerabilidade grave de segurança.  
- ❌ **Não permite adicionar novo endereço:** falta de funcionalidade essencial.  
- ❌ **Pulo de etapas via URL:** grave falha de segurança.  
- ❌ **Não há confirmação final do pedido:** falta de clareza e segurança no processo de finalização.  

---

## 🟡 Análise Rápida

O fluxo de checkout apresenta **problemas graves de segurança e ausência de funcionalidades básicas**:

🔴 Vulnerabilidade: checkout permitido sem autenticação.  
🔴 Usuário consegue pular etapas modificando a URL.  
🟠 Não há confirmação final clara do pedido.  
🟠 Falta opção para adicionar novo endereço e validação de campos.  

---

## 🟢 Testes que Passaram

✅ Checkout básico (usuário logado).  
✅ Uso de endereço de faturamento diferente (não altera nada).  
✅ Validações de campos obrigatórios (endereços, termos, pagamentos).  

---

## 🔴 Testes que Falharam

❌ Registro de novo usuário no checkout.  
❌ Adição de novo endereço.  
❌ Falta confirmação final do pedido.  
❌ Falhas de segurança ao pular etapas pela URL.

---

## 🟠 Testes não Realizados

⏳ Avançar sem selecionar frete.

---

## ⚙️ Conclusão

🚨 O fluxo de checkout precisa de **correções urgentes**:  
- **Bloquear checkout sem autenticação** (erro crítico).  
- **Corrigir o bypass de etapas via URL**.  
- **Implementar adição de novo endereço e validação de campos**.  
- **Adicionar uma página de confirmação final do pedido**.
