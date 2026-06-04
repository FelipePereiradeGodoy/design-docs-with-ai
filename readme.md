# Design Docs com IA

Repositório de referência para documentação técnica e de produto usando abordagens modernas de arquitetura, design de features, ADRs e suporte a geração via prompts/IA.

## Objetivo

Centralizar modelos, exemplos e classificações de documentos técnicos para times de engenharia que usam IA e processos modernos de documentação.

Este repositório reúne:
- Modelos e exemplos de PRD, HLD, FDD, ADR e documentação de pesquisa profunda
- Templates de prompts para geração assistida por IA
- Documentos de análise de arquitetura e dependências
- Comandos e agentes de suporte para geração de diagramas C4, Mermaid e ADRs

## Estrutura do repositório

- `classificacao_geral_de_documentos.md`
  - Guia de classificação de documentos técnicos, com categorias e relevância para produto, arquitetura e operações.

- `PRD/`
  - Documentos de Product Requirements Document (PRD) e prompt de entrevista para gerar PRDs de feature.
  - Exemplo de features: `exemplo-feature-rate-limit.md`, `exemplo-feature-catalogo-ecommerce.md`

- `Design_&_Arquitetura/`
  - `0_High_Level_Document/`
    - `HLD_rate_limiter.md`: design de alto nível para um SDK de rate limiter em Go.
    - `prompt_geracao_HLD.md`: prompt para ajudar na geração de HLDs.
  - `1_Feature_Design_Document/`
    - `FDD_rate_limiter.md`: documento de design de feature para o rate limiter.
    - `prompt_geracao_FDD.md`: prompt para gerar FDDs.
  - `2_Deep_Research/`
    - `DR_rate_limiter.md`: pesquisa aprofundada sobre o mesmo tema.
    - `prompt_geracao_DR_fase1.md` e `prompt_geracao_DR_fase2.md`: prompts para criar a pesquisa em duas fases.
    - `readme.md`: notas de processo para geração de DRs com PDF.
  - `3_diagram_c4/`
    - `command-c4-generate.md`: comando para geração de diagramas C4.
    - `subagent_geracao_c4.md`: subagent de geração de C4.
  - `4_diagram_mermaid/`
    - `command-mermaid-generate.md`: comando para geração de diagramas Mermaid.
    - `subagent_geracao_mermaid.md`: subagent de geração Mermaid.
  - `5_ADR/`
    - Documentos e comandos para geração, análise e associação de ADRs.
    - `agent-adr-generator.md`, `agent-adr-analyzer.md`, `agent-adr-linker.md`
    - `command-adr-generate.md`, `command-adr-identify.md`, `command-adr-link.md`, `command-adr-map.md`
  - `6_project_analizer/`
    - Agentes e comandos para auditoria de dependências e análise arquitetural.
    - `agent-architectural-analyzer.md`, `agent-component-deep-analyzer.md`, `agent-dependency-auditor.md`
    - `command-generate-architectural-report.md`, `command-run-dependency-audit.md`

- `Engineering_Guidelines/`
  - `exemplo_go_dev_guidelines.md`: guia de boas práticas para desenvolvimento Go.
  - `prompt-guilines-generate.md`: prompt para gerar guidelines de engenharia.

## Como usar

1. Leia `classificacao_geral_de_documentos.md` para entender os papéis de cada tipo de documento.
2. Use os arquivos de prompt dentro de cada pasta para gerar ou refinar documentos com IA.
3. Estude os exemplos de `PRD`, `HLD`, `FDD` e `DR` para alinhar o formato e o nível de detalhe desejado.
4. Execute os comandos de geração em `Design_&_Arquitetura/3_diagram_c4`, `4_diagram_mermaid` e `5_ADR` quando precisar criar diagramas ou ADRs automaticamente.
5. Consulte `Engineering_Guidelines/` para regras de estilo e padrões de desenvolvimento já definidos.

## Visão geral do fluxo de documentos

- `PRD` descreve o problema de negócio e requisitos de produto.
- `HLD` apresenta a arquitetura de alto nível e a visão técnica.
- `FDD` detalha a implementação da feature e as decisões de engenharia.
- `DR` aprofunda a pesquisa técnica e validações.
- `ADR` registra decisões arquiteturais importantes para rastreabilidade.

## Notas importantes

- Este repositório é voltado para times que desejam combinar documentação técnica tradicional com geração assistida por IA.
- Há foco em documentos de arquitetura e design de sistemas modernos, com exemplos aplicados a um rate limiter.
- Os arquivos `prompt_*` e `command-*` suportam a criação automatizada de artefatos a partir de prompts e agentes.

## Próximos passos sugeridos

- Expandir com mais exemplos de FDDs, ADRs e diagramas para outros domínios.
- Adicionar templates de PRD específicos para diferentes tipos de produto.
- Integrar um fluxo de CI/CD que valida consistência entre documentos e prompts.
