# Estratégia de Teste — SauceDemo

## Escopo

- **Login e Logout**: telas de autenticação, validação de credenciais e encerramento de sessão.
- **Catálogo**: listagem de produtos, incluindo descrições, preços e filtros.
- **Carrinho de Compras**: adição, remoção e persistência dos itens selecionados.
- **Checkout**: fluxo completo de finalização da compra.
- **Opções do Menu (parcial)**:
  - *Logout* — em escopo, parte da gestão de sessão.
  - *All Items* — em escopo, controla a navegação principal do catálogo.
  - *Reset App State* — em escopo. Reintegrado após investigação confirmar que a função limpa o carrinho sem fornecer feedback visual ao usuário (achado documentado).

## Fora de escopo

- **About** (menu de opções) — redireciona para um domínio externo (saucelabs.com), fora do controle da aplicação testada.

## Abordagem

Teste manual, caixa-preta.

## Prioridade

**Por evidência de risco (achados confirmados):**
- **Checkout** — Alta. Ponto crítico de conversão do negócio; maior impacto financeiro em caso de falha de fluxo ou cálculo.
- **Sessão / Logout** — Alta. Evidências concretas de falhas na gestão de sessão e no encerramento por inatividade.

**Por criticidade estrutural (bloqueadores de fluxo):**
- **Login e Catálogo** — Média/Alta. Sem achados graves registrados até o momento, mas são portas de entrada da aplicação — se falharem, todos os testes subsequentes ficam bloqueados.

## Fora de cobertura desta rodada (risco assumido conscientemente)

Teste de carga, múltiplos navegadores e teste de acessibilidade não foram executados nesta etapa do projeto — decisão consciente de escopo para um ciclo de teste solo, dentro do tempo disponível, não limitação de ferramenta.
