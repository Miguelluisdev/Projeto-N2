# 📝 Relatório de Testes Manuais - Cenário 01: Visualização de Itens no Carrinho

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

| Caso de Teste                                                                                              | Status                      |
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| 01 - Deve exibir corretamente múltiplos itens no carrinho com detalhes e subtotais                           | ✅ Passou                   |
| 02 - Deve atualizar a quantidade do item corretamente                                                        | ✅ Passou                   |
| 03 - Deve permitir a remoção de um item do carrinho                                                          | ✅ Passou                   |
| 04 - Deve permitir a remoção de todos os itens do carrinho                                                   | ✅ Passou                   |
| 05 - Deve aplicar cupom válido e recalcular o total                                                          | ⏳ Não Testado              |
| 06 - Deve navegar para a página "Continuar Comprando"                                                        | ❌ Não Passou - Não existe a funcionalidade  |
| 07 - Deve navegar para a página de "Finalizar Compra"                                                        | ✅ Passou                   |
| 08 - Deve exibir erro ao tentar atualizar quantidade para valor inválido                                      | ✅ Passou                   |
| 09 - Deve exibir erro ao tentar aplicar um cupom inválido ou expirado                                        | ✅ Passou                   |
| 10 - Deve verificar precisão dos cálculos de subtotais e totais                                              | ✅ Passou                   |
| 11 - Deve impedir a aplicação de múltiplos cupons, se a regra for permitir apenas um                         | ⏳ Não Testado              |

---

## 🚨 Bugs e Falhas Encontrados

✅ **Ausência da funcionalidade "Continuar Comprando"**: o botão ou link para retornar às compras não existe, impactando a fluidez de navegação.  

---

## 🟡 Análise Rápida

O carrinho funciona bem para:  
- Exibir múltiplos itens e detalhes.  
- Atualizar quantidades e remover itens.  
- Calcular corretamente subtotais e totais.  
- Validar a entrada de cupons inválidos e quantidades erradas.

A principal falha é a ausência do botão **"Continuar Comprando"**, que prejudica a experiência do usuário ao forçá-lo a usar métodos alternativos de navegação.

---

## 🟢 Testes que Passaram

✅ Visualização de itens e subtotais.  
✅ Atualização de quantidades e remoção de itens.  
✅ Validação de erros para cupons inválidos.  
✅ Precisão dos cálculos de totais.  

---

## 🔴 Testes que Falharam

❌ Ausência do botão "Continuar Comprando".

---

## 🟠 Testes não Realizados

⏳ Aplicação de cupom válido e verificação de múltiplos cupons.

---

## ⚙️ Conclusão

Apesar de a maioria das funcionalidades do carrinho estarem corretas, a falta da opção **"Continuar Comprando"** compromete a navegação fluida do usuário. Recomenda-se:  
- Implementar o botão ou link para **"Continuar Comprando"**.  
- Executar testes para cupons válidos e múltiplos cupons para garantir consistência nas regras de desconto.
