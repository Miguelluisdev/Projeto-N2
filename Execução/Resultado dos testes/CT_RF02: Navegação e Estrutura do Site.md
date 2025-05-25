# 📝 Relatório de Testes Manuais - Cenário 01: Navegação e Estrutura do Site

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
| 01 - Deve navegar para a PLP de Eletrônicos pelo menu principal                                          | ✅ Passou  |
| 02 - Deve retornar à Homepage ao clicar no logo                                                           | ✅ Passou  |
| 05 - Deve acessar a página de Contato pelo cabeçalho                                                      | ✅ Passou  |
| 06 - Deve realizar o Login (deslogado) ou Logout (logado) corretamente                                     | ✅ Passou  |
| 07 - Deve acessar a página do Carrinho pelo cabeçalho                                                     | ✅ Passou  |
| 08 - Deve acessar os links informativos no rodapé corretamente                                            | ✅ Passou  |
| 09 - Deve acessar “Meus Pedidos” com comportamento correto logado/deslogado                                | ❌ Não Passou - Possível acessar via URL (erro grave de segurança) |
| 11 - Deve acessar a página correta ao clicar em banner promocional                                        | ✅ Passou  |
| 12 - Deve validar que todos os links clicáveis não estão quebrados                                        | ⚠️ Parcialmente - Links de redes sociais não funcionam, mas demais links OK |

---

## 🚨 Bugs e Falhas Encontrados

✅ **Erro grave de segurança:** É possível acessar páginas internas (ex.: "Meus Pedidos") diretamente pela URL, mesmo deslogado.  
✅ Links para redes sociais no rodapé estão **quebrados** e não funcionam.  
✅ Falha de validação de autenticação em páginas sensíveis (ex.: "Meus Pedidos").

---

## 🟡 Análise Rápida

O sistema apresenta **graves falhas de segurança** no fluxo de navegação, permitindo acesso a páginas internas apenas com a URL. Além disso, há problemas de usabilidade relacionados a links de redes sociais inativos.

✅ Os demais fluxos de navegação (menu principal, banners, cabeçalho, rodapé) funcionam corretamente.  
✅ Experiência de navegação geral boa, mas com falhas de segurança críticas e links de redes sociais inativos.

---

## 🔍 Testes que Passaram

✅ Navegação pelo menu principal para a PLP de Eletrônicos.  
✅ Retorno à homepage pelo logo.  
✅ Acesso à página de Contato.  
✅ Acesso ao Login/Logout.  
✅ Acesso ao Carrinho.  
✅ Acesso aos links informativos no rodapé.  
✅ Acesso correto ao clicar em banner promocional.

---

## 🚧 Testes que Falharam

❌ Acesso à página “Meus Pedidos” sem estar logado (erro de segurança).  
❌ Links de redes sociais no rodapé estão quebrados.

---

## ⚙️ Conclusão

Apesar da navegação principal funcionar bem, **o sistema precisa de correções urgentes**:

- Bloquear acesso direto a URLs internas quando o usuário não está autenticado.
- Corrigir links de redes sociais no rodapé.
- Revisar segurança geral de páginas internas e implementações de autenticação.
