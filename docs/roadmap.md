# Roadmap

Este roadmap organiza a expansao do repositorio em etapas pequenas, com entregaveis verificaveis.

## Fase 0 - Base documental

Status: iniciada.

Entregaveis:

- README reorganizado.
- Matriz de fontes.
- Arquitetura de referencia.
- Contexto brasileiro separado de hipoteses.
- Exemplos sinteticos iniciais.

Criterio de pronto: toda afirmacao factual relevante possui fonte ou esta marcada como interpretacao/hipotese.

## Fase 1 - Modelo de credenciais

Objetivo: definir os primeiros schemas conceituais.

Entregaveis:

- Credencial de maioridade.
- Credencial de diploma.
- Credencial de vinculo profissional.
- Credencial de representacao organizacional.

Criterios:

- Cada campo deve ter finalidade clara.
- Campos sensiveis devem ser evitados ou justificados.
- Cada exemplo deve declarar origem sintetica.

Fontes: S2, S5, B4.

## Fase 2 - PoC de emissao e verificacao

Objetivo: demonstrar o fluxo emissor, wallet e verificador.

Entregaveis:

- Emissor de laboratorio com `did:web`.
- Titular com identificador de teste.
- Verificador com validacao de assinatura, schema e validade.
- Documentacao do fluxo.

Fontes: S1, S2, S7, S8, S12.

## Fase 3 - Status e revogacao

Objetivo: incluir status de credencial sem expor uso desnecessario.

Entregaveis:

- Modelo de status.
- Politica de revogacao.
- Exemplo de credencial revogada ou suspensa.
- Teste de verificacao de status.

Fontes: S5, S2.

## Fase 4 - Disclosure seletivo

Objetivo: reduzir dados revelados em apresentacoes.

Entregaveis:

- Prova de maioridade sem data de nascimento.
- Apresentacao de diploma com campos minimos.
- Comparativo entre SD-JWT, BBS e AnonCreds para os casos escolhidos.

Fontes: S2, S4, S6, S10.

## Fase 5 - Contexto brasileiro e governanca

Objetivo: mapear aderencia a contexto institucional e juridico brasileiro.

Entregaveis:

- Matriz LGPD por caso de uso.
- Mapa de relacao com CIN, GOV.BR e ICP-Brasil.
- Modelo de registro de confianca.
- Riscos de correlacao e tratamento de identificadores nacionais.

Fontes: B1, B2, B3, B4, B5, B6, B7, S15.

## Backlog

- Avaliar integracao com frameworks como Credo, Veramo, Trinsic, Dock ou Microsoft Entra Verified ID.
- Criar diagramas C4.
- Criar exemplos assinados reais em ambiente local.
- Adicionar testes de validacao de JSON Schema.
- Criar matriz de ameacas.
- Criar guia de implementacao para `did:web`.
