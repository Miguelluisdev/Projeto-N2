# 📝 Relatório de Testes Manuais - Submissão de Formulários

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

| Caso de Teste                                                       | Status                                              |
|----------------------------------------------------------------------|-----------------------------------------------------|
| 01 - Submissão com todos os campos válidos                           | ✅ Passou                                            |
| 02 - Campo obrigatório vazio                                         | ✅ Passou                                            |
| 03 - Formato inválido (email)                                        | ✅ Passou                                            |
| 04 - Formato inválido (telefone/CEP/outros)                          | ❌ Não passou - Não há validação para estes campos  |
| 05 - Validação client-side e server-side                             | ✅ Passou                                            |

---

## 🚨 Bugs e Falhas Críticas Encontradas

- ❌ **Falta de validação para campos como telefone e CEP**: atualmente não impede o envio de dados inválidos nesses campos.

---

## 🟢 Testes que Passaram

✅ Submissão bem-sucedida com dados corretos.  
✅ Verificação de campos obrigatórios.  
✅ Validação adequada para email.  
✅ Consistência de validações client-side e server-side.

---

## 🔴 Testes que Falharam

❌ Falta de validação para campos como telefone, CEP e outros formatos específicos.

---

## ⚙️ Conclusão

⚠️ Os formulários estão consistentes para campos essenciais (como email e campos obrigatórios). No entanto, **é necessário adicionar validação para campos como telefone e CEP** para evitar envios incorretos e problemas de UX.
