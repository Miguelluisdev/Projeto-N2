# 📝 Relatório de Testes Manuais - Formulário de Contato e Newsletter

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

### 🟢 Cenário 01: Formulário de Contato

| Caso de Teste                                                    | Status                                              |
|-------------------------------------------------------------------|-----------------------------------------------------|
| 01 - Envio com Sucesso                                           | ✅ Passou                                            |
| 02 - Envio - Campos Obrigatórios Vazios                          | ✅ Passou                                            |
| 03 - Envio - Email Inválido                                      | ❌ Não Passou - Email inválido é aceito sem validação e a mensagem (campo) também não é validada como obrigatória |

---

### 🟠 Cenário 02: Newsletter e Comparação

| Caso de Teste                                                    | Status                                              |
|-------------------------------------------------------------------|-----------------------------------------------------|
| 04 - Inscrição com Sucesso                                       | ✅ Passou                                            |
| 05 - Inscrição - Email Inválido                                  | ✅ Passou                                            |
| 06 - Inscrição - Email Duplicado                                 | ⏳ Não Testado                                       |
| 07 - Adicionar Produtos à Comparação                             | ✅ Passou                                            |
| 08 - Visualizar Página de Comparação                             | ❌ Não Passou - A página de comparação só é acessível via URL ou footer, dificultando o acesso para o usuário |
| 09 - Remover Produto da Comparação                               | ✅ Passou                                            |
| 10 - Adicionar ao Carrinho da Comparação                         | ✅ Passou                                            |

---

## 🚨 Bugs e Falhas Críticas Encontradas

- ❌ **Validação do Formulário de Contato**: email inválido aceito sem alerta de erro e campo de mensagem sem verificação obrigatória.  
- ❌ **Página de Comparação de Produtos**: acessível apenas via URL ou footer, dificultando a navegação para o usuário.

---

## 🟢 Testes que Passaram

✅ Envio do formulário com sucesso e validação de campos vazios.  
✅ Inscrição na newsletter (sucesso e email inválido).  
✅ Funcionalidade de comparação (adicionar/remover itens e adicionar ao carrinho).

---

## 🔴 Testes que Falharam

❌ Email inválido aceito no formulário de contato.  
❌ Falta de caminho intuitivo para acessar a página de comparação.

---

## ⏳ Testes não Realizados

⏳ Inscrição de email duplicado na newsletter.

---

## ⚙️ Conclusão

⚠️ Apesar de muitos testes terem passado, foram identificados **pontos críticos**:

🔴 **Validação de email no formulário de contato precisa de ajuste**.  
🔴 **Campo de mensagem deve ser obrigatório**.  
🟠 **Página de comparação precisa de um acesso mais intuitivo no site**.
