# Como usar este repositorio

Laboratorio de referencia para identidade descentralizada (DID), credenciais
verificaveis (SSI/VC) e provas de conhecimento zero (ZKP), com foco no contexto
brasileiro. E um repositorio documental: nao ha software para instalar.

## Ordem de leitura sugerida

1. [README.md](../README.md) — proposta, tese central e mapa do repositorio.
2. [SPEC.md](../SPEC.md) — status atual das fases (fonte da verdade).
3. [architecture.md](architecture.md) — arquitetura de referencia: atores e fluxos de emissao/apresentacao.
4. [standards.md](standards.md) — padroes e protocolos recomendados (W3C VC, OpenID4VCI/VP, did:web/did:key).
5. [use-cases.md](use-cases.md) — casos de uso priorizados (maioridade, diploma, onboarding profissional, representacao empresarial).
6. [brazil.md](brazil.md) — contexto CIN, GOV.BR, ICP-Brasil e LGPD, separando fatos de hipoteses.
7. [sources.md](sources.md) — matriz de fontes primarias citadas em todo o repositorio.

## Inspecionar os exemplos

Os exemplos sao sinteticos e conceituais (sem dados pessoais reais, sem
assinatura valida):

```bash
# Ler um exemplo de credencial
cat examples/credentials/age-credential-payload.example.json

# Validar a sintaxe JSON dos exemplos
python -m json.tool examples/credentials/age-credential-payload.example.json > /dev/null && echo OK
python -m json.tool examples/credentials/education-credential-payload.example.json > /dev/null && echo OK
python -m json.tool examples/presentations/age-over-18-derived-presentation.example.json > /dev/null && echo OK
```

O `proofValue` do exemplo de apresentacao derivada (+18) e deliberadamente um
placeholder — nao e prova criptografica real.

## Contribuir

Leia [CONTRIBUTING.md](../CONTRIBUTING.md). Regras essenciais:

- Toda afirmacao factual aponta para fonte primaria (W3C, OpenID Foundation,
  IETF, Planalto/GOV.BR etc.), registrada em `docs/sources.md` quando nova.
- Hipoteses e interpretacoes devem estar marcadas como tal.
- Exemplos usam apenas dados sinteticos: nada de CPF, RG, CIN, QR Code real,
  biometria ou nome real.

## O que este repositorio NAO e

- Nao e uma implementacao de wallet/emissor/verificador (isso e a Fase 2 do
  [SPEC.md](../SPEC.md), ainda pendente).
- Nenhum arquivo aqui serve como credencial valida em producao.
