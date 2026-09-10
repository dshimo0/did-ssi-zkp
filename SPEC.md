# DID, SSI e ZKP — SPEC viva

> Fonte da verdade do projeto. Conteúdo movido de `docs/roadmap.md` para a raiz
> pela padronização do MasterDashboard (2026-08-24) e enriquecido com checkboxes
> e status reais em 2026-08-26.
> Regra do repositório: toda afirmação factual relevante possui fonte primária ou
> está marcada como interpretação/hipótese ([docs/sources.md](docs/sources.md)).

## Fase 0 - Base documental

Entregáveis:

- [x] README reorganizado (proposta, mapa do repositório, direção técnica sugerida).
- [x] Matriz de fontes ([docs/sources.md](docs/sources.md)).
- [x] Arquitetura de referência com atores e fluxos ([docs/architecture.md](docs/architecture.md)).
- [x] Contexto brasileiro separado de hipóteses ([docs/brazil.md](docs/brazil.md)).
- [x] Exemplos sintéticos iniciais ([examples/](examples)).
- [x] Padrões e protocolos recomendados documentados ([docs/standards.md](docs/standards.md)).
- [x] Casos de uso priorizados ([docs/use-cases.md](docs/use-cases.md)).

Critério de pronto: toda afirmação factual relevante possui fonte ou está marcada
como interpretação/hipótese — cumprido nesta fase.

## Fase 1 - Modelo de credenciais

Objetivo: definir os primeiros schemas conceituais.

- [x] Credencial de maioridade ([examples/credentials/age-credential-payload.example.json](examples/credentials/age-credential-payload.example.json)).
- [x] Credencial de diploma ([examples/credentials/education-credential-payload.example.json](examples/credentials/education-credential-payload.example.json)).
- [ ] Credencial de vínculo profissional.
- [ ] Credencial de representação organizacional.

Critérios:

- Cada campo deve ter finalidade clara.
- Campos sensíveis devem ser evitados ou justificados.
- Cada exemplo deve declarar origem sintética.

Fontes: S2, S5, B4.

## Fase 2 - PoC de emissão e verificação

Objetivo: demonstrar o fluxo emissor, wallet e verificador.

- [ ] Emissor de laboratório com `did:web`.
- [ ] Titular com identificador de teste.
- [ ] Verificador com validação de assinatura, schema e validade.
- [ ] Documentação do fluxo.

Fontes: S1, S2, S7, S8, S12.

## Fase 3 - Status e revogação

Objetivo: incluir status de credencial sem expor uso desnecessário.

- [ ] Modelo de status.
- [ ] Política de revogação.
- [ ] Exemplo de credencial revogada ou suspensa.
- [ ] Teste de verificação de status.

Fontes: S5, S2.

## Fase 4 - Disclosure seletivo

Objetivo: reduzir dados revelados em apresentações.

- [x] Prova de maioridade sem data de nascimento — exemplo conceitual
      ([examples/presentations/age-over-18-derived-presentation.example.json](examples/presentations/age-over-18-derived-presentation.example.json);
      `proofValue` deliberadamente placeholder, não é prova criptográfica real).
- [ ] Apresentação de diploma com campos mínimos.
- [ ] Comparativo entre SD-JWT, BBS e AnonCreds para os casos escolhidos.

Fontes: S2, S4, S6, S10.

## Fase 5 - Contexto brasileiro e governança

Objetivo: mapear aderência ao contexto institucional e jurídico brasileiro.

- [x] Mapa de relação com CIN, GOV.BR e ICP-Brasil ([docs/brazil.md](docs/brazil.md), fatos B1–B7 + hipóteses de integração).
- [ ] Matriz LGPD por caso de uso (a linha de pesquisa LGPD está esboçada em `docs/brazil.md`; a matriz por caso de uso ainda não existe).
- [ ] Modelo de registro de confiança.
- [ ] Riscos de correlação e tratamento de identificadores nacionais.

Fontes: B1, B2, B3, B4, B5, B6, B7, S15.

## Backlog

- [ ] Avaliar integração com frameworks como Credo, Veramo, Trinsic, Dock ou Microsoft Entra Verified ID.
- [ ] Criar diagramas C4.
- [ ] Criar exemplos assinados reais em ambiente local.
- [ ] Adicionar testes de validação de JSON Schema.
- [ ] Criar matriz de ameaças.
- [ ] Criar guia de implementação para `did:web`.
