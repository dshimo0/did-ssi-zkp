# Proposta de Valor — DID, SSI e ZKP

> Baseada na secao "Proposta" e na direcao tecnica do README, mais os docs de
> arquitetura e casos de uso.

## Para quem

Times tecnicos e pesquisadores que precisam implementar ou avaliar identidade
descentralizada — especialmente no Brasil, onde CIN, GOV.BR e ICP-Brasil ja
formam uma base institucional forte e toda solucao precisa se posicionar
diante dela.

## Problema

- O ecossistema DID/SSI/VC esta espalhado entre especificacoes W3C, OpenID
  Foundation, IETF e material de vendors — dificil separar padrao oficial de
  marketing.
- Materiais sobre o tema ignoram o contexto juridico/institucional brasileiro
  (LGPD, CPF como chave da CIN, certificados ICP-Brasil).
- Exemplos praticos costumam expor dados pessoais realistas ou prometer ZKP
  sem mostrar o formato concreto de uma credencial/apresentacao.

## Solucao

Um laboratorio de referencia onde cada afirmacao aponta para fonte primaria:

1. **Tese clara** — credenciais emitidas por autoridades confiaveis, guardadas
   em wallet do titular, apresentadas com divulgacao minima (modelo
   emissor/titular/verificador do W3C VC 2.0 + OpenID4VCI/VP).
2. **Arquitetura de referencia** — atores, fluxos de emissao e apresentacao,
   registros de status/schema/confianca.
3. **Casos de uso priorizados** — prova de maioridade, diploma verificavel,
   onboarding profissional, representacao empresarial, acesso a servicos.
4. **Exemplos concretos e eticos** — JSONs sinteticos de credenciais e de uma
   apresentacao derivada (+18 sem data de nascimento), sem nenhum dado real.
5. **Contexto brasileiro honesto** — fatos documentados separados de hipoteses;
   recomendacao explicita de complementar (nao substituir) GOV.BR/CIN/ICP-Brasil.

## Diferenciais

- Rastreabilidade total: matriz de fontes (S1–S15 primarias, B1–B7 oficiais BR)
  e regra de contribuicao que obriga marcar hipotese vs fato.
- Privacidade por construcao: minimizacao de dados e proibicao explicita de
  dados pessoais reais nos exemplos.
- Posicionamento pragmatico: `did:web`/`did:key` como escolha de PoC,
  declaradas como tal, nao como decisao definitiva.

## Estado honesto

Fase 0 (base documental) concluida; Fase 1 parcial (2 de 4 credenciais
modeladas); PoC executavel (emissao/verificacao) ainda pendente — ver
[SPEC.md](../SPEC.md).
