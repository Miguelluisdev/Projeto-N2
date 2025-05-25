# 📝 Relatório de Testes Manuais - Cenário 03: Pesquisa de Produtos

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

| Caso de Teste                                                                                           | Status    |
|----------------------------------------------------------------------------------------------------------|-----------|
| 01 - Deve exibir produtos relevantes ao pesquisar por um termo existente (ex: "notebook")                 | ❌ Não Passou - Mostra itens irrelevantes com nomes errados e não condizentes com a pesquisa |
| 02 - Deve encontrar o produto ao pesquisar por parte do nome ou SKU                                       | ❌ Não Passou - Produtos mostrados mudam de nome e imagem, causando erro de identificação |
| 03 - Deve aplicar ordenação e/ou filtros com sucesso após uma busca                                       | ❌ Não Passou - Filtro funciona mas está invertido (ex.: "High to Low" mostra itens mais baratos primeiro) |
| 04 - Deve exibir mensagem "Nenhum resultado encontrado" ao pesquisar por termo inexistente                | ❌ Não Passou - Não exibe mensagem e continua mostrando itens irrelevantes |
| 05 - Deve lidar corretamente com tentativa de busca com campo vazio                                       | ✅ Passou  |

---

## 🚨 Bugs e Falhas Encontrados

✅ **Erro de correspondência de resultados**: A busca exibe produtos sem relação com o termo pesquisado, gerando confusão ao usuário.

✅ **Erro de identificação**: Produtos alteram nome e imagem ao pesquisar por parte do nome ou SKU, dificultando a navegação e gerando inconsistências.

✅ **Erro de ordenação/filtro**: Filtros estão invertidos — "High to Low" exibe itens baratos e "Low to High" mostra itens caros, sem efeito visível nos demais produtos.

✅ **Ausência de mensagem de busca sem resultado**: Falha de usabilidade ao não exibir a mensagem “Nenhum resultado encontrado” e exibir itens irrelevantes.

---

## 🟡 Análise Rápida

O módulo de pesquisa de produtos **apresenta diversas falhas críticas**, comprometendo diretamente a experiência do usuário e a confiabilidade dos resultados de busca.

✅ O único caso que passou foi a busca com campo vazio, que manteve a página inalterada corretamente.  
❌ Os demais casos demonstram falhas graves de funcionamento, inconsistências visuais e falhas de comunicação com o usuário.

---

## 🔍 Testes que Passaram

✅ Campo de busca vazio não causa erro e não altera a página.

---

## 🚧 Testes que Falharam

❌ Busca por termo existente retorna resultados errados.  
❌ Busca por parte do nome ou SKU gera inconsistências de nomes e imagens.  
❌ Filtros e ordenação funcionam de forma inversa e errada.  
❌ Falta de mensagem de "Nenhum resultado encontrado" em termos inválidos.

---

## ⚙️ Conclusão

O módulo de pesquisa necessita de uma revisão completa, incluindo:

- Correção na correspondência dos produtos com o termo buscado.  
- Estabilização das informações exibidas (nome e imagem corretos).  
- Ajustes na funcionalidade de filtros e ordenação.  
- Implementação da mensagem de “Nenhum resultado encontrado” quando necessário.
