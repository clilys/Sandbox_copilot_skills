---
name: auditoria-design-lili-teste
description: >-
  Use quando o pedido for para auditar, revisar ou dar feedback estruturado sobre uma tela,
  fluxo ou protótipo de design. Aciona em pedidos como "audita essa tela", "revisa esse design",
  "o que acha desse fluxo", "critique de design", "audit this screen", "review this flow",
  ou quando um link do Figma/screenshot for compartilhado pedindo avaliação.
---

# Auditoria de Design

Skill de teste (Lili) para gerar feedback estruturado de design em telas, fluxos ou protótipos,
cobrindo usabilidade, hierarquia visual, consistência com o design system, acessibilidade e copy/UX writing.

## O que eu preciso antes de rodar a auditoria

- **O design**: link do Figma, screenshot ou descrição detalhada da tela/fluxo
- **Contexto**: o que é, para quem é, em que estágio (exploração, refinamento, pronto pra dev)
- **Foco (opcional)**: ex. "foca só no fluxo de onboarding" ou "foca em copy"

Se alguma dessas informações não vier no pedido, pergunte apenas o que for essencial antes de
rodar a auditoria completa. Não assuma contexto de produto que não foi dito.

## Framework de auditoria

### 1. Primeira impressão (2 segundos)
- O que chama atenção primeiro? Isso está certo?
- O propósito da tela fica claro de imediato?

### 2. Usabilidade
- O usuário consegue completar o objetivo sem fricção?
- A navegação é intuitiva?
- Existem passos desnecessários ou redundantes?

### 3. Hierarquia visual
- Existe uma ordem de leitura clara?
- Os elementos certos estão em destaque?
- Espaçamento e tipografia reforçam a hierarquia?

### 4. Consistência com o design system
- Segue os tokens definidos (cor, espaçamento, tipografia)?
- Existem valores hardcoded que deveriam ser tokens?
- Componentes semelhantes se comportam de forma semelhante?

### 5. Acessibilidade (WCAG 2.1 AA)
- Contraste de cor nos textos principais
- Tamanho de área de toque (mínimo 44x44px)
- Legibilidade de texto (tamanho, altura de linha)
- Textos alternativos em imagens e ícones funcionais

### 6. Copy e UX Writing
- O texto está claro, direto e sem ambiguidade?
- Tom de voz consistente com o resto do produto?
- Labels, CTAs e mensagens de erro seguem o padrão do produto?
- Existe texto genérico que poderia ser mais específico ao contexto?

## Como dar o feedback

- Seja específico: "o CTA compete visualmente com a navegação", não "o layout está confuso"
- Explique o porquê: conecte o achado a um princípio de UX ou necessidade do usuário
- Sempre proponha uma alternativa, não só aponte o problema
- Reconheça o que funciona bem, não só os problemas
- Calibre pelo estágio: exploração inicial recebe feedback diferente de tela pronta pra dev

## Formato de saída

```markdown
## Auditoria de Design: [Nome da tela/fluxo]

### Resumo
[1-2 frases com a impressão geral e a maior oportunidade]

### Usabilidade
| Achado | Severidade | Recomendação |
|--------|-----------|--------------|
| [Problema] | Crítico / Moderado / Menor | [Correção] |

### Hierarquia Visual
- **O que chama atenção primeiro**: [elemento] — [está correto?]
- **Fluxo de leitura**: [como o olho percorre o layout]

### Consistência com Design System
| Elemento | Problema | Recomendação |
|----------|----------|--------------|
| [tipografia/espaçamento/cor] | [inconsistência] | [correção] |

### Acessibilidade
- **Contraste de cor**: [passa/falha nos textos principais]
- **Área de toque**: [adequada?]
- **Legibilidade**: [tamanho de fonte, altura de linha]

### Copy e UX Writing
| Trecho | Problema | Sugestão |
|--------|----------|----------|
| [texto atual] | [o que não funciona] | [reescrita sugerida] |

### O que funciona bem
- [Observação positiva 1]
- [Observação positiva 2]

### Recomendações prioritárias
1. [Mudança de maior impacto] — [por quê e como]
2. [Segunda prioridade] — [por quê e como]
3. [Terceira prioridade] — [por quê e como]
```

## Se houver conectores disponíveis

Se o Figma estiver conectado:
- Puxar o design diretamente do Figma e inspecionar componentes, tokens e camadas
- Comparar contra o design system existente para checar consistência

## Notas de origem

Skill adaptada a partir de `design-critique` (catálogo interno de skills de design), com adição
do bloco de Copy e UX Writing. Versão de teste para validação de fluxo Copilot + GitHub antes do
workshop AirOps.

