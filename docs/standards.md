# Padroes e Protocolos

Este arquivo resume os padroes que orientam a proposta. A fonte completa de cada item esta em [sources.md](sources.md).

## Camada de identificadores

| Tema | Recomendacao | Fonte |
| --- | --- | --- |
| DID Core | Usar W3C DID Core como definicao base de DID, DID Document, DID URL e relacoes de verificacao. | S1 |
| Metodo para emissor | Comecar com `did:web` quando o emissor controlar um dominio HTTPS. | S12, S14 |
| Metodo para titular | Usar `did:key` ou identificadores efemeros em exemplos e PoCs de baixa complexidade. | S13, S14 |
| Producao | Avaliar metodo DID conforme requisitos de governanca, rotacao de chaves, recuperacao, auditoria e privacidade. | S1, S14 |

`did:web` e `did:key` sao escolhas pragmaticas para iniciar, nao substituem uma decisao de arquitetura para producao.

## Camada de credenciais

| Tema | Recomendacao | Fonte |
| --- | --- | --- |
| Modelo de dados | Adotar W3C Verifiable Credentials Data Model v2.0. | S2 |
| Integridade | Comecar com Data Integrity ou JOSE/COSE conforme stack escolhida. | S3, S4 |
| Status e revogacao | Planejar status desde a primeira PoC, mesmo que a implementacao venha depois. | S5 |
| Schemas | Definir schemas versionados para cada tipo de credencial. | S2 |
| Evidencias | Separar evidencia de prova criptografica; evidencia apoia confianca, prova garante integridade/autenticidade. | S2 |

## Camada de emissao e apresentacao

| Tema | Recomendacao | Fonte |
| --- | --- | --- |
| Emissao | Usar OpenID4VCI para fluxos interoperaveis de emissao. | S7 |
| Apresentacao | Usar OpenID4VP para solicitar e entregar apresentacoes. | S8 |
| Definicao de requisitos | Avaliar DIF Presentation Exchange quando o verificador precisar expressar requisitos detalhados. | S9 |
| Wallet initiated / issuer initiated | Modelar ambos como fluxos possiveis, mas escolher um primeiro caso simples para a PoC. | S7, S8 |

## Privacidade e ZKP

| Tema | Recomendacao | Fonte |
| --- | --- | --- |
| Minimizacao | Solicitar apenas os atributos necessarios ao contexto. | S2, B4 |
| Disclosure seletivo | Usar SD-JWT ou BBS quando a PoC exigir revelar apenas parte da credencial. | S4, S6 |
| Unlinkability | Avaliar BBS ou AnonCreds para reduzir correlacao entre apresentacoes. | S6, S10 |
| ZKP | Tratar ZKP como meio tecnico para requisitos especificos, nao como requisito universal. | S2, S6, S10 |

O W3C VC Data Model v2.0 descreve compatibilidade com ZKP, mas cada mecanismo concreto possui capacidades e requisitos proprios. Portanto, a escolha entre SD-JWT, BBS, AnonCreds ou outro mecanismo deve vir depois do caso de uso e do modelo de ameacas.

## Interoperabilidade

Requisitos minimos para a PoC:

- Documentar formato de credencial.
- Documentar metodo DID usado por cada ator.
- Documentar algoritmo de assinatura ou prova.
- Documentar como o verificador resolve chaves.
- Documentar como status/revogacao sera consultado.
- Documentar quais dados sao revelados em cada apresentacao.

## Riscos tecnicos a acompanhar

| Risco | Mitigacao |
| --- | --- |
| Correlacao por identificador persistente | Usar identificadores por par, pseudonimos ou provas derivadas quando possivel. |
| Excesso de dados na apresentacao | Definir politicas de minimizacao e testes de payload. |
| Revogacao que revela uso da credencial | Preferir mecanismos de status com protecao de privacidade. |
| Dependencia de metodo DID experimental | Registrar status do metodo e preparar alternativa. |
| Confusao entre autenticacao e credencial verificavel | Documentar fluxos separadamente: login, emissao, apresentacao e verificacao. |
