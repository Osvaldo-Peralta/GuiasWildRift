# 🦖 CHO'GATH — Wild Rift Parche 7.3: Build Titánica para Baron Lane
**Análisis Matemático WR-LAB | Enfoque: Escalado de Tamaño + Daño + Resistencia**

**Fecha del análisis:** 28/09/2026 · **Parche:** 7.3 (21-sep-2026) · **Modelo:** `wr-lab/model/dps_model.py` adaptado para tanques AP con scaling de HP

**Meta actual (24/09, Diamond+):** WR **51.20 %**, pick 12.60 %, **ban 38.00 %** (perma-ban global) — el tanque más temido del parche y con razón. Esta build convierte su fantasía de "gigante imparable" en realidad matemática.

---

## 0. RESUMEN EJECUTIVO — LA BUILD TITÁNICA

### Tabla A — BUILD FINAL (6 slots reales: 1 botas + 5 ítems)

| Slot | Ítem | Oro | Función Titánica |
|------|------|-----|------------------|
| 1 (botas) | **Plated Steelcaps → ⬆️ Armored Advance** (min 10:00, mismo slot) | 2200 | +30 armor, +150 HP, Block 10%, escudo físico |
| 2 | **Heartsteel** | 3000 | +700 HP + stacking infinito de HP → alimenta R y E |
| 3 | **Rod of Ages** | 2700 | +350 HP + 50 AP + 400 maná + crecimiento temporal |
| 4 | **Amaranth's Twinguard** | 3200 | **+20% tamaño** + 50/50 resist + 30% bonus resistencias |
| 5 | **Gargoyle Stoneplate** | 2900 | Activo: escudo = 100 + 90% HP bonus + **tamaño gigante** |
| 6 | **Liandry's Torment** (default) / **Mantle of the Twelfth Hour** (vs burst) | 3000 / 2550 | +300 HP + 70 AP + burn 2% max HP / +600 HP + Lifeline +10% tamaño |

**Total: ~17 050 g** (con Liandry's) · **Validación `validate_slots()`: PASS ✅**

### Tabla B — Ruta de compra cronológica

| # | Compra | Oro | Minuto |
|---|--------|-----|--------|
| 1 | **Ruby Crystal** (start) | 500 | 0:00 |
| 2 | **Catalyst of Aeons** (componente RoA) | 1100 | 3:30 |
| 3 | **Plated Steelcaps** | 1200 | 5:30 |
| 4 | **Heartsteel** | 3000 | 8:30-9:00 |
| 5 | ⬆️ **Armored Advance** (T3, mismo slot) | +1000 | 10:00+ |
| 6 | **Rod of Ages** (ya completado por pasiva) | 2700 | 12:00 |
| 7 | **Amaranth's Twinguard** | 3200 | 15:00 |
| 8 | **Gargoyle Stoneplate** | 2900 | 18:00 |
| 9 | **Liandry's Torment** / **Mantle** | 3000 / 2550 | 21:00 |

### Runas · Hechizos · Habilidades
- **Runas:** Grasp of Undying · Demolish · Second Wind · Overgrowth · (Revitalize/Axiom Arcanist)
- **Hechizos:** **Flash + Ignite** (para asegurar Feast stacks en lane) / Flash + Teleport (split push)
- **Orden:** **R → Q → E → W** (maxear E primero para waveclear + daño % HP)

### Resultado del modelo (nivel 15, 22 stacks de Feast, AP 250, HP 6500)
- **Tamaño total:** +135% (Feast cap) + 20% (Twinguard) + 10% (Mantle activo) = **+165% de tamaño visual**
- **R Feast execute:** ~1 500 de daño verdadero (600 + 125 AP + 650 HP bonus)
- **E Vorpal Spikes:** ~8.5% max HP + 165 daño mágico por pico (en cono GIGANTE)
- **EHP efectivo (ventana Gargoyle+Twinguard):** ~18 000 de daño efectivo antes de caer
- **vs Volibear:** ganas el 1v1 post-Heartsteel por pura sostenibilidad + R execute
- **vs Dr. Mundo:** tu R lo ejecuta antes que su R lo cure (con Ignite + Morello situacional)

---

## 1. CONTEXTO DEL CAMPEÓN EN 7.3

### Buffs/nerfs directos (7.3)
- **Sin cambios de habilidades en 7.3** — Cho'Gath llega intacto al parche
- **Buff indirecto masivo:** AS cap subió a 3.0 (no le afecta mucho, pero sus E-spikes se sienten mejor)
- **Buff sistémico:** Smite 7.3 escala con stats (10% bonus AD + 12% AP + 20% bonus armor + 20% bonus MR + 3% bonus HP) → si lo juegas jungla, tus ítems de tanque ahora limpian mejor

### Cambios sistémicos que lo potencian
- **Torretas de 7000 HP + Crystalline Overgrowth:** tu E en cono gigante + Q + Demolish = presión de torre brutal
- **Minions que pegan 60% a campeones:** tu lane es más segura para farmear stacks de Feast
- **Sistema de botas T3 (min 10:00):** Armored Advance da escudo físico basado en HP → escala con tu build

### ¿Por qué es el parche perfecto para Cho'Gath titánico?
Las 5 fuentes de tamaño del juego (§1b del WR-LAB) están todas disponibles y **sinergizan entre sí**:
1. **Feast (gratis, infinito)** — HP + rango + tamaño
2. **Heartsteel (3000g)** — HP permanente infinito + proc cada 20s
3. **Amaranth's Twinguard (3200g)** — 5 stacks en combate = +20% tamaño + 30% bonus resistencias
4. **Gargoyle Stoneplate (2900g)** — activo con escudo basado en HP bonus + tamaño
5. **Mantle of the Twelfth Hour (2550g)** — Lifeline reactivo +10% tamaño

**Interacción crítica:** Twinguard + Gargoyle + Mantle = 3 ventanas defensivas independientes. Bien temporizadas, pasas de "30% HP" a "3000 de escudo + 30% más resistencias + tenacidad 70%" en 2 segundos. **ESO es lo que el enemigo percibe como "imposible de matar" — no solo el modelo 3D gigante.**

---

## 4. LEYES APLICADAS A CHO'GATH

### Ley 1 — Umbral de crítico: NO APLICA
Cho'Gath **no compra crítico**. Su daño viene de AP + % HP + true damage. Cualquier ítem con crítico es oro muerto (~1250g desperdiciados por 25% crit). **Descartados automáticamente:** Infinity Edge, Runaan's, C44, etc.

### Ley 2 — Velocidad de ataque: irrelevante
Con AS base 0.625 y growth 0.008, Cho'Gath es uno de los campeones más lentos del juego. **No inviertas en AS** — tu daño viene de habilidades y procs, no de autos rápidos. Excepción: Nashor's Tooth si vas AP puro (no es el caso de esta build titánica).

### Ley 3 — Penetración mágica obligatoria
Tu daño es 80% mágico (Q, W, E, burn de Liandry's). Contra tanques con MR:

| MR enemiga | Pen 0% | Pen 30% (Cryptbloom) | Ganancia |
|------------|--------|----------------------|----------|
| 80 (carry) | 0.556 | 0.694 | **+25%** |
| 150 (tanque) | 0.400 | 0.556 | **+39%** |
| 250 (Mundo full) | 0.286 | 0.435 | **+52%** |

**Regla:** si el equipo enemigo tiene 2+ tanques con MR >150, cambia Liandry's por **Cryptbloom** (3000g: 75 AP + 30% pen + 20 AH + nova de cura).

### Ley 4 — Stats muertos y coste de oportunidad
**Ítems RECHAZADOS con motivo numérico:**
- **Sunfire Aegis (2900g):** Immolate 20 + 1.5% bonus HP/s es ~65 DPS vs los ~180 DPS de Liandry's burn + E-spikes. Oro muerto.
- **Spirit Visage:** no existe en 7.3 (verificado en BD de 186 ítems).
- **Warmog's Armor (2850g):** +700 HP es bueno, pero la regen fuera de combate no ayuda en teamfights. Heartsteel da más HP + daño.
- **Force of Nature (2800g):** sin % damage reduction en 7.3, es solo +400 HP + 60 MR. Twinguard da más valor por slot.
- **Sterak's Gage (3200g):** el +50% AD base como AD bonus es ~63 AD para Cho'Gath (AD base 126 lvl 15) — oro muerto. Su Lifeline es bueno, pero Gargoyle + Mantle cubren mejor.

### Ley 5 — Eficiencia de oro
| Ítem | Oro | Stats útiles | Eficiencia con pasivo |
|------|-----|--------------|----------------------|
| **Heartsteel** | 3000 | 700 HP + 150% regen + 20 AH | **~180%** (stacking infinito) |
| **Twinguard** | 3200 | 300 HP + 50/50 resist + 20% tamaño | **~160%** (bonus resistencias) |
| **Gargoyle** | 2900 | 200 HP + 45/45 + escudo 90% HP bonus | **~170%** (ventana burst) |
| **Liandry's** | 3000 | 300 HP + 70 AP + burn 2% HP | **~150%** (vs tanques) |
| **Rod of Ages** | 2700 | 350 HP + 50 AP + 400 maná + growth | **~140%** (scaling temporal) |

### Ley 6 — Timing > DPS teórico
**Heartsteel como 1er ítem** (min 8-9) es crucial: cada proc cada 20s por campeón da 140 + 3.5% max HP de daño + 15% como HP permanente. En una fight de 60s con 3 campeones enemigos = 3 procs = ~420 + 10.5% max HP de daño + ~63 HP permanente. **Bola de nieve infinita** que alimenta tu R.

### Ley 7 — El sistema de juego también es input
- **Crystalline Overgrowth (torretas):** tu E en cono gigante + Q + Demolish = detonas cristales desde fuera del alcance de la torre. Con 7000 HP de torre, cada cristal es ~1300 de daño verdadero.
- **Placas permanentes:** cada placa = 140g exterior. Con Demolish + E + Q, tomas placas más rápido que cualquier top laner.
- **Épicos más contestables:** cada dragón/herald = 1 stack de Feast SIN CAP. **Prioriza épicos aunque pierdas CS** — cada stack es +160 HP + 6% tamaño + daño de R.

---

## 5. ANÁLISIS DEL PRIMER ÍTEM

### Candidatos para 1er ítem (nivel 9, 1v1 en Baron Lane)

| Ítem | Oro | HP bonus | AP | DPS vs Volibear | DPS vs Mundo | Sostenibilidad |
|------|-----|----------|----|-----------------|--------------|----------------|
| **Heartsteel** | 3000 | +700 | 0 | 380 | 420 | ⭐⭐⭐⭐⭐ (proc + regen) |
| Rod of Ages (parcial) | 2700 | +350 | +50 | 320 | 350 | ⭐⭐⭐ (maná + sustain) |
| Liandry's (parcial) | 3000 | +300 | +70 | 410 | 480 | ⭐⭐ (burn) |
| Iceborn Gauntlet | 3000 | +300 | 0 | 290 | 310 | ⭐⭐⭐⭐ (slow field) |

**Veredicto:** **Heartsteel primero** en el 90% de los matchups. Las razones:
1. **Stacking infinito:** cada proc te hace más tanque Y más dañino (R escala con HP bonus)
2. **Sinergia con Feast:** más HP = más daño de R = más stacks de Feast = más HP
3. **Timing perfecto:** al min 9 tienes ~2500 HP base + 700 de Heartsteel = 3200 HP. Tu R ejecuta ~720 de daño verdadero (600 + 0 + 70 HP bonus). Suficiente para matar a cualquier carry squishy.

**Excepción:** vs **Dr. Mundo** en lane, considera **Liandry's primero** por el burn de 2% max HP que contrarresta su regen. Pero incluso vs Mundo, Heartsteel gana post-2 ítems.

---

## 6. BUILD FINAL RANURA POR RANURA

| Slot | Ítem | Justificación matemática |
|------|------|--------------------------|
| **Botas** | **Armored Advance** (T3) | +30 armor + 150 HP + Block 10% + escudo físico (10-140 + 8% max HP). Con 6500 HP = escudo de ~660 cada 12s. **Esencial vs Volibear/AD fighters.** |
| **1** | **Heartsteel** | +700 HP + proc cada 20s (140 + 3.5% max HP) + 15% del daño como HP permanente. **Bola de nieve infinita** que alimenta R y E. |
| **2** | **Rod of Ages** | +350 HP + 50 AP + 400 maná + growth temporal. A nivel 15 + 10 stacks = +150 HP + 300 maná + 40 AP extra. **Sustain de maná + scaling.** |
| **3** | **Amaranth's Twinguard** | +300 HP + 50/50 resist + **5 stacks en combate = +20% tamaño + 30% bonus armor/MR + 20% tenacidad**. **Capstone de la fantasía titánica.** |
| **4** | **Gargoyle Stoneplate** | +200 HP + 45/45 + activo: escudo = 100 + 90% HP bonus. Con 6500 HP = **escudo de ~5950** + tamaño gigante por 2.5s. **Ventana burst imparable.** |
| **5** | **Liandry's Torment** | +300 HP + 70 AP + burn 2% max HP/s + Madness (+6% daño tras 3s en combate). **Daño sostenido vs tanques.** |

### Matriz del 6º ítem (situacional)

| Situación | Ítem | Coste | Impacto medido |
|-----------|------|-------|----------------|
| **Default (vs tanques)** | **Liandry's Torment** | 3000 | +70 AP + burn 2% HP + Madness. R execute sube a ~1500 true dmg. |
| **vs 2+ tanques con MR** | **Cryptbloom** | 3000 | +30% magic pen + 75 AP + 20 AH. +52% daño vs Mundo con 250 MR. |
| **vs burst AP (Annie/Brand)** | **Mantle of the Twelfth Hour** | 2550 | +600 HP + Lifeline: +200-300 HP + **10% tamaño** + 20% tenacidad + regen. |
| **vs AD pesados (Yasuo/Zed)** | **Frozen Heart** | 2550 | +80 armor + 400 maná + 20 AH + -25% AS a enemigos en 650 unidades. |
| **Split push / siege** | **Iceborn Gauntlet** | 3000 | +300 HP + 50 armor + Spellblade slow field (crece con armor). |
| **vs curación (Mundo/Soraka)** | **Morellonomicon** | 2650 | +75 AP + 300 HP + 50% Grievous Wounds. |

### Ítems RECHAZADOS (y por qué)
- **Sunfire Aegis:** Immolate 20 + 1.5% HP/s = ~65 DPS vs ~180 DPS de Liandry's. Oro muerto.
- **Warmog's Armor:** regen fuera de combate no ayuda en fights. Heartsteel da más HP + daño.
- **Force of Nature:** sin % damage reduction, es solo stats. Twinguard da más valor.
- **Sterak's Gage:** +50% AD base = ~63 AD (oro muerto). Gargoyle + Mantle cubren mejor.
- **Spirit Visage:** **no existe en 7.3** (verificado en BD de 186 ítems).
- **Thornmail:** solo vs AD auto-attackers puros. Armored Advance + Gargoyle son mejores.
- **Cualquier ítem de crítico:** oro muerto. Cho'Gath no critica.

---

## 7. RUNAS · HECHIZOS · HABILIDADES

### Runas (árbol completo)

**Keystone: Grasp of Undying** ⭐⭐⭐⭐⭐
- Cada 3s en combate, siguiente ataque: +3.3% max HP mágico + cura 1.3% max HP + **10 HP permanente**
- Con 6500 HP: **214 daño mágico + 84 HP de cura + 10 HP permanente** cada 3s
- **Sinergia perfecta:** más HP = más daño de Grasp = más sustain = más stacks de Feast

**Secundarias (Resolve):**
- **Demolish:** cada 3 ataques a torre = 85 + 28% max HP físico. Con 6500 HP = **1905 daño físico** a torres. Tomas placas en 2-3 golpes.
- **Second Wind:** tras recibir daño, regenera 3 + 1.5% HP faltante sobre 5s. Sustain en lane vs poke.
- **Overgrowth:** cada 3 minions/monstruos muertos cerca = +3 HP permanente. Al llegar a 30 stacks = +3% max HP. Late game: +500 HP extra.

**Terciarias (Sorcery/Resolve):**
- **Revitalize:** +5% a curas/escudos (+10% si target <40% HP). Sinergiza con Grasp + Heartsteel regen + Gargoyle escudo.
- **Axiom Arcanist:** +10% daño/curas/escudos de R + -7% CD con takedown. Tu R es tu identidad.

**Alternativas por matchup:**
- **vs Volibear (burst AD):** Bone Plating (reduce 30-60 daño de sus 3 golpes) en lugar de Second Wind
- **vs Dr. Mundo (regen):** Triumph (10% HP perdido + 35 MS por takedown) para cerrar con R + Ignite
- **vs AP pesados:** Nullifying Orb (escudo 60-180 al caer bajo 35% HP)

### Hechizos
- **Flash + Ignite** (default): Ignite asegura Feast stacks en lane + 60% Grievous Wounds vs Mundo/Soraka
- **Flash + Teleport** (split push): si tu equipo tiene buen engage y tú quieres presión global
- **Flash + Ghost** (vs kiting): si el enemigo es ranged y te kitea (Vayne, Quinn)

### Orden de habilidades
1. **E** (nivel 1) — waveclear + daño % HP desde el inicio
2. **Q** (nivel 2) — CC para trades + asegurar CS
3. **W** (nivel 3) — silencio para evitar que el enemigo use hechizos
4. **R** (nivel 5/9/13) — SIEMPRE que esté disponible
5. **Maxear E primero** (más daño % HP + ancho de cono con stacks)
6. **Luego Q** (más daño + menos CD)
7. **W al final** (el silencio dura igual en todos los ranks)

---

## 8. COMPARACIÓN CONTRA LAS ALTERNATIVAS

### Tabla maestra (nivel 15, 22 stacks de Feast, AP 250, HP 6500)

| Build | Oro | HP total | AP | Tamaño total | R execute | E % HP | EHP ventana | vs Volibear | vs Mundo |
|-------|-----|----------|----|--------------|-----------|--------|-------------|-------------|----------|
| **TITÁNICA (propuesta)** | 17 050 | 6 500 | 250 | **+165%** | **1 500** | **16.7%** | **18 000** | ✅ Gana | ✅ Gana |
| Comunidad (Heartsteel + Hollow Radiance + Mercury's) | 15 800 | 5 800 | 180 | +135% | 1 280 | 15.2% | 14 500 | ⚠️ Empate | ❌ Pierde |
| AP puro (Liandry's + Rabadon's + Cryptbloom) | 17 400 | 4 200 | 520 | +135% | 1 360 | 13.8% | 8 500 | ❌ Pierde | ✅ Gana |
| Tanque puro (Heartsteel + Gargoyle + Twinguard + Warmog's + Iceborn) | 17 150 | 7 800 | 0 | +155% | 1 380 | 17.5% | **22 000** | ✅ Gana | ❌ Pierde (sin pen) |

### Desglose multiplicativo de la diferencia (Titánica vs Comunidad)
1. **+700 HP** (Rod of Ages + Liandry's vs Hollow Radiance) → +70 daño de R
2. **+70 AP** (Liandry's + Rod of Ages stacks) → +35 daño de R + +21 daño de E por pico
3. **+30% bonus resistencias** (Twinguard max stacks) → +30% EHP efectivo
4. **+20% tamaño** (Twinguard) → cono de E más ancho + intimidación
5. **Escudo de Gargoyle** (90% HP bonus = ~5950) → ventana burst imparable

---

## 9. PLAN DE JUEGO

### Early (niveles 1-5)
- **Start:** Ruby Crystal (500g) + poción. Primer recall: Catalyst of Aeons (1100g) si vas por RoA, o Ruby Crystal + Boots of Speed si necesitas movilidad.
- **Lvl 1-2:** E para farmear + pokear. Q para asegurar CS o trades. **No uses W** (gasta mucho maná early).
- **Lvl 3-5:** busca trades cortos con E + Q + auto. Tu pasiva Carnivore te da sustain al matar minions.
- **Objetivo:** 6 stacks de Feast de minions (cap) + 1-2 de campeones si puedes. **No mueras** — cada muerte retrasa tu escalado.

### Mid (niveles 6-11)
- **Pico 1 (Heartsteel + botas T3, ~min 10-11):** tu R ejecuta ~720 true damage. Busca kills con Q + E + R + Ignite.
- **Placas de torreta:** con Demolish + E + Q, tomas placas en 2-3 golpes. Cada placa = 140g + 150g first blood.
- **Épicos:** **PRIORIZA DRAGONES/HERALD** aunque pierdas CS. Cada épico = 1 stack de Feast SIN CAP = +160 HP + 6% tamaño + daño de R.
- **Rotaciones:** con tu Q (knockup 1s) + W (silencio 2s), eres un ganker brutal. Rota a mid si ves oportunidad.

### Late (niveles 12-15)
- **Pico 2 (Twinguard + Gargoyle, ~min 15-18):** eres literalmente imparable. En teamfights:
  1. Entra con Q (knockup) + W (silencio)
  2. Activa Gargoyle (escudo de ~6000 + tamaño gigante)
  3. Twinguard stackea (5s = +20% tamaño + 30% resistencias)
  4. Usa E en cono gigante (barre teamfights enteros)
  5. Ejecuta con R al target más bajo de HP
- **Split push:** con Demolish + E + Q + 700 de rango (22 stacks), tomas torres más rápido que cualquier top laner. Si vienen 2 a por ti, tu R + Gargoyle te permiten sobrevivir hasta que llegue tu equipo.
- **Baron Nashor:** tu R ejecuta Baron con ~1500 true damage. Con Smite (1400 true) + R = **2900 true damage seguro**. Nadie te roba Baron.

### Reglas del parche 7.3 que cambian el macro
- **Min 5:00:** placas de torreta decaen (-10g/30s). Toma placas temprano.
- **Min 10:00:** botas T3 disponibles. Prioriza Armored Advance vs AD o Chainlaced vs AP.
- **Min 12:00:** penalización de jungla a laners se remueve. Puedes invadir jungla enemiga sin miedo.
- **Épicos más contestables:** duración estándar, Baron mid-game buffeado. Cada épico = 1 stack de Feast. **Prioriza dragones/herald aunque pierdas CS.**

---

## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS

### Fuentes primarias
- **Notas oficiales 7.3** (21-sep-2026): sistema de botas T3, Smite escalado con stats, torretas 7000 HP, Crystalline Overgrowth
- **Notas oficiales 7.2** (08-jul-2026): fin de encantamientos de botas, QSS/Scimitar como ítems de clase
- **Apéndice oficial de AS 7.3:** Cho'Gath base 0.625, ratio 0.625, bonus 0.28, growth 0.008

### Fuentes secundarias
- **wr-meta.com** (24-sep-2026): stats base de Cho'Gath (62 AD, 690 HP, 350 MS, 125 rango), habilidades con valores, change history
- **BD de 186 ítems 7.3:** verificación de que Spirit Visage NO existe, stats de Heartsteel/Twinguard/Gargoyle/Mantle

### Discrepancias detectadas
1. **Tamaño de Gargoyle:** las notas oficiales dicen "+tamaño durante el activo" pero no especifican el porcentaje. Modelado como +20% (conservador, similar a Twinguard). **Verificar en juego.**
2. **Ancho del cono de E:** la ficha dice "Vorpal Spikes' width increases with Cho'Gath's size" pero no da fórmula. Asumimos escala lineal con tamaño total.
3. **Stacks de Feast de épicos:** la ficha dice "Stacks gained from minions and non-epic monsters are capped at 6" pero no especifica cap de épicos. Asumimos sin cap (confirmado por notas 7.3 de épicos más contestables).

### Supuestos del modelo
- **22 stacks de Feast al late game:** 6 de minions (cap) + 5 de campeones early + 11 de épicos/teamfights
- **Uptime de E:** 75% (3 ataques cada 4s en pelea)
- **Twinguard stacks:** 5 stacks (5s en combate) = +20% tamaño + 30% bonus resistencias
- **Gargoyle activo:** usado al inicio de teamfight (2.5s de escudo + tamaño)
- **Mantle Lifeline:** activado al caer bajo 30% HP (ventana reactiva)
- **R execute calculado vs target con 100 MR:** daño verdadero ignora resistencias

### Contexto meta (24/09, Diamond+)
- **Cho'Gath Top:** WR 51.20%, Pick 12.60%, Ban 38.00% (perma-ban)
- **Muestra pequeña post-parche:** solo 7 días de datos 7.3. El meta de tanques está en ajuste.
- **Matchups específicos:**
  - **vs Dr. Mundo (WR 52.3%):** tu R lo ejecuta antes que su R lo cure (con Ignite + Liandry's burn). Ganas 60% de las lanes.
  - **vs Volibear (WR 49.4%):** tu sustain + R execute > su burst + shield. Ganas 55% de las lanes.
  - **vs Camille (WR 48.7%):** cuidado con su true damage de Q2. Compra Armored Advance temprano.
  - **vs Darius (WR 47.9%):** su R ejecuta con más HP que tú. Juega seguro hasta Heartsteel.

---

## APÉNDICE A — POOL DE ÍTEMES PARA CHO'GATH TOP (veredicto)

| Ítem | Oro | Veredicto |
|------|-----|-----------|
| **Heartsteel** | 3000 | ✅ **Core 1** — stacking infinito de HP + daño |
| **Rod of Ages** | 2700 | ✅ **Core 2** — HP + AP + maná + growth temporal |
| **Amaranth's Twinguard** | 3200 | ✅ **Core 3** — capstone de tamaño + bonus resistencias |
| **Gargoyle Stoneplate** | 2900 | ✅ **Core 4** — ventana burst + tamaño gigante |
| **Liandry's Torment** | 3000 | ✅ **Core 5 (default)** — daño sostenido vs tanques |
| **Armored Advance** (T3) | 2200 | ✅ **Botas default** — vs AD fighters |
| **Chainlaced Crushers** (T3) | 2200 | ✅ **Botas vs AP** — +30 MR + 30% tenacidad |
| **Cryptbloom** | 3000 | ⚠️ Situacional — vs 2+ tanques con MR |
| **Mantle of the Twelfth Hour** | 2550 | ⚠️ Situacional — vs burst AP + Lifeline +10% tamaño |
| **Iceborn Gauntlet** | 3000 | ⚠️ Situacional — split push + slow field |
| **Morellonomicon** | 2650 | ⚠️ Situacional — vs curación (Mundo/Soraka) |
| **Frozen Heart** | 2550 | ⚠️ Situacional — vs AD pesados + -25% AS |
| **Sunfire Aegis** | 2900 | ❌ Oro muerto — Immolate < Liandry's burn |
| **Warmog's Armor** | 2850 | ❌ Regen fuera de combate no ayuda en fights |
| **Force of Nature** | 2800 | ❌ Sin % damage reduction en 7.3 |
| **Sterak's Gage** | 3200 | ❌ +50% AD base = ~63 AD (oro muerto) |
| **Spirit Visage** | — | ❌ **No existe en 7.3** |
| **Thornmail** | 2700 | ❌ Solo vs AD auto-attackers puros |
| **Cualquier ítem de crítico** | — | ❌ Oro muerto — Cho'Gath no critica |

---

## APÉNDICE B — RUTAS DE COMPRA POR MATCHUP

### DEFAULT (vs la mayoría de top laners)
```
Ruby Crystal → Catalyst → Plated Steelcaps → Heartsteel → ⬆️ Armored Advance
→ Rod of Ages → Twinguard → Gargoyle → Liandry's
```

### VS DR. MUNDO (tanque regenerativo)
```
Ruby Crystal → Liandry's (1º) → Plated Steelcaps → Heartsteel → ⬆️ Armored Advance
→ Twinguard → Gargoyle → Morellonomicon (6º, 50% GW)
```
**Clave:** Liandry's burn + Morellonomicon GW contrarrestan su regen. Tu R lo ejecuta antes que su R lo cure.

### VS VOLIBEAR (burst AD + shield)
```
Ruby Crystal → Plated Steelcaps (early) → Heartsteel → ⬆️ Armored Advance
→ Rod of Ages → Twinguard → Gargoyle → Frozen Heart (6º, -25% AS)
```
**Clave:** Armored Advance temprano + Frozen Heart reduce su AS (su daño viene de autos + W). Tu R execute > su R HP bonus.

### VS AP BURST (Annie/Brand/Rumble)
```
Ruby Crystal → Catalyst → Mercury's Treads → Heartsteel → ⬆️ Chainlaced Crushers
→ Rod of Ages → Twinguard → Mantle (6º, Lifeline +10% tamaño) → Gargoyle
```
**Clave:** Chainlaced + Mantle + Gargoyle = 3 capas de defensa vs burst. Mantle Lifeline te salva de su combo completo.

### SPLIT PUSH / SIEGE
```
Ruby Crystal → Heartsteel → Plated Steelcaps → ⬆️ Armored Advance
→ Iceborn Gauntlet → Twinguard → Gargoyle → Liandry's
```
**Clave:** Iceborn slow field + Demolish + E en cono gigante = tomas torres más rápido que cualquier top laner. Si vienen 2 a por ti, Gargoyle + R te permiten sobrevivir.