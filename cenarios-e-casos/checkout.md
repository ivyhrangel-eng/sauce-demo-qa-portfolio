# Cenários e Casos de Teste — Checkout

## Caso 1 — Fluxo principal: checkout com produto no carrinho
**Passos:** login → adicionar produto ao carrinho → carrinho → checkout → preencher First Name/Last Name/Zip → Continue → Finish
**Esperado:** compra finalizada, comprovante gerado com o produto e valor corretos.
**Obtido:** conforme o esperado (evidência: `evidencias/checkout/caso1-overview-sucesso.png`, `evidencias/checkout/caso1-comprovante.pdf`).

## Caso 2 — Alternativo: checkout sem autenticação (N/A)
**Investigação:** verificado se existe algum modo de acesso ao checkout sem login.
**Evidência:** tentativa de acesso direto a `/cart.html` sem login retorna "Epic sadface: You can only access '/cart.html' when you are logged in."
**Conclusão:** Não aplicável — o SauceDemo exige autenticação para qualquer acesso; não existe modo convidado.
**Status:** N/A

## Caso 3 — Erro: checkout com carrinho vazio
**Passos:** login → carrinho vazio → checkout → preencher dados → Continue → Finish
**Esperado:** sistema bloqueia a finalização já no passo do carrinho, informando que está vazio.
**Obtido:** sistema finaliza a compra e gera comprovante de R$0,00 (evidência: `evidencias/checkout/caso3-overview-valor-zero.png`, `evidencias/checkout/caso3-comprovante-valor-zero.pdf`).
**→ Ver `bugs-encontrados/bug-01-checkout-valor-zero.md`**

*Nota: variações de login válido (ex: `visual_user`) testando o mesmo fluxo de checkout são casos de dado adicionais dentro do fluxo principal — não constituem um fluxo alternativo próprio, já que a rota até o objetivo é idêntica à do Caso 1.*
