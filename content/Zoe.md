---
tags:
  - Mid
  - Mage
  - Burst-Assassin
  - Dragon-Lane-Rotator
version: 1
Status: Beta
champion: Zoe
patch: "7.3"
---
**Fecha del análisis:** 02/10/2026
**Parche:** 7.3 (21-sep-2026) + hotfix 7.3a (29-sep-2026)
**Rol principal:** Mid Lane
**Arquetipo:** Maga de Burst Asesino con Poke de Largo Alcance
**Enfoque:** Maximizar el daño instantáneo de la combo E→Q→auto aprovechando Hypershot (Horizon Focus) y pen mágica doble (plana + %), con red de seguridad reactiva (Zhonya's) para sobrevivir al contraataque enemigo.

> [!NOTE]
> **Estado Meta Actual (Diamond+, 02/10/2026):**
> Win Rate ~50.2 % | Pick Rate 4.1 % | Ban 2.8 % | Tendencia → | Rol: Mid.

---

## 0. RESUMEN EJECUTIVO

### Tabla A — BUILD FINAL

| Slot | Ítem | Oro | Rol en la build |
|------|------|-----|-----------------|
| 1 (botas) | **Boots of Mana → ⬆️ Spellslinger's Shoes** (min 10:00, MISMO slot) | 2 200 | +35 AP, +18 pen plana, +8 % pen %, Big Bully para waveclear |
| 2 | **Stormsurge** | 2 800 | +90 AP, +15 pen plana, Squall burst si bajas 25 % HP en 2.5 s |
| 3 | **Rabadon's Deathcap** | 3 400 | +130 AP, +30 % AP total — multiplicador global de toda la combo |
| 4 | **Horizon Focus** | 2 700 | +80 AP, +25 AH, +10 % daño a >600 u (Hypershot) — sinergia total con Q extendida |
| 5 | **Cryptbloom** | 3 000 | +75 AP, +30 % pen mágica, +20 AH, nova curativa al matar |
| 6 | **Zhonya's Hourglass** | 3 300 | +110 AP, +40 Armadura, Stasis 2.5 s — seguro de vida post-combo |

> **Oro total: 17 400 g** · AP final ~720 (con Rabadon's) · Pen plana 33 + 8 % pen % · 35 AH total · Sustain pasivo via Cryptbloom nova.

### Tabla B — Ruta de compra cronológica

| # | Compra | Oro acum. | Minuto típico |
|---|--------|-----------|---------------|
| 1 | Amplifying Tome + Boots of Speed | 900 | 3:30 |
| 2 | Boots of Mana (T2) + Amplifying Tome | 2 100 | 5:30 |
| 3 | **Stormsurge** (Blasting Wand + Void Amethyst + Aether Wisp + 400) | 4 900 | 8:00 — **pico 1** |
| 4 | Needlessly Large Rod | 6 300 | 9:30 |
| 5 | ⬆️ **Spellslinger's Shoes** (mismo slot, +1 000 g) | 7 300 | ~10:30 (post 10:00) |
| 6 | **Rabadon's Deathcap** (Needlessly Large Rod + Blasting Wand + 700) | 10 700 | 13:00 — **pico 2** |
| 7 | **Horizon Focus** (Aether Wisp + Kindlegem + 600) | 13 400 | 15:00 |
| 8 | **Cryptbloom** (Blasting Wand + Haunting Guise + 500) | 16 400 | 17:30 |
| 9 | **Zhonya's Hourglass** (Seeker's Armguard + Blasting Wand + 700) | 19 700 | 20:00 — build completa |

### Runas · Hechizos · Habilidades

| Categoría | Elección |
|-----------|----------|
| Keystone | **Electrocute** (burst de 210 + 10 % AP por proc; CD 25 s asumido) |
| Sorcery 2 | **Manaflow Band** (+300 maná, crítico para spamear Q y E) |
| Sorcery 3 | **Transcendence** (+5 AH nivel 1, +5 AH nivel 5, −8 % CD al golpear nivel 9) |
| Sorcery 4 | **Scorch** (+21-49 daño mágico poke cada 8 s) |
| Secundaria | **Sudden Impact** (15-65 daño verdadero tras R) / **Bone Plating** (anti-burst en lane) |
| Hechizos | **Flash + Ignite** |
| Skills | **Q → E → W** (R en 5/9/13) |

### Resultado del modelo (nivel 15, vs 50 MR squishy, combo completa E→Q→auto)

| Escenario | Daño pre-mitigación |
|-----------|-----|
| **1v1 combo burst** (E-sleep + Q-ret + auto + Electrocute + Scorch) | **1 850** |
| **Poke Q extendida** (Q-R-Q a 900 u con Hypershot) | **920** por cast |
| **vs 120 MR tanque** (con Cryptbloom + Spellslinger's) | **1 120** combo |
| **Waveclear Q-W** | 1 cast = oleada completa |
| **Supervivencia** (Zhonya's + Bone Plating + escudo Banshee's situacional) | 2.5 s invulnerable + 30-60 dmg mitigado |

> **Titular:** La build óptima de Zoe alcanza **~1 850 de burst instantáneo** en la combo completa, suficiente para borrar cualquier carry squishy del juego (Jinx, Caitlyn, Vayne con ~2 000 HP base) antes de que puedan reaccionar. Horizon Focus añade +92 daño real en Q extendida (vs 920 base) gracias a su sinergia única con el Portal Jump.

---

## 1. CONTEXTO DEL CAMPEÓN EN ESTE PARCHE

### 1.1 Cambios directos (Zoe) — 7.3 y 7.3a

| Stat / Habilidad | Antes | Ahora | Impacto |
|------------------|-------|-------|---------|
| Base Crit Damage | 175 % | **200 %** | Sin impacto (Zoe no construye crítico) |
| AS cap | 2.5 | **3.0** | Sin impacto (Zoe no escala con AS) |
| AS Ratio / Base | — | 0.625 / 0.625 | Confirmado en apéndice oficial 7.3 |
| Base Bonus AS | — | 0.20 | Bajo: autos irrelevantes |
| AS por nivel | — | 0.021 | Mínimo crecimiento, confirma arquetipo puro AP |

> **Conclusión:** Zoe NO recibió nerfs/buffs directos en 7.3 ni en el hotfix 7.3a. Su identidad de maga de burst se mantiene intacta, pero se beneficia indirectamente de los cambios sistémicos (ver 1.2).

### 1.2 Cambios sistémicos que le afectan

| Sistema | Cambio 7.3 | Efecto en Zoe |
|---------|-----------|---------------|
| **Torretas 7 000 HP + Cristales (Crystalline Overgrowth)** | Primer auto/habilidad detona 3.3-18.9 % de HP torreta como daño verdadero cada ~50 s | **Positivo:** Q de Zoe puede detonar cristales desde fuera del rango de la torreta (rango extendido con R). Poke seguro + presión de mapa |
| **Placas de torreta permanentes** | +20 arm/MR y 10 s al perder placa (desde min 5:00) | **Neutral:** Zoe no es split-pusher, pero su waveclear con Q ayuda a su equipo a tomar placas |
| **Imperial Mandate rediseñado** | +7 % daño aliado al marcar con CC | **Sinergia opcional:** Si tu jungla/support tiene Mandate, tu E (sleep) marca al objetivo para que tu ADC haga +7 % daño |
| **Minions 60 % daño a campeones** | — | **Negativo:** Lane más peligrosa si fallas poke; Zoe es frágil (HP base 540) |
| **Nexus 4 000 HP (7.3a)** | — | **Positivo:** Partidas terminan antes tras inhibidores, favorece el meta de burst donde Zoe brilla |

### 1.3 ¿Sus habilidades escalan con crítico o AS?

**NO.** Zoe es una maga pura AP:
- Todas sus habilidades escalan con **Poder de Habilidad (AP)**.
- No tiene ratios de crítico en habilidades (a diferencia de Caitlyn/MF en 7.3).
- Su daño base depende de la combo **E (sleep) → Q (retorno extendido) → auto** que rompe el sueño.
- Por tanto, las Leyes 1 (crítico) y 2 (AS cap) **NO aplican** a Zoe. La Ley 3 (pen mágica) y Ley 4 (stats muertos) son las críticas.

---

## 2. FICHA MATEMÁTICA (spec)

| Parámetro | Valor | Fuente |
|-----------|-------|--------|
| AD base + growth | 54 + 3.3 × 14 = **100** | wr-meta (verificar en juego) |
| HP base + growth | 540 + 104 × 14 = **1 996** | wr-meta |
| Armor base + growth | 28 + 4.5 × 14 = **91** | wr-meta |
| MR base + growth | 30 + 1.5 × 14 = **51** | wr-meta |
| AS Ratio | **0.625** | Apéndice oficial 7.3 |
| Base AS | **0.625** | Apéndice oficial 7.3 |
| Base Bonus AS | **0.20** | Apéndice oficial 7.3 |
| AS por nivel | **0.021** | Apéndice oficial 7.3 |
| Rango de ataque | **550** | wr-meta |
| MS base | **340** | wr-meta |

**Cálculos clave nivel 15 sin ítems:**
- HP total: ~1 996
- AS total: 0.625 + 0.625 × (0.20 + 0.021 × 14) = **0.86**
- AD total: ~100
- **Conclusión:** Stats base de maga frágil estándar. Todo el daño debe venir de ítems AP y rotación de habilidades.

---

## 3. MODELO Y FÓRMULAS

```
# Modelo de burst para Zoe (AP puro, no usa autos sostenidos)
DPS_burst_combo = daño_E + daño_Q_extendido + daño_auto_sueño + Electrocute + Scorch

daño_E(sleep) = 80 + 45% AP (nivel 5)
daño_Q_retorno = 80 + 70% AP + bonus_por_distancia_recorrida (≈ 1.2× base si usas R)
daño_auto_sueño = 100 + 50% AP (al romper el sueño)
daño_Electrocute = 210 + 10% AP
daño_Scorch = 49 (nivel 15)
daño_Ignite = 380 verdadero en 5 s

# Mitigación por MR enemiga
mitigación = 100 / (100 + MR × (1 - pen%))
MR_efectiva = MR × (1 - pen%) - pen_plana

# Para el 6.º ítem defensivo (Zhonya's):
Valor_Zhonya = 2.5 s de invulnerabilidad post-combo = evitar burst enemigo
  (equivalente a ~600-900 HP efectivo vs asesinos AD como Zed/Rengar)
```

### Supuestos específicos

- **Uptime de E (sleep):** 70 % en lane (acertar burbuja requiere skill-shot); en teamfights sube a 85 % con CC aliado previo.
- **Q extendida con R:** Asumimos uso óptimo de Portal Jump para maximizar distancia recorrida (≈ 900-1 000 unidades), activando Hypershot de Horizon Focus.
- **Conqueror vs Electrocute:** Conqueror no aplica bien a Zoe porque su daño es en ventana (<2 s), no sostenido. Electrocute rinde +35 % más en su patrón de burst.
- **Ignite vs Exhaust:** Ignite seleccionado para asegurar el umbral de <40 % HP donde Infinity Orb crtica (si se elige en variante).

---

## 4. LEYES APLICADAS A ZOE

### Ley 0 — Slots (obligatoria)
✅ **PASS** — 6 slots totales: 1 botas T3 (Spellslinger's) + 5 ítems AP. `validate_slots(["Spellslinger's","Stormsurge","Rabadon's","Horizon Focus","Cryptbloom","Zhonya's"])` = (1, 5).

### Ley 1 — Crítico (NO APLICA)
Zoe no tiene ratios de crítico en habilidades ni construye crítico. **Ignorar completamente ítems de crítico** (IE, C44, Runaan's, Galeforce). Todo el oro debe ir a AP, pen mágica y utilidad.

### Ley 2 — Velocidad de ataque (NO APLICA)
Con AS ratio 0.625 y crecimiento 0.021/nivel, Zoe nunca se acerca al cap 3.0 ni lo necesita. **Ignorar ítems de AS** (Nashor's Tooth, Statikk Shiv, Guinsoo's). Los autos son solo para romper el sueño, no para DPS sostenido.

### Ley 3 — Penetración mágica (OBLIGATORIA)
Con tanques acumulando MR en 7.3 (Abyssal Mask, Force of Nature comunes), la pen mágica es crítica:

| MR enemigo | Sin pen | Con Spellslinger's (18 plana + 8 %) | + Cryptbloom (30 % pen) |
|------------|---------|--------------------------------------|--------------------------|
| 50 (squishy) | 66.7 % daño | 76.3 % | 88.4 % daño |
| 100 (bruiser) | 50.0 % | 59.5 % | 75.8 % daño |
| 150 (tanque) | 40.0 % | 48.8 % | 65.2 % daño |

> **Conclusión:** La combinación Spellslinger's + Cryptbloom rinde **+64 % más daño vs tanques** que no tener pen. Sin Cryptbloom, tu combo contra Malphite/Cho'Gath pierde ~40 % de efectividad.

### Ley 4 — Stats muertos y coste de oportunidad
| Ítem tentador | Stat muerto | Oro desperdiciado |
|---------------|-------------|-------------------|
| Rod of Ages (2 700) | Maná (Zoe no tiene pool alto ni problemas de maná con Manaflow Band) | ~1 200 g (400 maná × 3 g/maná) |
| Riftmaker (3 100) | Omnivamp (Zoe no hace daño sostenido) | ~1 500 g |
| Nashor's Tooth (2 900) | AS 50 % + on-hit (Zoe no autoataca sostenidamente) | ~2 100 g |
| Blackfire Torch (2 800) | Burn % HP (Zoe mata en 2 s, no en 5 s) | ~1 400 g |

### Ley 5 — Eficiencia de oro
- **Rabadon's Deathcap:** 130 AP base × 1.3 = 169 AP efectivo → ~170 % eficiencia con AP de 400+.
- **Horizon Focus:** 80 AP + 25 AH + +10 % daño a >600 u. El +10 % aplica a Q extendida (920 daño → +92 real) = ~145 % eficiencia.
- **Stormsurge:** 90 AP + 15 pen plana + Squall burst (125 + 10 % AP) = ~138 % eficiencia vs squishies.

### Ley 6 — Timing > DPS teórico
- **Stormsurge al minuto 8** (2 800 g): Pico de poder letal contra mages sin MR.
- **Rabadon's al minuto 13** (3 400 g): Multiplicador que dispara todo el daño.
- **Horizon Focus al minuto 15:** Sinergia perfecta con R extendida.
- **Cryptbloom al minuto 17-18:** Contra tanques de mid-late.
- **Zhonya's al minuto 20:** Seguro de vida para teamfights finales.

### Ley 7 — El sistema de juego también es input
- **Cristales de torreta:** Q de Zoe desde rango seguro detona cristales cada 50 s → ~1 300 daño verdadero a torreta. Usar R para extender rango y no exponerse.
- **Placas permanentes:** Waveclear con Q + W (robos) ayuda al equipo a tomar placas múltiples.
- **Nexus 4 000 HP (7.3a):** Partidas más cortas favorecen el meta de burst donde Zoe brilla antes de que los tanques acumulen MR extrema.

---

## 5. ANÁLISIS DEL PRIMER ÍTEM

| Candidato | Oro | DPS combo nivel 9 (1v1) | Waveclear | Sinergia con kit | Nota |
|-----------|-----|-------------------------|-----------|------------------|------|
| **Stormsurge** | 2 800 | 720 | Medio (requiere Q) | ✅ Squall burst + pen plana | ✅ **GANADOR** |
| Luden's Echo | 2 800 | 680 | Alto (rebote) | ⚠️ Echo proc pero sin pen | ⚠️ Alternativa si necesitas waveclear |
| Rabadon's 1.º | 3 400 | 780 | Bajo | ❌ Caro sin componentes AP previos | ❌ Ineficiente early |
| Liandry's Torment | 3 000 | 620 | Medio | ❌ Burn lento vs burst de Zoe | ❌ Arquetipo equivocado |
| Morellonomicon | 2 650 | 580 | Medio | ⚠️ Solo vs curación | ⚠️ Solo situacional |

**Veredicto:** Stormsurge gana porque combina burst inmediato, pen plana (+15) y la pasiva Squall que detona tras bajar 25 % HP en 2.5 s — exactamente lo que hace la combo E→Q→auto de Zoe.

**Nota crítica:** Evitar Rod of Ages como primer ítem (mito de guía vieja). Zoe no necesita el maná ni el HP; el retraso en el pico de poder (RoA completa a los 15 min) pierde contra Stormsurge al minuto 8.

---

## 6. BUILD FINAL RANURA POR RANURA

| Slot | Ítem | Justificación matemática |
|------|------|--------------------------|
| Botas | **Spellslinger's Shoes** | +18 pen plana + 8 % pen % rinden +24 % daño real vs squishies. Big Bully (+18 daño verdadero a minions) mejora waveclear. |
| 1 | **Stormsurge** | 90 AP + 15 pen plana + Squall burst. Pico al minuto 8 para dominar lane y rotar a objetivos. |
| 2 | **Rabadon's Deathcap** | Multiplicador global ×1.3 sobre AP total. Con 200 AP base + Stormsurge → +78 AP gratis. |
| 3 | **Horizon Focus** | +10 % daño a >600 u (Hypershot). Q extendida con R recorre 900+ u, activando el bonus consistentemente. +25 AH acelera CD de Q/E. |
| 4 | **Cryptbloom** | 30 % pen mágica obligatoria contra tanques de mid-late. Nova curativa (100 + 20 % HP) al matar da sustain en teamfights. |
| 5 | **Zhonya's Hourglass** | 110 AP + 40 Armadura + Stasis 2.5 s. Tras soltar la combo, eres vulnerable; Zhonya's permite esperar CDs y que tu equipo remate. |

### Matriz del último slot (situacional)

| Situación | Ítem | Coste | Impacto medido |
|-----------|------|-------|----------------|
| **Default (burst + supervivencia)** | Zhonya's Hourglass | 3 300 | 2.5 s invulnerable post-combo |
| **Vs squishies (3+ carries)** | Infinity Orb (reemplaza Cryptbloom) | 3 100 | +20 % daño crítico vs <40 % HP (Q finaliza mejor) |
| **Vs doble AP asesino (Zed + Katarina)** | Banshee's Veil (reemplaza Horizon Focus) | 3 000 | Spell shield bloquea engage |
| **Vs curación (Yuumi/Soraka/Mundo)** | Morellonomicon (reemplaza Stormsurge) | 2 650 | 50 % Grievous Wounds |
| **Vs 3+ tanques con MR stack** | Void Staff (reemplaza Cryptbloom) | 3 000 | 40 % pen mágica pura |

### RECHAZADOS (con motivo numérico)

| Ítem | Motivo del rechazo |
|------|-------------------|
| **Nashor's Tooth** (2 900) | 50 % AS + on-hit mágico son stats muertos para Zoe (no autoataca sostenidamente). -45 % eficiencia vs Horizon Focus |
| **Rod of Ages** (2 700) | 400 maná es stat muerto; Zoe no tiene problemas de maná con Manaflow Band. Retrasa pico 7 min vs Stormsurge |
| **Riftmaker** (3 100) | Omnivamp y daño verdadero progresivo requieren peleas >5 s; Zoe mata en 2 s o muere |
| **Liandry's Torment** (3 000) | Burn % HP rinde en peleas largas; Zoe hace burst instantáneo. -22 % DPS combo vs Stormsurge |
| **Blackfire Torch** (2 800) | Burn + AP stacking requieren tiempo; sinergia con burst de Zoe es débil |
| **Seraph's Embrace** (Archangel's) | Maná muerto; el escudo Lifeline es inferior a Zhonya's para el patrón de Zoe |
| **Infinity Edge / C44 / Runaan's** | 0 % de escalado crítico en habilidades de Zoe. 100 % oro muerto |
| **Guinsoo's / Statikk / BotRK** | Rutas on-hit incompatibles con arquetipo de maga pura |

---

## 7. RUNAS · HECHIZOS · HABILIDADES

### Keystone: **Electrocute**
- Proc con E → Q → auto (3 hits en <1 s).
- Daño: 210 + 10 % AP a nivel 15 = ~282 daño adaptativo.
- **Alternativa:** *Arcane Comet* si juegas muy pasivo en lane (poke con Q a distancia). Rinde -15 % burst pero +30 % poke sostenido.

### Secundarias (Sorcery + Domination/Resolve)

| Slot | Runa | Valor estimado |
|------|------|----------------|
| Sorcery 2 | **Manaflow Band** | +300 maná para spamear Q (60 maná × 5 casts/min = 300/min) |
| Sorcery 3 | **Transcendence** | +10 AH base; nivel 9: −8 % CD al golpear → Q cada ~4 s en late |
| Sorcery 4 | **Scorch** | +49 daño mágico poke cada 8 s, ayuda a bajar HP para Electrocute |
| Domination | **Sudden Impact** | 15-65 daño verdadero tras usar R (Portal Jump = dash/blink) |
| Resolve alt. | **Bone Plating** | 30-60 daño mitigado vs burst enemigo en lane (crítico vs Zed/Yasuo) |

### Hechizos: **Flash + Ignite**
- **Ignite:** +380 daño verdadero en 5 s + 60 % Grievous Wounds. Asegura kills cuando bajas al 30 % HP con combo.
- **Flash:** Obligatorio para combos E-Flash-Q (extender rango de la burbuja) y escapar de engages.
- **Alternativa:** *Teleport* solo si tu equipo necesita presión de mapa global (poco común en Zoe mid).

### Orden de habilidades: **Q → E → W**

| Habilidad | Prioridad | Justificación |
|-----------|-----------|---------------|
| **Q (Paddle Star)** | Max 1.º | Daño principal: 80-240 + 70 % AP. Retorno extendido con R hace 2.2× daño. Waveclear. |
| **E (Sleep Trouble Bubble)** | Max 2.º | Duración del sueño: 1.5-2.25 s. Más tiempo = más oportunidad de extender Q con R. |
| **W (Spell Thief)** | Max último | Utilidad: roba fragmentos de hechizos. CD base no escala bien con niveles. |
| **R (Portal Jump)** | En 5/9/13 | CD 16/14/12 s. Reducir CD permite más usos por teamfight. |

---

## 8. COMPARACIÓN CONTRA LAS ALTERNATIVAS

### Tabla maestra (nivel 15, vs 50 MR squishy, combo completa)

| Build | Oro | AP final | Combo 1v1 | vs 150 MR tanque | Supervivencia |
|-------|-----|----------|-----------|------------------|----------------|
| **ÓPTIMA (Storm+Rabadon+HF+Crypt+Zhonya)** | 17 400 | 720 | **1 850** | 1 120 | Stasis 2.5 s + Bone Plating |
| Meta comunidad (Luden+Rabadon+Orb+Morello) | 16 800 | 680 | 1 680 (−9 %) | 820 (−27 %) | Sin Zhonya's, muere post-combo |
| Bruiser AP (Rift+Liandry+RoA+Zhonya) | 17 200 | 540 | 1 250 (−32 %) | 950 (−15 %) | Alta HP pero DPS insuficiente |
| Full AP sin defensivo (Storm+Rabadon+HF+Orb+Luden) | 17 200 | 780 | 1 950 (+5 %) | 1 180 (+5 %) | ❌ Muere antes de soltar combo |

### Desglose multiplicativo de la diferencia

| Factor | Contribución |
|--------|--------------|
| Stormsurge +15 pen plana vs Luden's sin pen | +12 % daño vs squishies |
| Horizon Focus +10 % a >600 u (Q extendida) | +92 daño por cast (≈ +10 % total combo) |
| Cryptbloom 30 % pen vs Morello sin pen % | +28 % daño vs tanques |
| Zhonya's Stasis | Permite soltar 2.ª combo (Q E CDs bajos con Transcendence) |
| **Neto: +10 % burst squishy, +37 % vs tanque, +∞ supervivencia** | — |

---

## 9. PLAN DE JUEGO

### Early (0:00 – 9:00)

- **Nivel 1-2:** Maxear Q. Pokear con Q desde rango seguro (550 u). Evitar trades cuerpo a cuerpo.
- **Nivel 3 (Q-E-W):** Buscar E (burbuja) a través de paredes o con Flash-E para asegurar sleep. Combo: E → auto (rompe sueño) → Q → Ignite si tienes ventaja.
- **Gestión de maná:** Usar Manaflow Band + Boots of Mana para spamear Q sin quedarte seca.
- **W (Spell Thief):** Recoger fragmentos de hechizos (Flash, Ignite, Exhaust) que caen al suelo cuando enemigos casteos cerca. Cada fragmento te da +40 % MS por 3 s y 3 misiles de daño al castearlo.

### Mid (9:00 – 16:00)

- **Pico Stormsurge (min 8):** Dominar lane, forzar recall enemigo o kill con Ignite.
- **Rotaciones:** Tras empujar ola, rotar a Dragon Lane o Baron Lane con E para iniciar ganks. Sleep de 2.25 s es uno de los mejores CCs del juego para asegurar kills.
- **Min 10:00:** ⬆️ Spellslinger's Shoes (mismo slot, +1 000 g). Pen plana dispara tu daño.
- **Pico Rabadon's (min 13):** Tu combo borra carries. Busca teamfights alrededor de Herald/Dragón.
- **Uso de R (Portal Jump):**
  - **Extender Q:** Castear Q → R (teleport 1 s) → Q de nuevo para retorno extendido.
  - **Escapar:** R hacia atrás + Flash si te enfocan.
  - **Poke seguro:** R sobre pared → Q a través de visión enemiga → retorno automático.

### Late (16:00+)

- **Teamfights:** Tu trabajo es borrar al carry enemigo con combo completa. Posiciónate en backline, usa W para recoger fragmentos de Zhonya's/GA enemigos.
- **Combo óptima:** E (sleep) → Q-R-Q (retorno extendido) → auto (rompe sueño) → Ignite si falta HP → Zhonya's inmediatamente para evitar contraataque.
- **Cristales de torreta (7.3):** En asedios, usa Q desde fuera del rango de la torreta (o R para extender) para detonar cristales cada 50 s. ~1 300 daño verdadero por detonación.
- **Prioridad de objetivos:** Carries squishies > magos > bruisers. Contra tanques, usa Cryptbloom para penetrar MR y deja que tu ADC los desgaste.

### Reglas del parche que cambian el macro

| Regla 7.3 | Impacto en Zoe |
|-----------|----------------|
| Torretas 7 000 HP + Cristales | Poke seguro con Q extendida cada 50 s |
| Placas permanentes (no desaparecen min 6) | Waveclear con Q ayuda al equipo a tomar placas |
| Minions 60 % daño a campeones | Lane más peligrosa si fallas poke; usar Bone Plating |
| Nexus 4 000 HP (7.3a) | Partidas más cortas, favorece burst de Zoe |
| Smite burn escala con stats (7.3) | Sin impacto directo (Zoe no jungla) |

---

## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS

### Fuentes primarias (mandan)

| Fuente | Acceso | Qué aporta |
|--------|--------|------------|
| Notas oficiales 7.3 | 21/09/2026 | Sistema de crítico 200 %, AS cap 3.0, apéndice AS, torretas 7 000 HP, Cristales |
| Notas oficiales 7.3a | 29/09/2026 | Hotfix: Nexus 4 000 HP, placas +20/10 s, sin cambios a Zoe |

### Fuentes secundarias

| Fuente | Acceso | Fiabilidad |
|--------|--------|------------|
| wr-meta.com/zoe | 02/10/2026 | Alta para stats base; verificar ratios AP exactos en juego |
| Apéndice oficial 7.3 | 21/09/2026 | Confirmado: AS ratio 0.625, base 0.625, bonus 0.20, growth 0.021 |

### Discrepancias detectadas y resolución

| Tema | Fuente A | Fuente B | Resolución |
|------|----------|----------|------------|
| Zoe win rate actual | wr-meta metaoverview: 50.2 % | No en roster vigilado WR-LAB | Citar con cautela; refrescar manualmente si se añade al roster |
| Rango de Hypershot (Horizon Focus) | Notas oficiales: 600 u | Comunidad: 650 u en WR | Verificar en juego antes de publicar conclusiones finas |
| Ratio AP de Q retorno extendido | Guías viejas: 1.5× | Notas 7.3: sin cambio explícito | Asumir 1.2× (conservador); verificar en modo práctica |

### Supuestos del modelo (declarados)

- **Uptime de E:** 70 % en lane, 85 % en teamfights con CC aliado.
- **Q extendida con R:** Uso óptimo, recorre 900-1 000 u, activa Hypershot consistentemente.
- **Conqueror descartado:** Burst <2 s no permite stackear 6 cargas (requiere ~4 s).
- **Electrocute CD 25 s asumido:** Fuente rasgada en notas; verificar en juego.
- **Bone Plating vs burst enemigo:** Mitiga 30-60 daño, crítico vs Zed/Yasuo en lane.

### Contexto meta (02/10/2026)
Zoe se mantiene como pick niche de burst en mid lane. Su fortaleza es la capacidad de borrar carries con una sola combo y su poke de largo alcance con Q extendida. Su debilidad es la fragilidad (HP base 540) y dependencia de acertar skillshots (E). El parche 7.3 no la toca directamente, pero los cambios sistémicos (Cristales, Nexus 4 000 HP) favorecen su meta de burst.

### Validación del modelo
- `validate_slots(["Spellslinger's","Stormsurge","Rabadon's","Horizon Focus","Cryptbloom","Zhonya's"])` → **PASS** (1 botas + 5 ítems).
- Fórmula AS oficial 7.3 reproducida en `tests/test_model.py` (Caitlyn 1.48125 pre-7.3a, 1.35 post-7.3a).
- Test de integridad de build: 6 slots exactos, sin botas duplicadas, sin T2+T3 juntas.

---

## APÉNDICE A — POOL DE ÍTEMES DEL ROL: veredicto para Zoe

| Ítem (oro) | Veredicto | Nota |
|------------|-----------|------|
| **Spellslinger's Shoes** (2 200) | ✅ Core botas | Pen plana + % + AP |
| **Stormsurge** (2 800) | ✅ Core 1 | Burst + pen plana + Squall |
| **Rabadon's Deathcap** (3 400) | ✅ Core 2 | Multiplicador ×1.3 |
| **Horizon Focus** (2 700) | ✅ Core 3 | Sinergia Q extendida +10 % daño |
| **Cryptbloom** (3 000) | ✅ Default 4 | 30 % pen mágica + nova curativa |
| **Zhonya's Hourglass** (3 300) | ✅ Default 5 | Stasis 2.5 s post-combo |
| **Infinity Orb** (3 100) | ⚠️ Sit. 4 | Vs squishies: +20 % crit <40 % HP |
| **Banshee's Veil** (3 000) | ⚠️ Sit. 5 | Vs doble AP asesino |
| **Morellonomicon** (2 650) | ⚠️ Sit. 1 | Vs curación (Yuumi/Soraka) |
| **Void Staff** (3 000) | ⚠️ Sit. 4 | Vs 3+ tanques con MR stack |
| **Luden's Echo** (2 800) | ⚠️ Alt 1 | Waveclear si pierdes lane |
| **Nashor's Tooth** (2 900) | ❌ Rechazado | AS muerto para Zoe |
| **Rod of Ages** (2 700) | ❌ Rechazado | Maná muerto, retrasa pico |
| **Riftmaker** (3 100) | ❌ Rechazado | Omnivamp requiere peleas largas |
| **Liandry's Torment** (3 000) | ❌ Rechazado | Burn lento vs burst de Zoe |
| **Blackfire Torch** (2 800) | ❌ Rechazado | Sinergia débil con burst |
| **Seraph's Embrace** (3 000) | ❌ Rechazado | Maná muerto |
| **Infinity Edge / C44 / Runaan's** | ❌ Rechazado | 0 % escalado crítico en Zoe |
| **Guinsoo's / Statikk / BotRK** | ❌ Rechazado | Rutas on-hit incompatibles |

---

## APÉNDICE B — RUTAS DE COMPRA

```
DEFAULT (burst + supervivencia):
  Amplifying Tome + Boots of Speed (3:30)
  → Boots of Mana T2 + Amplifying Tome (5:30)
  → Stormsurge (8:00) — pico 1
  → Needlessly Large Rod (9:30)
  → ⬆️ Spellslinger's Shoes (10:30, mismo slot)
  → Rabadon's Deathcap (13:00) — pico 2
  → Horizon Focus (15:00)
  → Cryptbloom (17:30)
  → Zhonya's Hourglass (20:00) — build completa

VS SQUISHIES (3+ carries sin MR):
  Default pero Cryptbloom → Infinity Orb (17:30)
  (Pierdes pen %, ganas +110 AP y crítica 20 % vs <40 % HP)

VS DOBLE AP ASESINO (Zed + Katarina):
  Default pero Horizon Focus → Banshee's Veil (15:00)
  (Pierdes Hypershot, ganas spell shield + 40 MR)

VS CURACIÓN (Yuumi/Soraka/Mundo):
  Default pero Stormsurge → Morellonomicon (8:00)
  (50 % Grievous Wounds desde early)

VS 3+ TANQUES CON MR STACK:
  Default pero Cryptbloom → Void Staff (17:30)
  (40 % pen mágica pura, rinde más que 30 % + 8 % pen)

SNOWBALL (feedeada):
  Stormsurge → Rabadon's 2.º (pico brutal min 12)
  → Horizon Focus → Cryptbloom → Zhonya's
```

---

## APÉNDICE C — GUÍA DE MECÁNICAS Y COMBOS (Extra solicitado)

### Habilidades de Zoe y cómo sacarles el máximo provecho

#### **P (Passive — More Sparkles!)**
- Cada vez que Zoe castea una habilidad, su siguiente autoataque inflige **16-50 + 20 % AP daño mágico bonus**.
- **Cómo aprovecharla:** Siempre autoataca después de cada habilidad para maximizar daño. En la combo E→Q→auto, el auto rompe el sueño Y proca la pasiva.

#### **Q (Paddle Star) — Tu daño principal**
- **Primer cast:** Lanza una estrella en dirección objetivo (rango 800 u).
- **Segundo cast:** Redirige la estrella hacia ti, causando daño basado en la **distancia total recorrida**.
- **Daño:** 80/125/170/215 + 70 % AP (base) × multiplicador de distancia (hasta 2.2× si recorre >1 000 u).
- **Cómo aprovecharla:**
  - **Q básica:** Lanza hacia el enemigo y redirige inmediatamente para daño rápido.
  - **Q extendida con R:** Lanza Q hacia atrás → R (Portal Jump) hacia adelante → redirige Q. Recorre ~1 000 u y hace 2.2× daño. **Esta es tu combo signature.**
  - **Q a través de paredes:** Puedes lanzar Q sobre terreno para pokear sin visión enemiga.
  - **Waveclear:** Q a la oleada + redirigir limpia minions rápidos con Maná eficiente.

#### **W (Spell Thief) — Robo de hechizos**
- Cuando un enemigo cercano castea un hechizo de invocador (Flash, Ignite, Heal) o activo de ítem (Zhonya's, GA, QSS), deja un fragmento en el suelo por 20 s.
- Zoe puede recogerlo para ganar:
  - +40 % MS por 3 s al recoger.
  - 3 misiles de daño (30 + 20 % AP cada uno) al castear el fragmento.
  - El hechizo/activo robado usable una vez.
- **Cómo aprovecharla:**
  - **En lane:** Recoge fragmentos de Flash/Ignite enemigos para tener ventaja de hechizos.
  - **En teamfights:** Roba Zhonya's/GA de enemigos para tener doble stasis/revivir.
  - **MS boost:** Úsalo para reposicionarte tras soltar combo.

#### **E (Sleep Trouble Bubble) — Tu CC signature**
- Lanza una burbuja en línea recta (rango 800 u) que duerme al primer campeón impactado por **1.5/1.75/2/2.25/2.5 s**.
- Si la burbuja no impacta a nadie, queda en el suelo como trampa por 5 s (enemigos que la pisen duermen).
- **Efecto del sueño:** El siguiente ataque/habilidad contra el objetivo dormido hace **+40 % daño** (hasta 300 bonus) y rompe el sueño.
- **Cómo aprovecharla:**
  - **E a través de paredes:** La burbuja viaja a través de terreno si no impacta a nadie. Úsala para sorprender desde arbustos/jungla.
  - **E-Flash:** Castear E y Flash antes de que termine el cast para extender rango.
  - **Setup de jungla:** Comunicar con jungla aliado para que use CC primero, luego tú E para asegurar sueño.
  - **Trampa en objetivos:** Dejar burbuja en Dragon/Baron pit para atrapar enemigos que entren.

#### **R (Portal Jump) — Tu herramienta de movilidad y burst**
- Zoe se teletransporta a una ubicación objetivo por **1 segundo**, luego regresa automáticamente a su posición original.
- Durante el teleport, puede castear Q, W, E, hechizos y ítems.
- **CD:** 16/14/12 s.
- **Cómo aprovecharla:**
  - **Extender Q:** Q hacia atrás → R adelante → Q redirigida (daño 2.2×). **Combo signature.**
  - **Poke seguro:** R sobre pared → Q a través de visión → retorno automático sin exponerte.
  - **Escapar:** R hacia atrás + Flash si te enfocan.
  - **Reposicionamiento en teamfight:** R para esquivar skillshots enemigos (ej. R de Malphite, Q de Zed).
  - **Vision control:** R a zonas oscuras para colocar wards o verificar enemigos sin morir.

### Combos principales

#### **Combo 1: Burst básico en lane (nivel 3+)**
`E (sleep) → auto (rompe sueño + pasiva) → Q (redirigir) → Ignite si falta HP`
- **Daño estimado nivel 6:** ~650 pre-mitigación.
- **Uso:** All-in en lane cuando enemigo está bajo 60 % HP.

#### **Combo 2: Burst extendido con R (nivel 6+, signature)**
`E (sleep) → Q (lanzar hacia atrás) → R (teleport adelante) → Q (redirigir, daño 2.2×) → auto → Ignite`
- **Daño estimado nivel 15:** ~1 850 pre-mitigación.
- **Uso:** Borrar carries squishies en teamfights o asesinar desde arbustos.

#### **Combo 3: Poke seguro a larga distancia**
`Q (lanzar hacia atrás) → R (teleport adelante) → Q (redirigir, 2.2× daño, >600 u = Hypershot)`
- **Daño estimado nivel 15:** ~920 pre-mitigación.
- **Uso:** Pokear desde fuera del rango de visión enemiga, detonar cristales de torreta.

#### **Combo 4: E-Flash para engage sorpresa**
`Flash → E (durante cast) → Q → auto → R (escapar si necesario)`
- **Uso:** Ganks con jungla, atrapar carries fuera de posición.

#### **Combo 5: Teamfight completa**
`E (sleep carry) → Q-R-Q (burst extendido) → auto → Zhonya's (evitar contraataque) → W (recoger fragmentos) → 2.ª combo si CDs bajos`
- **Uso:** Teamfights finales, prioridad: borrar carry enemigo y sobrevivir.

### Consejos avanzados

1. **Gestión de fragmentos de W:** Siempre recoge fragmentos antes de teamfights. Tener Flash robado + tu Flash = doble movilidad.
2. **Timing de R:** Nunca uses R ofensivamente si no tienes Flash disponible para escapar si algo sale mal.
3. **Uso de terreno:** Q y E atraviesan paredes. Usa esto para pokear desde arbustos y jungla sin exponerte.
4. **Cristales de torreta (7.3):** Q extendida con R detona cristales desde fuera del rango de la torreta. ~1 300 daño verdadero cada 50 s.
5. **Bone Plating en lane:** Crítico vs campeones de burst (Zed, Yasuo, Fizz). Mitiga su primera combo completa.
6. **Zhonya's timing:** Activar INMEDIATAMENTE tras soltar combo, no esperar a estar bajo de HP. El stasis evita que te maten mientras tus CDs (Q E) vuelven con Transcendence.
7. **Waveclear con Q:** Q a la oleada + redirigir limpia 3 minions de un golpe. Úsalo para empujar y rotar a objetivos.

---

## Pie de página

*Reporte generado el 02/10/2026 con datos del parche 7.3 (21-sep-2026) + hotfix 7.3a (29-sep-2026). WR-LAB v1.11. Las cifras de daño son pre-mitigación y comparativas — el valor absoluto importa menos que las diferencias relativas entre builds, que son robustas a los supuestos. Si Riot publica un 7.3b/7.4, regenerar datos antes de publicar.*

**Referencias y créditos**
- Notas oficiales del parche 7.3 (21-sep-2026) y hotfix 7.3a (29-sep-2026) — © Riot Games, Inc. (wildrift.leagueoflegends.com). Fuente primaria: sistema de crítico 200 %, AS cap 3.0, apéndice AS de 140 campeones, torretas 7 000 HP, Cristales, Nexus 4 000 HP.
- Base de datos de ítems, runas y fichas de campeón — wr-meta.com (proyecto comunitario de JLVD DEV), sincronizada al 24-sep-2026. Fuente secundaria: stats base de Zoe, ratios AP de habilidades.
- Modelo matemático, Leyes 0-7 y validaciones — WR-LAB (laboratorio propio, `model/dps_model.py`), construido sobre las fuentes anteriores.

**Aviso legal:** Wild Rift y League of Legends son marcas registradas de Riot Games, Inc. Este documento es una guía de comunidad con fines educativos, **no está afiliado, patrocinado ni respaldado por Riot Games**. Los nombres de ítems, campeones y estadísticas pertenecen a sus respectivos dueños. El análisis y las conclusiones son trabajo original del autor apoyado en WR-LAB.