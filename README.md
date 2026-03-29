# Gym

Tracking de treino, dieta, objetivos e progresso. Serve como base de conhecimento para AI fitness assistant.

## Perfil

| | |
|---|---|
| Altura | 1.80m |
| Peso atual | 90.0 kg |
| BF estimado | ~20% |
| Foco | Estetica / composicao corporal |
| Joelho | Lesao patela — rehab ativo |

## Ciclo Atual — Cut Verao

| | |
|---|---|
| Objetivo | 90kg → 83-85kg (seco) |
| Periodo | 31 Mar — 29 Jun 2026 (13 semanas) |
| Treino | Push/Pull/Posterior/Upper/Arms+Delts, 4-5x/sem |
| Dieta | Cut carb cycling (~2,250 treino / ~2,040 descanso) |
| Deficit | ~550-620 kcal/dia |
| Perda esperada | ~0.55 kg/semana |
| Check-in | Domingos, pesagem jejum |

### Calendario

| Sem | Datas | Fase | Peso esperado |
|---|---|---|---|
| 1 | 31 Mar - 6 Abr | Mesociclo 1 | 90.0 |
| 2 | 7-13 Abr | Mesociclo 1 | ~88.5 |
| 3 | 14-20 Abr | Mesociclo 1 | ~88.0 |
| 4 | 21-27 Abr | Mesociclo 1 | ~87.5 |
| **5** | **28 Abr - 4 Mai** | **DELOAD** | **~87.0** |
| 6 | 5-11 Mai | Mesociclo 2 | ~86.5 |
| 7 | 12-18 Mai | Mesociclo 2 | ~86.0 |
| 8 | 19-25 Mai | Mesociclo 2 | ~85.5 |
| 9 | 26 Mai - 1 Jun | Mesociclo 2 | ~85.0 |
| **10** | **2-8 Jun** | **DELOAD** | **~84.5** |
| 11 | 9-15 Jun | Mesociclo 3 | ~84.0 |
| 12 | 16-22 Jun | Mesociclo 3 | ~83.5 |
| 13 | 23-29 Jun | Mesociclo 3 | ~83.0 |

### Pesagens

| Data | Peso (kg) | Sem | Nota |
|---|---|---|---|
| 31 Mar | — | 0 | Inicio ciclo |

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
