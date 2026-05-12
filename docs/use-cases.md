# Casos de Uso

Todos os casos abaixo sao propostas de aplicacao. As fontes indicam origem dos conceitos e do contexto institucional, nao aprovacao oficial para implementacao.

## Priorizacao

| Caso | Objetivo | Tecnica de privacidade | Fontes |
| --- | --- | --- | --- |
| Prova de maioridade | Provar que uma pessoa atende a uma idade minima sem revelar data de nascimento. | Credencial derivada, disclosure seletivo ou ZKP. | S2, S6, S10 |
| Diploma verificavel | Provar formacao academica sem expor todo o historico. | Apresentacao seletiva de instituicao, curso e status. | S2, S8 |
| Onboarding profissional | Verificar vinculo, cargo ou certificacao para acesso corporativo. | Claims minimos e validade curta. | S2, S7, S8 |
| Representacao empresarial | Provar que uma pessoa representa uma organizacao. | Credencial organizacional com revogacao rapida. | S2, S5 |
| Acesso a servicos | Provar atributo necessario sem compartilhar documento completo. | Minimizacao e proposito explicito. | S2, B4 |

## Prova de maioridade

Problema: muitos verificadores precisam saber se uma pessoa atende a um limite de idade, mas nao precisam da data de nascimento.

Proposta: emitir uma credencial com data de nascimento ou atributo derivavel e permitir uma apresentacao que revele apenas `ageOver18: true` ou equivalente.

Dados de exemplo: sinteticos. Nenhum dado real deve ser usado.

Fontes: W3C VC Data Model v2.0 descreve ZKP e credenciais derivadas; BBS e AnonCreds sao alternativas tecnicas para disclosure seletivo e unlinkability. Ver S2, S6 e S10.

## Diploma verificavel

Problema: verificadores podem precisar confirmar uma titulacao sem receber historico completo, documentos anexos ou dados sensiveis.

Proposta: instituicao educacional emite uma VC de diploma. O titular apresenta apenas curso, grau, instituicao emissora e status de validade.

Dados de exemplo: sinteticos, inspirados em exemplos educacionais do W3C VC Data Model v2.0.

Fontes: S2 e S8.

## Onboarding profissional

Problema: empresas precisam validar certificacoes, vinculo anterior ou autorizacoes sem criar processos manuais e duplicacao de documentos.

Proposta: emissores confiaveis fornecem credenciais de certificacao ou vinculo. A empresa verifica assinatura, status, schema e politica de confianca.

Dados de exemplo: sinteticos.

Fontes: S2, S5, S7 e S8.

## Representacao empresarial

Problema: uma pessoa precisa provar que pode agir em nome de uma organizacao sem expor documentos societarios completos.

Proposta: emitir credencial de representante com escopo, validade curta e revogacao. A apresentacao deve revelar apenas organizacao, papel, poderes aplicaveis e validade.

Dados de exemplo: sinteticos. Para CNPJ ou dados empresariais reais, usar apenas fontes oficiais e dados publicos, com referencia explicita.

Fontes: S2, S5 e B4.

## Acesso a servicos publicos ou privados

Problema: servicos costumam pedir copia de documentos quando precisam apenas de um atributo.

Proposta: usar credenciais verificaveis e apresentacoes seletivas para reduzir compartilhamento de dados. Exemplo: residente em determinada jurisdicao, conta GOV.BR em certo nivel, credencial profissional valida ou documento verificado.

Esta e uma hipotese de integracao. GOV.BR, CIN e ICP-Brasil sao fontes de contexto institucional, nao uma declaracao de que essas plataformas suportam DID/SSI/VC conforme esta proposta.

Fontes: B1, B2, B3, B4, S2 e S8.
