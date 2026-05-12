# Exemplos

Os exemplos nesta pasta sao sinteticos e servem para discutir formato, fluxo e minimizacao de dados. Eles nao contem dados pessoais reais e nao devem ser tratados como credenciais validas em producao.

## Origem dos dados

| Arquivo | Origem | Observacao |
| --- | --- | --- |
| `credentials/age-credential-payload.example.json` | Sintetico, inspirado no modelo W3C VC Data Model v2.0. | Payload sem assinatura real. |
| `credentials/education-credential-payload.example.json` | Sintetico, inspirado nos exemplos de diploma do W3C VC Data Model v2.0. | Payload sem assinatura real. |
| `presentations/age-over-18-derived-presentation.example.json` | Sintetico, inspirado na secao de ZKP do W3C VC Data Model v2.0. | Apresentacao conceitual, prova criptografica placeholder. |

Fontes conceituais: [S2 - W3C VC Data Model v2.0](https://www.w3.org/TR/vc-data-model-2.0/) e [S6 - W3C Data Integrity BBS Cryptosuites v1.0](https://www.w3.org/TR/vc-di-bbs/). O `proofValue` do exemplo de apresentacao e deliberadamente um placeholder, nao uma prova criptografica real.

## Regra

Nao adicionar CPF, RG, CIN, QR Code, biometria, nome real, data de nascimento real ou documento real em exemplos publicos.
