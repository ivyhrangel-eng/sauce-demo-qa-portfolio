# Bug #03 — Sessão permanece autenticada após fechamento total do navegador

**Severidade:** Alta (risco de segurança) | **Prioridade:** Alta (evidência de risco confirmada)

## Ambiente
Computador, Google Chrome versão 152.0.7977.84, conexão Wi-Fi

## Pré-condição
Usuário possui conta válida no sistema (`standard_user` / `secret_sauce`).

## Passos para reproduzir
1. Efetuar login com usuário e senha válidos
2. Fechar o navegador totalmente
3. Reabrir o navegador e acessar o site novamente

## Resultado esperado
O site deveria desconectar o usuário automaticamente, já que não existe a opção "mantenha-me conectado".

## Resultado obtido
Mesmo sem a opção "mantenha-me conectado", o site mantém o usuário logado após o navegador ser reaberto.

## Evidência
⚠️ **Pendente.** Este achado foi validado através de teste manual repetido, mas ainda não tem print/vídeo anexado neste repositório — recomendação registrada durante a investigação foi gravar vídeo (fechar navegador → reabrir → mostrar sessão ainda ativa, sem cortes) por se tratar de um comportamento sequencial no tempo, que print isolado não comprova sozinho. **Adicionar antes de considerar este bug pronto para portfólio público.**

## Impacto
**Observado no SauceDemo:** a sessão do usuário permanece ativa mesmo depois do navegador ser completamente fechado e reaberto.

**Projetado para uma aplicação real** (não confirmado, hipótese de risco): esse comportamento poderia representar risco de segurança em dispositivos compartilhados — um usuário que fecha o navegador acreditando ter encerrado sua sessão deixaria a conta acessível para a próxima pessoa que usar o mesmo computador. Isso configuraria acesso não autorizado à conta por terceiros com acesso físico ao dispositivo, com possíveis consequências jurídicas para a empresa em caso de uso indevido dos dados.
