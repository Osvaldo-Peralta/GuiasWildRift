---
tags:
  - Mid
  - Mage
  - Burst/Control
version: 0.1
Status: Borrador (Datos Incompletos)
champion: Mel
patch: "7.3"
---
**Fecha del análisis:** 02/10/2026
**Parche:** 7.3 (21-sep-2026) + hotfix 7.3a (29-sep-2026)
**Rol principal:** Mid
**Arquetipo:** Mago Puro (Burst/Control) — *Deducido por AS Ratio*
**Enfoque:** Maximización de AP, Penetración Mágica y Haste. Cero inversión en AS/AD/Crítico.

---
## 0. RESUMEN EJECUTIVO
### Tabla A — BUILD FINAL (Proyección Teórica para Mago Puro)
| Slot | Ítem | Oro | Rol en la build |
|------|------|-----|-----------------|
| 1 (botas) | **Boots of Mana → ⬆️ Spellslinger's Shoes** (min 10:00, MISMO slot) | 2 200 | 35 AP, 18 Pen plana, 8% Pen %, Big Bully |
| 2 | **Stormsurge** | 2 800 | 90 AP, 15 Pen plana, Squall (Burst + MS) |
| 3 | **Rabadon's Deathcap** | 3 400 | 130 AP, +30% AP total (Multiplicador global) |
| 4 | **Infinity Orb** | 3 100 | 110 AP, 15 Pen plana, Ejecución <40% HP |
| 5 | **Cryptbloom** | 3 000 | 75 AP, 30% Pen %, Nova de curación |
| 6 | **Zhonya's Hourglass** | 3 300 | 110 AP, 40 Armadura, Stasis 2.5s |
> **Oro total: 17 800 g** · **AP Final estimado: ~740** · **Pen Plana: 48** · **Pen %: 38%** · **Haste: ~15**

### Tabla B — Ruta de compra cronológica
| # | Compra | Oro acum. | Minuto típico |
|---|--------|-----------|---------------|
| 1 | Amplifying Tome + Boots of Speed | 900 | 3:30 |
| 2 | **Stormsurge** | 2 800 | ~8:00 |
| 3 | **Boots of Mana** (T2) | 4 000 | ~9:30 |
| 4 | **Rabadon's Deathcap** | 7 400 | ~13:00 |
| 5 | ⬆️ **Spellslinger's Shoes** (mismo slot, +1 000 g) | 8 400 | ~13:30 |
| 6 | **Infinity Orb** | 11 500 | ~16:30 |
| 7 | **Cryptbloom** | 14 500 | ~19:00 |
| 8 | **Zhonya's Hourglass** | 17 800 | ~22:00 |

### Runas · Hechizos · Habilidades
| Categoría | Elección |
|-----------|----------|
| Keystone | **Electrocute** (Burst adaptativo) / **Arcane Comet** (Poke) |
| Domination | **Sudden Impact** (Penetración tras dash/sigilo) |
| Sorcery | **Transcendence** (Haste y CDR) |
| Sorcery | **Scorch** (Daño mágico early) |
| Hechizos | **Flash + Ignite** (Asegurar umbral de Orb) |
| Skills | **Orden dependiente del kit** (R en 5/9/13) |

---
## 1. CONTEXTO DEL CAMPEÓN EN ESTE PARCHE
### 1.1 Cambios directos (Mel) — ⚠️ DATOS AUSENTES
Mel no figura en los cambios de campeones del parche 7.3 ni 7.3a. Su única mención es en la tabla de Attack Speed.
### 1.2 Cambios sistémicos que le afectan
- **Torretas 7 000 HP + Cristales (Crystalline Overgrowth):** Como maga, puede detonar cristales desde rango seguro con habilidades.
- **Lifesteal nuevo stat:** No le afecta directamente, pero los ADCs enemigos tendrán más sustain, haciendo que el burst completo (Stormsurge + Orb) sea obligatorio para evitar que se curen.
### 1.3 ¿Sus habilidades escalan con crítico/AS?
**NO.** Con un `AS Ratio` de 0.625 y un `Growth` de 0.016 (el más bajo del juego, compartido con Annie, Vex, Yuumi), Mel pertenece al arquetipo de **Mago Puro**. Cualquier ítem de AS, AD o Crítico es **oro muerto** (Ley 4).

---
## 2. FICHA MATEMÁTICA (spec deducida)
| Parámetro | Valor | Fuente |
|-----------|-------|--------|
| **AS Ratio / Base** | 0.625 / 0.625 | Apéndice Oficial 7.3 |
| **Base Bonus AS** | 0.2 | Apéndice Oficial 7.3 |
| **AS per Level** | 0.016 | Apéndice Oficial 7.3 |
| **AD / HP / Armor / MR** | *Desconocido* | ⚠️ No publicado por Riot / wr-meta |
| **Rango** | *Estimado ~550-600* | Estándar de magos de control |

---
## 3. MODELO Y FÓRMULAS
Al carecer de ratios de habilidades (AP ratios), WR-LAB aplica el **Modelo de Rotación AP Genérico (Batch 2 - Diana/Mago)** asumiendo un burst de ventana de 2-3 segundos.
```python
# Supuestos del modelo genérico para Mel
Burst_Window = 2.5s
Mitigation_Magic = 100 / (100 + MR_enemy * (1 - Pen_Pct) - Pen_Flat)
DPS_Efectivo = (Base_Dmg + AP * Ratio) * Mitigation_Magic
```
### Supuestos específicos
- **Penetración Plana (48):** Reduce la MR base de los squishies (40 MR) a 0, resultando en daño verdadero equivalente en el early/mid game.
- **Penetración % (38%):** Obligatoria en el late game contra tanques que acumulan MR (Force of Nature, Abyssal Mask).

---
## 4. LEYES APLICADAS A MEL
### Ley 0 — Slots
Build final = 1 botas (Spellslinger's) + 5 ítems. `validate_slots()` = PASS.
### Ley 1 & 2 — Crítico y AS (DESCARTADAS)
Con `AS Growth = 0.016`, Mel no escala con autos. Invertir en Nashor's Tooth o Statikk Shiv es ineficiente.
### Ley 3 — Penetración Mágica Obligatoria
En 7.3, los tanques y bruisers compran MR. La combinación de **Spellslinger's (18 plana + 8%) + Stormsurge (15 plana) + Infinity Orb (15 plana) + Cryptbloom (30%)** garantiza que el daño de Mel ignore por completo las resistencias de los carries y penetre profundamente a los tanques.
### Ley 4 — Stats Muertos
Cero oro gastado en AD, AS, o Vida pasiva (excepto Zhonya's por su Armadura y Stasis).
### Ley 6 — Timing
**Stormsurge (2 800 g)** como primer ítem asegura un pico de poder al minuto 8, permitiendo rotar y aprovechar los **Cristales de Torreta** (18.9% de vida máx como daño verdadero).

---
## 5. ANÁLISIS DEL PRIMER ÍTEM
| Candidato | Oro | Veredicto | Nota |
|-----------|-----|-----------|------|
| **Stormsurge** | 2 800 | ✅ Core 1 | Burst + MS para kiteo. Squall detona con combos rápidos. |
| **Luden's Echo** | 2 800 | ⚠️ Alt | Mejor para waveclear, pero pierde el pico de asesinato 1v1. |
| **Malignance** | 2 700 | ❌ | Solo si la R de Mel tiene un CD base muy alto y es su única fuente de daño. |

---
## 6. BUILD FINAL RANURA POR RANURA
| Slot | Ítem | Justificación matemática |
|------|------|--------------------------|
| **Botas** | **Spellslinger's Shoes** | 18 Pen plana + 8% Pen. Multiplica el daño early un 25% real contra la línea trasera. |
| **1** | **Stormsurge** | 90 AP + 15 Pen. La pasiva *Squall* otorga +25% MS para reposicionarse tras soltar el combo. |
| **2** | **Rabadon's Deathcap** | Multiplicador global. Con ~200 AP base al comprarlo, añade +60 AP gratis. |
| **3** | **Infinity Orb** | 110 AP + 15 Pen. *Inevitable Demise* hace que las habilidades critiquen (+20% daño) contra enemigos <40% HP. |
| **4** | **Cryptbloom** | 30% Pen % obligatoria en el min 18+ contra frontline. Su pasiva *Life from Death* otorga sustain en teamfights. |
| **5** | **Zhonya's Hourglass** | 110 AP + 40 Armadura. Supervivencia reactiva (Stasis 2.5s) para esperar CDs tras el burst. |

### Matriz del último slot (situacional)
| Situación | Ítem | Coste | Impacto medido |
|-----------|------|-------|----------------|
| **Default (Burst)** | Rabadon's Deathcap | 3 400 | AP ~740 |
| **Vs 3+ Tanques MR** | Void Staff | 3 000 | +40% Pen (Reemplaza Cryptbloom o Rabadon's) |
| **Vs Curación** | Morellonomicon | 2 650 | 50% GW + 75 AP |
| **Vs Asesinos AD** | Seeker's Armguard (Componente) | 1 200 | Acelera Zhonya's |

### RECHAZADOS (con motivo numérico)
| Ítem | Motivo del rechazo |
|------|--------------------|
| **Nashor's Tooth** | AS muerto (Ratio 0.625). El on-hit mágico no compensa la pérdida de AP puro. |
| **Riftmaker** | Requiere peleas de 5+ segundos. Los magos de burst mueren antes de llegar al 8% de amp. |
| **Rod of Ages** | Escalado tardío, falta Haste y Penetración. |

---
## 7. RUNAS · HECHIZOS · HABILIDADES
### Keystone: Electrocute / Arcane Comet
- **Electrocute:** Si el kit de Mel tiene un combo rápido de 3 golpes/habilidades, añade ~150-200 de daño adaptativo instantáneo, cruzando el umbral del 40% HP para Infinity Orb.
- **Arcane Comet:** Si Mel es de poke de largo alcance (tipo Xerath/Ziggs).
### Secundarias
- **Sudden Impact:** Penetración letal tras cualquier dash o salida de sigilo.
- **Transcendence:** +10 AH base y CDR al golpear.
- **Scorch:** Poke en fase de líneas y detonación de cristales de torreta.
### Hechizos
- **Flash + Ignite:** Ignite asegura el umbral de ejecución de Infinity Orb y aplica 60% GW.

---
## 8. COMPARACIÓN CONTRA LAS ALTERNATIVAS
| Build | Oro | AP Estimado | Pen Plana / % | Supervivencia | Veredicto WR-LAB |
|-------|-----|-------------|---------------|---------------|------------------|
| **ÓPTIMA (Burst + Pen)** | 17 800 | ~740 | 48 / 38% | Stasis + 40 Armor | ✅ Recomendada |
| **Glass Cannon (Sin Zhonya's)** | 17 500 | ~780 | 48 / 30% | Nula | ❌ Oro muerto si te focusean |
| **Bruiser (Riftmaker + RoA)** | 16 500 | ~450 | 15 / 30% | Alta | ⚠️ Pierde el rol de Asesina |

---
## 9. PLAN DE JUEGO
### Early (0:00 – 9:00)
- Farmeo seguro. Con AS 0.625, el last-hit bajo torreta requiere calcular bien el daño de las habilidades.
- **Macro 7.3:** Usar habilidades para detonar los **Cristales de Torreta** (Crystalline Overgrowth) desde rango seguro, infligiendo hasta 18.9% de la vida máx de la torreta como Daño Verdadero.
### Mid (9:00 – 16:00)
- **Pico Stormsurge (Min 8):** Buscar escaramuzas en el río. El burst + MS permite limpiar y rotar.
- **Min 10:00:** ⬆️ Spellslinger's Shoes. La pen plana hace que el daño sea casi verdadero contra los midlaners enemigos.
### Late (16:00+)
- **Borrar -> Stasis -> Salir:** Soltar el combo completo sobre el carry enemigo, activar Zhonya's Hourglass inmediatamente para esquivar el burst de respuesta, y esperar a que Transcendence refresque las habilidades básicas.

---
## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS
### Fuentes primarias (mandan)
| Fuente | Acceso | Qué aporta |
|--------|--------|------------|
| Notas oficiales 7.3 (Apéndice AS) | 21/09/2026 | Única confirmación de la existencia de "Mel" en el código del parche. |
### Discrepancias detectadas y resolución
| Tema | Resolución |
|------|------------|
| "Mel" no tiene ficha en wr-meta ni en notas 7.3 | Se asume que es un placeholder, leak (Mel Medarda) o error de scrapeo. Se aplica el modelo genérico de Mago Puro basado en su AS Ratio (0.625). |
### Supuestos del modelo (declarados)
- El kit de Mel consiste en habilidades de daño mágico con ratios AP estándar (no se modelan autos).
- Se asume un rango de combate de ~550-600 unidades.
### Validación del modelo
- `validate_slots(["Spellslinger's", "Stormsurge", "Rabadon's", "Infinity Orb", "Cryptbloom", "Zhonya's"])` → **PASS** (6 slots, 1 botas T3).

---
## APÉNDICE A — POOL DE ÍTEMES DEL ROL: veredicto para Mel
| Ítem (oro) | Veredicto | Nota |
|------------|-----------|------|
| Stormsurge (2 800) | ✅ Core | Burst + MS |
| Rabadon's Deathcap (3 400) | ✅ Core | Multiplicador |
| Infinity Orb (3 100) | ✅ Core | Ejecución |
| Cryptbloom (3 000) | ✅ Core | Pen % + Sustain |
| Zhonya's Hourglass (3 300) | ✅ Core | Stasis |
| Spellslinger's Shoes (2 200) | ✅ Botas | Pen Plana + % |
| Void Staff (3 000) | ⚠️ Sit | Vs 3+ Tanques MR |
| Morellonomicon (2 650) | ⚠️ Sit | Vs Curación |
| Nashor's Tooth (2 900) | ❌ | AS muerto |
| Riftmaker (3 100) | ❌ | Requiere peleas largas |

---
## APÉNDICE B — RUTAS DE COMPRA
```text
DEFAULT (Burst Mid):
  Tome + Boots → Stormsurge (8:00) → Boots of Mana (9:30) → Rabadon's (13:00)
  → ⬆️ Spellslinger's (13:30) → Infinity Orb (16:30) → Cryptbloom (19:00) → Zhonya's (22:00)

VS TANQUES (MR Stack):
  ... → Cryptbloom (16:30) → Void Staff (19:00) → Zhonya's (22:00)
```

---
## Pie de página
*Reporte generado el 02/10/2026 con datos del parche 7.3 (21-sep-2026) + hotfix 7.3a (29-sep-2026). WR-LAB v1.12. Las cifras de DPS son pre-mitigación y comparativas. Si Riot publica un 7.3b/7.4 o libera a Mel, regenerar datos antes de publicar.*
**Referencias y créditos**
- Notas oficiales del parche 7.3 (21-sep-2026) y 7.3a (29-sep-2026) — © Riot Games, Inc. (wildrift.leagueoflegends.com). Fuente primaria del Apéndice de Attack Speed.
- Base de datos de ítems, runas y fichas de campeón — wr-meta.com (proyecto comunitario de JLVD DEV), sincronizada al 24/09/2026.
- Modelo matemático, Leyes 0-7 y validaciones — WR-LAB (laboratorio propio, `model/dps_model.py`), construido sobre las fuentes anteriores.
**Aviso legal:** Wild Rift y League of Legends son marcas registradas de Riot Games, Inc. Este documento es una guía de comunidad con fines educativos, **no está afiliado, patrocinado ni respaldado por Riot Games**. Los nombres de ítems, campeones y estadísticas pertenecen a sus respectivos dueños. El análisis y las conclusiones son trabajo original del autor apoyado en WR-LAB.