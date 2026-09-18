# Cenários e Casos de Teste — Sessão / Logout

## Cenário 1 — Fluxo principal: logout manual
**Passos:** login → menu de opções → Logout
**Esperado:** sistema desloga a conta e retorna à tela de login.
**Obtido:** conforme o esperado.

## Cenário 2 — Alternativo: logout por outra via (N/A)
**Investigação:** verificado se existe caminho alternativo para a ação de logout pela interface.
**Conclusão:** não identificado nenhum caminho alternativo além do botão de menu.
**Status:** N/A

## Cenário 3 — Erro: logout automático por inatividade
**Passos:** login → aguardar ~17 min sem interação → clicar em qualquer elemento
**Esperado:** sistema desloga o usuário e informa claramente o motivo (ex: "sua sessão expirou por inatividade").
**Obtido:** sistema desloga o usuário, mas exibe "Epic sadface: You can only access '/cart.html' when you are logged in" — mensagem que não comunica a causa real.
**→ Ver `bugs-encontrados/bug-02-logout-mensagem-confusa.md`**

## Teste adicional — Persistência de sessão (fora da classificação de fluxo)
Não se encaixa em principal/alternativo/erro por não representar uma rota até um objetivo — é um teste de comportamento de sessão.
**Passos:** login → fechar navegador totalmente → reabrir e acessar o site
**Esperado:** sessão encerrada (não há opção "mantenha-me conectado").
**Obtido:** sessão permanece ativa.
**→ Ver `bugs-encontrados/bug-03-sessao-persistente.md`**
