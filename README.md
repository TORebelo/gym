# Gym

Tracking de treino, dieta, objetivos e progresso. Serve como base de conhecimento para AI fitness assistant.

## Perfil

| | |
|---|---|
| Altura | 1.80m |
| Peso atual | 91.0 kg |
| BF estimado | ~20% |
| Foco | Estetica / composicao corporal |
| Joelho | Lesao patela — rehab ativo |

## Ciclo Atual — Cut Verao

| | |
|---|---|
| Objetivo | 91kg → 84-85kg (seco) |
| Periodo | 31 Mar — 29 Jun 2026 (13 semanas) |
| Treino | Push/Pull/Posterior/Upper/Arms+Delts, 4-5x/sem |
| Dieta | Cut carb cycling (~2,244 treino / ~1,831 descanso) |
| Deficit | ~614 kcal/dia |
| Perda esperada | ~0.6 kg/semana |
| Check-in | Domingos, pesagem jejum |

### Calendario

| Sem | Datas | Fase | Peso esperado |
|---|---|---|---|
| 1 | 31 Mar - 6 Abr | Mesociclo 1 | 91.0 |
| 2 | 7-13 Abr | Mesociclo 1 | ~89.5 |
| 3 | 14-20 Abr | Mesociclo 1 | ~89.0 |
| 4 | 21-27 Abr | Mesociclo 1 | ~88.4 |
| **5** | **28 Abr - 4 Mai** | **DELOAD** | **~87.8** |
| 6 | 5-11 Mai | Mesociclo 2 | ~87.2 |
| 7 | 12-18 Mai | Mesociclo 2 | ~86.6 |
| 8 | 19-25 Mai | Mesociclo 2 | ~86.0 |
| 9 | 26 Mai - 1 Jun | Mesociclo 2 | ~85.4 |
| **10** | **2-8 Jun** | **DELOAD** | **~84.8** |
| 11 | 9-15 Jun | Mesociclo 3 | ~84.2 |
| 12 | 16-22 Jun | Mesociclo 3 | ~83.6 |
| 13 | 23-29 Jun | Mesociclo 3 | ~83.0 |

### Dieta Atual

Carb cycling — mais carbs dias treino, mais gordura dias descanso. Proteina ~200g+ constante.

| | Dia Treino (~2,250) | Dia Descanso (~1,830) |
|---|---|---|
| **Almoco** | 150g frango, 100g arroz, 2 ovos, 150g vegetais | 150g frango, 80g arroz, 2 ovos, salada+azeite |
| **Lanche** | 250g iogurte grego, 30g whey, 20g amendoins, 1 maca | 250g iogurte grego, 30g whey, 25g amendoins, frutos vermelhos |
| **Pre-treino** | 2 ovos, 1 banana (ou 3 bolachas arroz) | — |
| **Jantar** | 200g peixe, 200g arroz, 150g vegetais | 200g peixe, 0 arroz, 300g vegetais |
| **Ceia** | 200g iogurte grego, 30g whey, 20g amendoins, creatina | 200g iogurte grego, 30g whey, 25g amendoins, creatina |
| **Totais** | ~2,244kcal · P:237g · C:192g · F:60g | ~1,831kcal · P:219g · C:88g · F:65g |

Media semanal (5T+2D): **~2,126kcal/dia** · deficit **~614kcal/dia** · perda **~0.6kg/sem**

→ Detalhes completos: [`ciclos/atual/dieta.md`](ciclos/atual/dieta.md)

### Split Atual

| Dia | Foco | Exercicios-chave |
|---|---|---|
| **Seg** | Push (Peito+Ombro+Tri) | Supino inclinado barra, supino reto haltere, cable fly, press militar, lateral raises, triceps overhead |
| **Ter** | Pull (Costas+Rear Delt+Bi) | Pull-up/pulldown, remada barra, remada baixa cabo, straight-arm pulldown, reverse pec deck, biceps barra+inclinado |
| **Qua** | Lower (Post Chain+Rehab) | Isometria joelho, extensora rehab, leg press 45°, terra romeno, hip thrust, curl deitado, gemeos |
| **Qui** | Upper (Peito+Costas+Delts) | Supino reto barra, remada haltere, dips, lat pulldown, lateral raises, face pulls |
| **Sex** | Arms+Delts (skippable) | Lateral raises, upright row, reverse pec deck, curl EZ, skull crusher, hammer curl, triceps overhead |

RPE 7-8 · Cardio: stairmaster 15min pos-treino · Deload sem 5 e 10

→ Detalhes completos: [`ciclos/atual/treino.md`](ciclos/atual/treino.md)

### Pesagens

| Data | Peso (kg) | Sem | Nota |
|---|---|---|---|
| 30 Mar | 91.0 | 0 | Baseline (pre-ciclo) |

## Estrutura

```
gym/
├── perfil.md              # dados estaveis, saude, suplementos
├── prs.md                 # tracker de cargas compostos
├── ciclos/
│   ├── atual/
│   │   ├── objetivo.md    # meta, calendario, metricas
│   │   ├── treino.md      # split completo
│   │   ├── dieta.md       # plano alimentar, macros, rotacao peixe
│   │   └── checkins/      # check-ins semanais (domingos)
│   └── arquivo/           # ciclos passados com retrospetiva
```
