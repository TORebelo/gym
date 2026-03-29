# Design: Sistema de Tracking Ginasio/Dieta/Lifestyle

## Contexto
Pasta para servir como base de conhecimento para um AI fitness assistant. O utilizador e um lifter intermedio (1.80m, ~90kg) focado em estetica/composicao corporal, com lesao no joelho (patela) em reabilitacao.

## Decisoes de Design

### Formato: Markdown puro
- Legivel para o utilizador, perfeito para LLMs
- Sem necessidade de TSON/JSON/YAML — o volume de dados nao justifica formatos otimizados para tokens
- Frontmatter YAML descartado em favor de markdown simples por ser mais direto

### Organizacao: Por ciclo/fase
Escolhida sobre "por tipo de conteudo" e "flat/minimalista" porque:
- Treino, dieta e objetivo mudam juntos quando muda a fase
- Historico limpo — cada ciclo passado e uma capsula completa
- AI consegue isolar contexto (atual/ vs arquivo/)
- Retrospetiva obriga reflexao e da ao AI contexto para nao repetir erros

### Estrutura de pastas
```
gym/
├── perfil.md              # dados estaveis (altura, saude, suplementos)
├── prs.md                 # tracker de cargas compostos principais
├── ciclos/
│   ├── atual/
│   │   ├── objetivo.md    # meta, metricas, horizonte, estrategia
│   │   ├── treino.md      # split completo, volume, progressao
│   │   ├── dieta.md       # plano alimentar, macros, regras
│   │   └── checkins/
│   │       ├── template.md
│   │       └── YYYY-MM-DD.md
│   └── arquivo/
│       └── YYYY-MM_YYYY-MM_nome-fase/
│           ├── objetivo.md
│           ├── treino.md
│           ├── dieta.md
│           ├── checkins/
│           └── retrospetiva.md
```

### Convencoes
- Nome arquivo ciclo: `YYYY-MM_YYYY-MM_nome-da-fase` (ex: `2026-04_2026-06_cut-verao`)
- Check-ins: `YYYY-MM-DD.md` (data da segunda-feira da semana)
- PRs: tabela unica no root, atualizada nos check-ins

### Fluxo de mudanca de ciclo
1. Escrever `retrospetiva.md` (o que funcionou, o que falhou, licoes)
2. Mover `atual/` para `arquivo/` com nome correto
3. Criar novo `atual/` com novos planos

## Ciclo Atual: Cut Verao (Abr-Jun 2026)

### Objetivo
90kg → 83-85kg, perder gordura mantendo massa muscular

### Treino: Push/Pull/Posterior Chain/Upper/Arms+Delts
- 5x semana (sexta skippable → 4x)
- Volume reduzido ~1/3 vs bulk (fase cut)
- RPE 7-8, manter cargas, deload cada 3-4 semanas
- Prioridades V-taper: side delts alta frequencia (3x), lats, upper chest
- Lower: posterior chain focus + rehab quads (isometria, extensora low weight, prensa pes altos)

### Dieta: Cut com Carb Cycling
- Dias treino: ~2400kcal (carbs backloaded pos-treino)
- Dias descanso: ~1800kcal (low carb)
- Proteina: ~2.0-2.4g/kg constante
- Deficit medio: ~500kcal/dia
- Ajustes automaticos baseados em taxa de perda semanal

### Check-in semanal
Peso + treino (aderencia, cargas, energia) + dieta (aderencia, desvios) + lifestyle (sono, stress, alcool) + notas livres

## Decisoes baseadas em evidencia
- Split redesenhado: cada upper day tem push+pull para garantir 2x/semana (vs anterior que era push day/pull day = 1x/semana)
- Side delts priorizados: 12-18 sets/semana em 3-4 sessoes (musculo #1 para V-taper)
- Proteina redistribuida: ~45-55g por refeicao em vez de 95g almoco + 2.5g pre-treino
- Pre-treino: ovos + banana (proteina + glucose) em vez de maca + leite condensado (frutose + gordura)
- Carbs backloaded: sedentario de dia, treina a noite — concentrar carbs pos-treino
- Cut escolhido sobre recomp: 3 meses ate ao verao, recomp seria demasiado lenta para resultados visiveis
