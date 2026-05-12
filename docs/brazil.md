# Contexto Brasileiro

Este arquivo separa fatos documentados, inferencias e oportunidades de pesquisa para identidade descentralizada no Brasil.

## Fatos documentados

| Tema | O que a fonte afirma | Fonte |
| --- | --- | --- |
| CIN | A Carteira de Identidade Nacional usa o CPF como numero unico de identificacao, possui formato fisico e digital e inclui QR Code. | B1, B6 |
| CIN e GOV.BR | A versao digital da CIN esta disponivel no aplicativo GOV.BR. | B1 |
| Conta GOV.BR | A conta GOV.BR possui niveis bronze, prata e ouro, associados a diferentes formas de validacao. | B2 |
| Nivel ouro | O GOV.BR lista validacao por QR Code da CIN e certificado digital de pessoa fisica ICP-Brasil entre formas de elevar a conta. | B2 |
| ICP-Brasil | O certificado digital ICP-Brasil permite identificacao segura e assinaturas eletronicas qualificadas. | B3, B7 |
| LGPD | A LGPD estabelece fundamentos como respeito a privacidade e autodeterminacao informativa. | B4 |
| SIC | O Decreto 11.797/2023 trata do Servico de Identificacao do Cidadao e define o CPF como chave de vinculacao dos dados da pessoa natural no servico. | B5 |

As fontes B1 a B7 estao listadas em [sources.md](sources.md).

## Interpretacao para este projeto

Esta secao e uma interpretacao de arquitetura, nao uma afirmacao oficial.

A CIN, o GOV.BR e a ICP-Brasil formam uma base institucional forte de identificacao digital no Brasil. Uma arquitetura DID/SSI/VC nao deve tentar substituir esse ecossistema sem mandato legal ou institucional. O caminho mais realista para pesquisa e PoC e complementar fluxos existentes com credenciais verificaveis, minimizacao de dados e apresentacoes seletivas.

## Hipoteses de integracao

| Hipotese | Valor potencial | Cuidado |
| --- | --- | --- |
| Credencial verificavel derivada de documento oficial | Permitir verificacao de atributos sem compartilhar documento completo. | Exige base legal, governanca do emissor e politicas claras de privacidade. |
| Prova de atributo sem CPF | Reduz exposicao de identificador nacional em interacoes privadas. | O emissor ainda pode precisar validar a identidade de origem por canais oficiais. |
| Credencial organizacional ligada a CNPJ | Facilita prova de representacao de empresa. | Precisa de fonte oficial, autoridade emissora e mecanismo de revogacao. |
| Uso de ICP-Brasil para emissores | Pode apoiar confianca institucional em chaves de emissores. | Nao substitui por si so o modelo de VC, wallet, status e apresentacao. |

## O que evitar

- Publicar CPF, biometria, documento real ou QR Code real em exemplos.
- Gravar identificadores pessoais em blockchain publica.
- Chamar CIN ou GOV.BR de SSI sem fonte oficial que estabeleca essa equivalencia.
- Tratar bCPF ou bCNPJ como fato estabelecido sem documento primario.
- Confundir assinatura eletronica de documento com credencial verificavel portavel.

## Linha de pesquisa recomendada

1. Mapear quais atributos podem ser provados sem expor o identificador original.
2. Definir emissores autorizados para cada credencial.
3. Definir regras de confianca e revogacao.
4. Criar exemplos sinteticos sem dados pessoais.
5. Avaliar aderencia a LGPD, especialmente minimizacao, finalidade e direitos do titular.
6. Validar se o fluxo complementa GOV.BR/CIN/ICP-Brasil ou se cria uma sobreposicao desnecessaria.
