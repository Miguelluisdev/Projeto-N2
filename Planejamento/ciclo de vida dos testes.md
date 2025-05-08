# Ciclo de Vida de Testes

O **Ciclo de Vida de Testes** é o processo completo que define as etapas que os testes seguem desde o planejamento até o encerramento. Ele se aplica tanto para testes manuais quanto para automatizados, com algumas diferenças pontuais.

## 🔄 Etapas do Ciclo de Vida (Manual e Automatizado)

### 1. Análise de Requisitos
**Objetivo**: Entender o que será testado.  
**Exemplo (e-commerce)**: "Usuário pode adicionar produto ao carrinho", "Pagamento com cartão deve funcionar".  
**Ação (QA)**: Ler histórias de usuário, critérios de aceitação e tirar dúvidas.

### 2. Planejamento de Testes
**Objetivo**: Definir o escopo dos testes, quem testa, o quê, como e quando.  
**Exemplo**: Definir que o login, cadastro e carrinho serão testados nessa sprint.  
**Ação**: Escolher ferramentas, tempo necessário, definir se será manual, automatizado ou ambos.

### 3. Design dos Casos de Teste
**Objetivo**: Escrever os casos de teste com passos claros.  
**Exemplo (manual)**:

**Título**: Adicionar produto ao carrinho  
**Pré-condição**: Usuário logado  
**Passos**: Buscar produto → clicar em "Adicionar" → verificar carrinho  
**Resultado Esperado**: Produto aparece no carrinho

**Exemplo (automatizado)**: Escrever scripts com Cypress ou Selenium simulando o mesmo cenário.

### 4. Configuração do Ambiente de Testes
**Objetivo**: Garantir que o ambiente (servidores, dados, ferramentas) esteja pronto.  
**Exemplo**: Ter uma versão de testes do e-commerce com dados fictícios, acesso ao banco de dados e ferramentas como Postman, Cypress, etc.

### 5. Execução dos Testes
- **Manual**: Seguir os passos dos casos de teste e registrar o resultado (passou, falhou, etc.).
- **Automatizado**: Rodar os scripts e verificar os logs/prints dos testes.  
**Exemplo**:  
Testar se o botão "Comprar agora" leva à página de pagamento.  
Verificar se o campo "CEP" bloqueia letras.

### 6. Registro e Reporte de Bugs
**Objetivo**: Reportar falhas encontradas.  
**Ferramentas**: Jira, Trello, Azure DevOps.  
**Exemplo**: "Ao tentar pagar com cartão inválido, o site trava em tela branca."  
**Ação**: Relatar com prints, passos para reproduzir, ambiente, navegador, etc.

### 7. Reexecução dos Testes (Reteste e Regressão)
- **Reteste**: Testar novamente bugs corrigidos.
- **Regressão**: Verificar se nada que funcionava antes quebrou com a nova alteração.  
**Automatizado**: Scripts ajudam muito na regressão — rodam centenas de testes em minutos.

### 8. Encerramento do Ciclo de Testes
**Objetivo**: Finalizar e documentar os testes feitos.  
**Exemplo**: Checklist de testes concluídos, bugs pendentes, cobertura de testes.  
**Entregáveis**: Relatórios de testes, indicadores (ex: % de falhas corrigidas), aprendizados.

---

## 🔍 Diferenças entre Manual e Automatizado

| **Aspecto**         | **Teste Manual**                            | **Teste Automatizado**                          |
|---------------------|---------------------------------------------|------------------------------------------------|
| **Execução**        | Por um humano                               | Por scripts/códigos                            |
| **Tempo**           | Mais demorado                               | Mais rápido, ideal para testes repetitivos     |
| **Custo inicial**   | Baixo                                       | Alto (precisa programar os testes)            |
| **Manutenção**      | Fácil (mas repetitiva)                      | Requer atenção com mudanças no sistema        |
| **Ideal para**      | Testes exploratórios, UI, testes únicos    | Testes de regressão, carga, performance       |
