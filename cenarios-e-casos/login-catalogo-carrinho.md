# Cenários e Casos de Teste — Login, Catálogo e Carrinho

*Cobertura em modo reduzido: estas áreas entraram no escopo por criticidade estrutural (bloqueadores de fluxo), sem achado grave confirmado — por isso receberam um cenário de fluxo principal cada, sem investigação aprofundada de bug.*

## Login
**Passos:** acessar o site → efetuar login com `standard_user` / `secret_sauce`
**Esperado:** login efetuado com sucesso, redirecionamento para a tela de produtos.
**Obtido:** conforme o esperado.

## Catálogo e Filtro
**Passos:** login → visualizar catálogo completo → aplicar cada filtro (Name A-Z, Name Z-A, Price low-high, Price high-low)
**Esperado:** produtos exibidos corretamente; filtros reordenando a lista de forma correta.
**Obtido:** filtros funcionam corretamente em todas as quatro ordenações. Descrições de dois produtos (Sauce Labs Backpack, Test.allTheThings() T-Shirt) apresentam erro de digitação/sintaxe de código embutida no texto — **reincidência** do achado já registrado na exploração inicial do sistema, não uma descoberta nova. Status: **Aprovado com ressalva.**

## Carrinho de Compras
**Passos:** login → adicionar produto ao carrinho → abrir carrinho e conferir nome/valor/descrição → remover o item
**Esperado:** produto exibido corretamente no carrinho; ao remover, o carrinho volta a ficar vazio.
**Obtido:** conforme o esperado.
