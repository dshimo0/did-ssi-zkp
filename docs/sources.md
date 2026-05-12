# Fontes e Origem dos Dados

Consulta inicial: 2026-05-12.

Esta matriz lista as fontes usadas no repositorio e o escopo em que cada uma deve ser citada.

## Padroes e protocolos

| ID | Fonte | Status observado | Uso no repositorio |
| --- | --- | --- | --- |
| S1 | [W3C Decentralized Identifiers (DIDs) v1.0](https://www.w3.org/TR/did-core/) | W3C Recommendation | Definicao de DID, DID Document, DID URL, metodos DID e resolucao. |
| S2 | [W3C Verifiable Credentials Data Model v2.0](https://www.w3.org/TR/vc-data-model-2.0/) | W3C Recommendation, 2025-05-15 | Modelo de credenciais, apresentacoes, papeis emissor-holder-verificador, privacidade, seguranca e ZKP. |
| S3 | [W3C Verifiable Credential Data Integrity 1.0](https://www.w3.org/TR/vc-data-integrity/) | W3C Recommendation, 2025-05-15 | Provas de integridade, suites criptograficas e verificacao de documentos. |
| S4 | [W3C Securing Verifiable Credentials using JOSE and COSE](https://www.w3.org/TR/vc-jose-cose/) | W3C Recommendation, 2025-05-15 | Uso de JOSE, SD-JWT e COSE para proteger VCs e VPs. |
| S5 | [W3C Bitstring Status List v1.0](https://www.w3.org/TR/vc-bitstring-status-list/) | W3C Recommendation, 2025-05-15 | Status, suspensao e revogacao com foco em privacidade. |
| S6 | [W3C Data Integrity BBS Cryptosuites v1.0](https://www.w3.org/TR/vc-di-bbs/) | Candidate Recommendation Draft, 2026-04-07 | Disclosure seletivo e provas derivadas com BBS; tratar como tecnologia em evolucao. |
| S7 | [OpenID for Verifiable Credential Issuance 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0-final.html) | OpenID Final Specification, 2025-09-16 | Fluxos de emissao de credenciais, credential offer, credential endpoint e metadata. |
| S8 | [OpenID for Verifiable Presentations 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0-final.html) | OpenID Final Specification, 2025-07-09 | Solicitar e entregar apresentacoes, DCQL, `vp_token` e fluxos same-device/cross-device. |
| S9 | [DIF Presentation Exchange](https://identity.foundation/presentation-exchange/) | DIF spec family, com versoes ratificadas listadas pela DIF | Presentation Definition e Presentation Submission; usar quando a PoC exigir esse modelo. |
| S10 | [Hyperledger AnonCreds](https://github.com/hyperledger/anoncreds) | Projeto open source Hyperledger | Credenciais com ZKP e unlinkability; usar em comparativos e alternativas tecnicas. |
| S11 | [OpenWallet Foundation Credo](https://openwallet.foundation/projects/credo/) | Projeto OpenWallet Foundation | Framework de referencia para DIDComm, credenciais e interoperabilidade. |
| S12 | [did:web Method Specification](https://w3c-ccg.github.io/did-method-web/) | Draft W3C CCG | Metodo DID baseado em dominio HTTPS; recomendado apenas para PoC ou emissores com dominio controlado. |
| S13 | [did:key DID Method Specification](https://w3c-ccg.github.io/did-key-spec/) | Draft W3C CCG | Metodo DID derivado de chave publica; util para exemplos, chaves efemeras e PoCs. |
| S14 | [W3C DID Methods Registry](https://w3c.github.io/did-extensions/methods/) | Registro de metodos em desenvolvimento | Descoberta de metodos DID; nao deve ser tratado como endosso de metodo especifico. |
| S15 | [Trust Over IP Foundation](https://www.trustoverip.org/about/about/) | Fundacao e materiais publicos | Governanca, arquitetura de confianca e modelos de ecossistema. |

## Contexto brasileiro

| ID | Fonte | Status observado | Uso no repositorio |
| --- | --- | --- | --- |
| B1 | [Carteira de Identidade Nacional - Governo Digital](https://www.gov.br/governodigital/pt-br/identidade/identificacao-do-cidadao-e-carteira-de-identidade-nacional/carteira-de-identidade-nacional-cin) | Pagina oficial Gov.br, atualizada em 2026 | CPF como numero unico, formato fisico/digital, QR Code, GOV.BR e objetivos da CIN. |
| B2 | [Niveis da conta GOV.BR](https://www.gov.br/governodigital/pt-br/identidade/conta-gov-br/niveis-da-conta-govbr) | Pagina oficial Gov.br | Niveis bronze, prata e ouro, metodos de validacao e relacao com CIN/ICP-Brasil. |
| B3 | [Certificacao Digital - ITI](https://www.gov.br/iti/pt-br/acesso-a-informacao/perguntas-frequentes/certificacao-digital) | Pagina oficial ITI, atualizada em 2026 | Certificado digital ICP-Brasil, identificacao segura e assinatura eletronica qualificada. |
| B4 | [Lei Geral de Protecao de Dados Pessoais - Lei 13.709/2018](https://www.planalto.gov.br/ccivil_03/_Ato2015-2018/2018/Lei/L13709compilado.htm) | Texto compilado Planalto | Privacidade, autodeterminacao informativa, bases legais e direitos do titular. |
| B5 | [Decreto 11.797/2023](https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/decreto/d11797.htm) | Texto Planalto | Servico de Identificacao do Cidadao, governanca da identificacao e uso do CPF como chave de vinculacao. |
| B6 | [Decreto 10.977/2022](https://www.planalto.gov.br/ccivil_03/_Ato2019-2022/2022/Decreto/D10977.htm) | Texto Planalto | Padroes da carteira de identidade fisica/digital, requisitos de seguranca, QR Code e interoperabilidade. |
| B7 | [Lei 14.063/2020](https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2020/Lei/L14063.htm) | Texto Planalto | Assinaturas eletronicas simples, avancadas e qualificadas. |

## Regra para novas fontes

Ao adicionar uma nova fonte:

1. Prefira documento oficial, especificacao, lei, decreto, repositorio oficial ou documentacao mantida pelo projeto.
2. Registre o link nesta matriz.
3. Informe o status observado e a data de consulta quando o status for relevante.
4. Use a fonte perto da afirmacao no arquivo alterado.

## Alegacoes sem fonte primaria

Itens como "bCPF" ou "bCNPJ" devem permanecer fora da proposta principal ate haver fonte primaria, documento oficial ou material tecnico identificavel. Se forem discutidos, devem ser marcados como hipotese ou pauta de pesquisa, nao como fato estabelecido.
