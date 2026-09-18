# QA Portfolio — Teste Manual Exploratório no SauceDemo

Projeto de teste manual completo, do zero, aplicado a um sistema real (SauceDemo), cobrindo desde a análise de risco até a documentação formal de bugs no padrão usado por times de QA no mercado.

> "Eu testei um sistema real, encontrei riscos e documentei tudo" — em vez de apenas listar cursos concluídos.

## O que este projeto demonstra

- Exploração de sistema sem documentação prévia, mapeando funcionalidades e regras de negócio observáveis
- Análise de risco com critérios formais de **severidade** (impacto funcional, caminho alternativo, escopo, reprodutibilidade) e **prioridade** (evidência de risco × criticidade estrutural)
- Estratégia de teste com escopo, fora de escopo e priorização justificados
- Cenários e casos de teste cobrindo fluxos principais, alternativos e de erro
- Três bugs reais, documentados no formato completo de bug report (título, ambiente, pré-condição, passos, resultado esperado × obtido, evidência, impacto)
- Separação disciplinada entre o que foi **observado** no ambiente de teste e o que seria **hipotético/projetado** em uma aplicação de produção real
- Conclusão final com avaliação de qualidade e recomendação de go/no-go

## Sistema testado

[SauceDemo](https://www.saucedemo.com/) — aplicação de e-commerce de demonstração, mantida pela Sauce Labs, usada publicamente pela comunidade de QA para prática de testes.

## Bugs encontrados

| # | Bug | Severidade | Prioridade |
|---|---|---|---|
| 1 | [Checkout finaliza com carrinho vazio, gerando comprovante de R$0,00](bugs-encontrados/bug-01-checkout-valor-zero.md) | Alta | Alta |
| 2 | [Logout automático por inatividade com mensagem enganosa](bugs-encontrados/bug-02-logout-mensagem-confusa.md) | Média-Alta | Alta |
| 3 | [Sessão permanece autenticada após fechamento total do navegador](bugs-encontrados/bug-03-sessao-persistente.md) | Alta (segurança) | Alta |

## Estrutura do repositório

```
├── README.md                          — este arquivo
├── estrategia-de-teste.md             — escopo, abordagem e priorização
├── cenarios-e-casos/                  — cenários e casos de teste por área
│   ├── checkout.md
│   ├── sessao-logout.md
│   └── login-catalogo-carrinho.md
├── bugs-encontrados/                  — os três bugs, em formato completo
│   ├── bug-01-checkout-valor-zero.md
│   ├── bug-02-logout-mensagem-confusa.md
│   └── bug-03-sessao-persistente.md
├── conclusao.md                       — avaliação final e recomendação
└── evidencias/                        — capturas de tela e comprovantes em PDF
```

## Sobre este projeto

Testado manualmente, em abordagem caixa-preta, como parte de uma formação prática em Quality Assurance.
