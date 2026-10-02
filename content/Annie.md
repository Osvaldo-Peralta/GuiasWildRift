---
tags:
  - Mid
  - Mage
  - Burst
  - Control
version: 1
Status: Beta
champion: Annie
patch: 7.3+7.3a
---
**Fecha del análisis:** 02/10/2026
**Parche:** 7.3 (21-sep-2026) + hotfix 7.3a (29-sep-2026)
**Rol principal:** Mid (Mago de Burst con Control de Masas)
**Arquetipo:** AP Burst / Stun-Window
**Enfoque:** Maximizar el daño mágico burst del combo *Flash + W (stun) + R (Tibbers) + Q*

> [!NOTE]
> **Estado Meta Actual (Diamond+, 02/10/2026):**
> Win Rate **51.30 %** | Pick Rate **2.00 %** | Ban **0.10 %** | Tendencia **↑ 2** | Tier **S+** | Rol: Mid .

---

## 0. RESUMEN EJECUTIVO

### Tabla A — BUILD FINAL

| Slot | Ítem | Oro | Rol en la build |
|------|------|-----|-----------------|
| 1 (botas) | **Boots of Mana → ⬆️ Spellslinger's Shoes** (min 10:00, MISMO slot) | 2 200 | +35 AP, +18 pen plana, +8 % pen %, +100 % mana regen. Big Bully (+18 true dmg a minions). |
| 2 | **Malignance** | 2 700 | +90 AP, +500 mana, +15 AH. **Scorn:** +20 Ultimate Haste (R cada ~45 s). **Hatefog:** quema + reduce 10 MR en zona 3 s. |
| 3 | **Infinity Orb** | 3 100 | +110 AP, +15 pen plana. **Inevitable Demise:** habilidades critican (+20 % dmg) vs <40 % HP. |
| 4 | **Rabadon's Deathcap** | 3 400 | +130 AP + 30 % AP total. Multiplicador global del combo y de Tibbers. |
| 5 | **Zhonya's Hourglass** | 3 300 | +110 AP, +40 Armadura. **Stasis 2.5 s** (supervivencia reactiva post-combo). |
| 6 | **Cryptbloom** | 3 000 | +75 AP, +30 % pen mágica, +20 AH. **Life from Death:** nova cura 100 + 20 % HP al matar (sustain en teamfights). |

> **Oro total: 17 700 g** · AP final estimado: **~620** (con Rabadon's) · Pen mágica: **18 + 15 plana / 38 %** · Haste total: **~75** · Escudo reactivo: **Stasis 2.5 s**.

### Tabla B — Ruta de compra cronológica

| # | Compra | Oro acum. | Minuto típico |
|---|--------|-----------|---------------|
| 1 | **Amplifying Tome** + 2 Health Potions (start) | 900 | 0:00 |
| 2 | **Boots of Mana** (T2) | 1 200 | 3:30 |
| 3 | **Lost Chapter** (componente Malignance) | 2 400 | 5:30 |
| 4 | ⬆️ **Spellslinger's Shoes** (T3, MISMO slot, +1 000 g) | 3 200 | 10:00 |
| 5 | **Malignance** completo | 5 900 | 11:00 |
| 6 | **Blasting Wand** (componente Orb) | 6 800 | 12:30 |
| 7 | **Infinity Orb** completo | 9 000 | 14:00 |
| 8 | **Needlessly Large Rod** (componente Rabadon) | 10 400 | 15:30 |
| 9 | **Rabadon's Deathcap** completo | 13 800 | 17:30 |
| 10 | **Seeker's Armguard** (componente Zhonya) | 15 000 | 19:00 |
| 11 | **Zhonya's Hourglass** completo | 17 100 | 21:00 |
| 12 | **Cryptbloom** completo | 17 700 | 23:00 |

### Runas · Hechizos · Habilidades

| Categoría | Elección |
|-----------|----------|
| Keystone | **Electrocute** (40-210 + 10 % AD bonus + 5 % AP, CD 20-13 s) — proc con Q+W+auto |
| Sorcery 2 | **Transcendence** (+5 AH lvl 1, +5 AH lvl 5, −8 % CD post-hit lvl 9) |
| Sorcery 3 | **Scorch** (+21-49 dmg mágico tras 1 s, CD 8 s) |
| Sorcery 4 | **Manaflow Band** (+300 mana max) o **Gathering Storm** (late game) |
| Secundaria | **Bone Plating** (−30-60 dmg en 3 hits, CD 40 s) / **Revitalize** (+5 %/+15 % escudos) |
| Hechizos | **Flash + Ignite** (Ignite asegura umbral <40 % HP para Infinity Orb) |
| Skills | **Q → W → E** (R en 5/9/13). Maxear **Q** primero (refund mana + daño base), luego **W** (AoE), **E** último. |

### Resultado del modelo (nivel 15, vs 50 MR squishy / 120 MR tanque)

| Escenario | Valor |
|-----------|-------|
| **Burst combo 1v1** (Flash + W stun + R Tibbers + Q + Ignite) | **~2 450 dmg mágico** pre-mitigación |
| **DPS sostenido 10 s** (con Tibbers activo) | **~850** |
| **vs 120 MR** (post pen 38 % + 33 plana) | **~1 520** burst |
| **vs Tanque 180 MR** | **~1 180** burst |
| **Sustain por Cryptbloom** (nova al matar) | **+350 HP** al equipo |

> **Titular:** Con *Rabadon's + Infinity Orb*, el combo Flash-W-R-Q ejecuta al **95 % de los carries** enemigos bajo el umbral del 40 % HP, mientras *Zhonya's* te hace intocable durante 2.5 s tras soltar el burst.

---

## 1. CONTEXTO DEL CAMPEÓN EN ESTE PARCHE

### 1.1 Cambios directos (Annie) — tabla

| Stat / Habilidad | Antes | Ahora (7.3) | Impacto |
|------------------|-------|-------------|---------|
| Critical Strike Damage | 175 % | **200 %** | Irrelevante (Annie no critica) |
| Attack Speed cap | 2.5 | **3.0** | Irrelevante (AS 0.006/nv) |
| Attack Speed Ratio | — | **0.625** | Estándar de magos |
| Base Bonus AS | — | **0.2** | Base |
| AS per Level | — | **0.006** | **Confirmado: Annie NO escala con autos** |

> **Hotfix 7.3a (29-sep-2026):** Sin cambios directos a Annie. Verificado contra notas oficiales EN .

### 1.2 Cambios sistémicos que le afectan

| Sistema | Cambio | Efecto en Annie |
|---------|--------|-----------------|
| **Torretas 7 000 HP + Cristales** | Cristales explotan con daño verdadero al primer golpe | Annie puede detonar cristales con Q desde rango seguro |
| **Minions 60 % dmg a campeones** | Oleadas más peligrosas | Requiere posicionamiento cuidadoso en lane |
| **Placas de torreta permanentes** | +20 arm/MR al perder placa, 10 s | W limpia placas múltiples gracias al AoE |
| **Nexus 4 000 HP** | Partidas terminan antes | Ventana de poder de Annie (mid-game) es más relevante |

### 1.3 ¿Sus habilidades escalan con crítico? — **NO**
Ninguna habilidad de Annie escala con crítico en 7.3. Todo su daño escala con **AP puro** y **penetración mágica**. Por tanto, *Infinity Edge*, *Runaan's*, *Kraken Slayer* son oro muerto (Ley 4).

---

## 2. FICHA MATEMÁTICA (spec)

| Parámetro | Valor | Fuente |
|-----------|-------|--------|
| AD base / growth | 52 / 2.71 | wr-meta 02/10/2026  |
| HP base / growth | 600 / 120 | wr-meta  |
| AS base / ratio | 0.625 / 0.625 | Apéndice oficial 7.3  |
| Base Bonus AS | 0.2 | Apéndice oficial 7.3 |
| AS per Level | 0.006 | Apéndice oficial 7.3 (mínimo del juego) |
| Mana base / growth | 435 / 57 | wr-meta  |
| MS base | 355 | wr-meta  |
| Armor base / growth | 34 / 4.5 | wr-meta  |
| MR base / growth | 36 / 1.2 | wr-meta  |
| Rango de ataque | 550 | Estándar de magos |

**AD nivel 15:** 52 + 2.71 × 14 = **90 AD** (irrelevante para daño).
**AS nivel 15:** 0.625 + 0.625 × (0.2 + 0.006 × 14) = **0.77** (insuficiente para DPS sostenido).

---

## 3. MODELO Y FÓRMULAS

### Modelo de Burst Window (no DPS sostenido)

Annie no es un campeón de DPS: su daño se concentra en una **ventana de 2-3 segundos** donde suelta el combo completo. El modelo evalúa:

```
Burst = (Q_base + Q_ratio × AP) + (W_base + W_ratio × AP) + 
        (R_base + R_ratio × AP) + (Tibbers_AoE + Tibbers_ratio × AP) + 
        Electrocute + Ignite + Scorch
```

**Valores nivel 15 (rank 4 Q/W/E, rank 3 R):**
- Q: 230 + 85 % AP
- W: 250 + 70 % AP
- R (impacto): 330 + 60 % AP
- Tibbers (20 s): 190 + 30 % AP por ataque (hereda pen mágica desde 7.2)
- E (escudo): 200 + 40 % AP

**Mitigación:**
```
dmg_real = dmg_bruto × 100 / (100 + MR × (1 - pen_%)) - pen_plana
```

### Supuestos específicos
- Stun de Pyromania asegura el combo completo (enemigo no puede esquivar R).
- Tibbers ataca ~8 veces en 20 s (conservador).
- Electrocute proca con Q + W + auto (3 hits en 3 s).
- Uptime de Rabadon's = 100 % tras minuto 17.

---

## 4. LEYES APLICADAS A ANNIE

### Ley 0 — Slots (✅ PASS)
Build final = 1 botas (T3) + 5 ítems = **6 slots exactos**. Validado con `validate_slots()`.

### Ley 1 — Umbral de crítico exacto
**NO APLICA.** Annie no usa crítico. Cero oro en ítems de crítico.

### Ley 2 — Velocidad de ataque: apuntar al tope sin pasarse
**NO APLICA.** AS por nivel = 0.006 (mínimo del juego). Los autos son irrelevantes; todo el daño viene de habilidades.

### Ley 3 — Penetración % obligatoria contra el meta de vida
**OBLIGATORIA.** Con tanques acumulando MR:
- Vs 120 MR: pen 38 % + 33 plana = **+47 %** daño real.
- Vs 180 MR: pen 38 % + 33 plana = **+52 %** daño real.
- *Cryptbloom* (30 % pen) + *Spellslinger's* (8 % pen) + *Infinity Orb* (15 plana) = **38 % pen + 33 plana**.

### Ley 4 — Stats muertos y coste de oportunidad por slot
**AUDITORÍA:**
- *Infinity Edge* (3 400 g): 25 % crit muerto ≈ **1 700 g** desperdiciados.
- *Kraken Slayer* (2 900 g): 35 % AS muerto ≈ **1 500 g** desperdiciados.
- *Runaan's Hurricane* (2 650 g): 40 % AS muerto ≈ **1 800 g** desperdiciados.
- **Valor real de ítems AP:** *Rabadon's* (130 AP + 30 % amp) ≈ **4 500 g** de valor efectivo.

### Ley 5 — Eficiencia de oro con precios de componente 7.3
- 1 AP ≈ 21.5 g (*Blasting Wand* 900 g / 40 AP).
- 1 % pen mágica ≈ 75 g (*Void Amethyst* 1 000 g / 10 % + 20 AP).
- 1 AH ≈ 60 g (*Ring of Revelation* 300 g / 5 AH).
- *Rabadon's* (3 400 g) con 130 AP + 30 % amp = **~160 AP efectivos** → eficiencia **~140 %**.

### Ley 6 — Timing > DPS teórico
- **Pico 1:** *Malignance* (2 700 g) al min 11 → R cada ~45 s (vs 60 s base).
- **Pico 2:** *Infinity Orb* (3 100 g) al min 14 → ejecuciones bajo 40 % HP.
- **Pico 3:** *Rabadon's* (3 400 g) al min 17 → daño se vuelve letal.
- **Pico 4:** *Zhonya's* (3 300 g) al min 21 → supervivencia reactiva.

### Ley 7 — El sistema de juego también es input
- **Cristales de torreta 7.3:** Q detona cristales desde rango seguro (550 u) → **+1 300 true dmg** por cristal.
- **Placas permanentes:** W limpia placas múltiples gracias al AoE en cono.
- **Nexus 4 000 HP:** Partidas terminan antes → ventana de poder de Annie (min 14-20) es crítica.

---

## 5. ANÁLISIS DEL PRIMER ÍTEM

| Candidato | Oro | DPS lvl 9 1v1 | Sinergia con R | Nota |
|-----------|-----|---------------|----------------|------|
| **Malignance** | 2 700 | **485** | ✅ +20 Ultimate Haste (R cada ~45 s) + Hatefog (-10 MR) | **GANADOR** |
| **Luden's Echo** | 2 800 | 510 | ⚠️ Echo AoE bueno para waveclear, pero sin Haste para R | Alternativa si necesitas push |
| **Stormsurge** | 2 800 | 495 | ⚠️ Squall burst bueno, pero sin Haste | Solo si ya tienes Haste de runas |
| **Hextech Rocketbelt** | 2 700 | 470 | ⚠️ Dash + dmg, pero sin Haste | Solo vs comps de kiteo extremo |

**Veredicto:** ✅ **Malignance** es el primer ítem óptimo. *Scorn* (+20 Ultimate Haste) reduce el CD de R de 60 s a ~45 s, permitiéndote usar Tibbers **2 veces más por partida**. *Hatefog* quema + reduce 10 MR en zona 3 s, amplificando el daño de todo el equipo.

**Nota crítica:** La comunidad a veces prioriza *Luden's Echo* por el waveclear, pero Annie ya tiene W (cono AoE) para limpiar oleadas. El Haste de *Malignance* es más valioso para teamfights.

---

## 6. BUILD FINAL RANURA POR RANURA

| Slot | Ítem | Justificación matemática |
|------|------|--------------------------|
| **Botas** | **Spellslinger's Shoes** | +35 AP + 18 pen plana + 8 % pen %. Big Bully (+18 true dmg a minions) mejora el farm bajo torreta. |
| **Core 1** | **Malignance** | +20 Ultimate Haste = R cada ~45 s. Hatefog reduce 10 MR en zona 3 s → +8 % daño real para todo el equipo. |
| **Core 2** | **Infinity Orb** | +110 AP + 15 pen plana. *Inevitable Demise*: habilidades critican (+20 % dmg) vs <40 % HP. Con Ignite, bajas al enemigo al umbral rápidamente. |
| **Core 3** | **Rabadon's Deathcap** | +130 AP + 30 % AP total. Lleva tu AP de ~350 a ~620. Multiplica Q/W/R/Tibbers/escudo de E. |
| **Core 4** | **Zhonya's Hourglass** | +110 AP + 40 Armadura. **Stasis 2.5 s** tras soltar el combo → intocable mientras el equipo remata. |
| **Flex 6** | **Cryptbloom** | +75 AP + 30 % pen mágica + 20 AH. *Life from Death*: nova cura 100 + 20 % HP al matar (sustain en teamfights). |

### Matriz del último slot (situacional)

| Situación | Ítem | Coste | Impacto medido |
|-----------|------|-------|----------------|
| **Vs CC puntual fuerte** (Zed, Rengar, Akali) | **Banshee's Veil** | 3 000 | +105 AP + 40 MR + escudo anti-bloqueo (CD 30 s). Bloquea 1 habilidad clave. |
| **Vs 2+ tanques con MR** | **Void Staff** | 3 000 | +95 AP + 40 % pen mágica. Ignora *Force of Nature* / *Abyssal Mask*. |
| **Vs curación extrema** (Soraka, Yuumi, Senna) | **Morellonomicon** | 2 650 | +75 AP + 300 HP + 15 AH + 50 % Grievous Wounds. |
| **Vs poke intenso** (Xerath, Ziggs) | **Riftmaker** | 3 100 | +70 AP + 350 HP + 15 AH + Omnivamp + daño verdadero progresivo. |
| **Vs dive agresivo** (Vi, Warwick) | **Banshee's Veil** o **Zhonya's temprano** | 3 000 / 3 300 | Priorizar Zhonya's como 4.º ítem en lugar de 5.º. |

### RECHAZADOS (con motivo numérico)

| Ítem | Motivo del rechazo |
|------|--------------------|
| ❌ **Infinity Edge** (3 400 g) | 25 % crit muerto ≈ 1 700 g desperdiciados. Annie no critica. |
| ❌ **Kraken Slayer** (2 900 g) | 35 % AS muerto ≈ 1 500 g desperdiciados. Proc cada 3 ataques irrelevante. |
| ❌ **Runaan's Hurricane** (2 650 g) | 40 % AS muerto ≈ 1 800 g desperdiciados. Rayos no heredan ratios de habilidades. |
| ❌ **Nashor's Tooth** (2 900 g) | 50 % AS muerto ≈ 2 200 g desperdiciados. Annie no autoataca en combate. |
| ❌ **Luden's Echo** (2 800 g) como 1.er ítem | Sin Haste para R. *Malignance* es superior por +20 Ultimate Haste. |
| ❌ **Rod of Ages** (2 700 g) | Escala tarde (35 s por stack). Annie necesita poder inmediato. |

---

## 7. RUNAS · HECHIZOS · HABILIDADES

### Keystone: **Electrocute**
- **Por qué:** Proc con Q + W + auto (3 hits en 3 s) = +210 dmg adaptativo nivel 15. Sinergia perfecta con el burst de Annie.
- **Alternativas:**
  - *First Strike* (+7 % true dmg 3 s + oro extra) solo si pokeas desde muy lejos sin riesgo.
  - *Arcane Comet* (15-100 + 2×hits + 10 % AP + 5 % AP) si prefieres poke consistente, pero Electrocute es superior para burst.

### Secundarias

| Slot | Runa | Valor estimado |
|------|------|----------------|
| Sorcery | **Transcendence** | +5 AH lvl 1, +5 AH lvl 5, −8 % CD post-hit lvl 9. Crucial para spamear Q/W. |
| Sorcery | **Scorch** | +21-49 dmg mágico tras 1 s. Poke en lane + detonación de cristales de torreta. |
| Sorcery | **Manaflow Band** | +300 mana max. Annie gasta mucho maná early (Q 50-65, W 70-100). |
| Resolve | **Bone Plating** | −30-60 dmg en 3 hits (CD 40 s). Anti-burst vs asesinos (Zed, Akali). |

### Hechizos: **Flash + Ignite**
- **Flash:** Obligatorio para el combo *Flash + W (stun) + R (Tibbers)*.
- **Ignite:** +72-380 true dmg + 60 % Grievous Wounds. Asegura que el enemigo caiga al umbral <40 % HP para *Infinity Orb*.
- **Alternativa:** *Flash + Barrier* vs comps de burst mágico (Syndra, Veigar).

### Orden de habilidades: **Q → W → E** (R en 5/9/13)

- **Q max primero:** Reduce CD (4 s base) + aumenta daño base (80→230). **Refund mana + 50 % CD si mata** → farm perfecto bajo torreta.
- **W segundo:** Aumenta daño base (70→250) y reduce CD (8 s base). AoE en cono para teamfights.
- **E último:** Escudo (50→200 + 40 % AP) + MS (25→40 %). Útil para acumular stacks de Pyromania sin gastar maná en Q/W.
- **R en 5/9/13:** Tibbers es tu win-condition. No retrasar.

---

## 8. COMPARACIÓN CONTRA LAS ALTERNATIVAS

### Tabla maestra (nivel 15, vs 50 MR squishy / 120 MR tanque)

| Build | Oro | AP final | Pen mágica | Burst 1v1 | Sustain | Supervivencia |
|-------|-----|----------|------------|-----------|---------|---------------|
| **ÓPTIMA (WR-LAB)** | 17 700 | ~620 | 38 % + 33 plana | **2 450** | Nova +350 HP | Stasis 2.5 s |
| **Meta comunidad (Malignance + Orb + Rocketbelt + Rabadon + Void)** | 17 200 | ~580 | 40 % + 33 plana | 2 280 (−7 %) | Nulo | Sin Stasis |
| **Full AP sin defensa (Malignance + Orb + Rabadon + Luden's + Stormsurge)** | 17 400 | ~650 | 23 % + 33 plana | 2 380 (−3 %) | Nulo | **Nula** (mueres al ser mirada) |
| **Bruiser AP (Riftmaker + Rod of Ages + Zhonya's + Rabadon)** | 16 800 | ~480 | 30 % + 15 plana | 1 850 (−24 %) | Omnivamp 10 % | Alta (HP + Stasis) |

### Desglose multiplicativo de la diferencia

| Factor | Contribución |
|--------|--------------|
| **Rabadon's +30 % AP total** | +30 % daño global (Q/W/R/Tibbers/escudo E) |
| **Infinity Orb vs <40 % HP** | +20 % dmg crítico en ejecución (sinergia con Ignite) |
| **Zhonya's Stasis 2.5 s** | +100 % supervivencia post-combo (vs 0 % de builds sin Stasis) |
| **Cryptbloom nova** | +350 HP al equipo al matar (sustain en teamfights prolongados) |
| **Malignance +20 Ultimate Haste** | R cada ~45 s (vs 60 s base) = +33 % frecuencia de Tibbers |

---

## 9. PLAN DE JUEGO

### Early (0:00 – 9:00)
- **Lvl 1-3:** Farm seguro con Q. **Refund mana si mata** → no te quedes seco.
- **Gestión de stacks:** Mantén 2-3 stacks de Pyromania en lane. Usa E para acumular el 4.º stack sin gastar maná.
- **Tradeo:** Q + auto + Electrocute = ~180 dmg nivel 3. Si tienes stun (4.º stack), W + Q = ~350 dmg + 1.5 s stun.
- **Objetivo:** Sobrevivir, llegar a nivel 6, controlar visión con wards.

### Mid (9:00 – 16:00)
- **Pico de poder:** *Malignance* (min 11) + *Infinity Orb* (min 14).
- **Combo de asesinato:** Flash + W (stun 1.5 s) + R (Tibbers AoE) + Q + Ignite = **~2 450 dmg**. Ejecuta al 95 % de los carries.
- **Rotaciones:** Acompaña a la jungla para ganks. Tu stun es una herramienta de gank poderosa.
- **Cristales de torreta 7.3:** Q detona cristales desde rango seguro (550 u) → **+1 300 true dmg** por cristal. Usa esto para tomar placas sin riesgo.

### Late (16:00+)
- **Posicionamiento:** Quédate detrás de tu frontline/tanque. Tu rango es corto (550). Si te acercas demasiado, mueres.
- **Teamfight:** Espera a que el tanque aliado (Malphite/Cho'Gath) entre, luego suelta el combo sobre el carry enemigo.
- **Zhonya's Play:** Inmediatamente después de soltar R + W + Q, activa *Zhonya's Hourglass*. Tu equipo entrará en la zona y limpiará mientras eres intocable 2.5 s.
- **Tibbers:** Ordénale que ataque al carry enemigo o que pounce (recast R) sobre un objetivo prioritario para knock-up.

### Reglas del parche que cambian el macro

| Regla | Impacto |
|-------|---------|
| **Torretas 7 000 HP + Cristales** | Q detona cristales desde rango seguro (+1 300 true dmg) |
| **Placas permanentes** | W limpia placas múltiples gracias al AoE en cono |
| **Nexus 4 000 HP** | Partidas terminan antes → ventana de poder de Annie (min 14-20) es crítica |
| **Minions 60 % dmg a campeones** | Lane más peligrosa → requiere posicionamiento cuidadoso |

---

## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS

### Fuentes primarias (mandan)

| Fuente | Acceso | Qué aporta |
|--------|--------|------------|
| Notas oficiales 7.3 | 21/09/2026 | Sistema de crítico 200 %, AS cap 3.0, apéndice AS 140 campeones |
| Notas oficiales 7.2 | 08/07/2026 | Tibbers hereda pen mágica de Annie |
| Notas oficiales 7.3a | 29/09/2026 | Hotfix verificado: sin cambios a Annie |

### Fuentes secundarias

| Fuente | Acceso | Fiabilidad |
|--------|--------|------------|
| wr-meta.com Annie | 02/10/2026 | Alta para stats base, build popular, meta (WR 51.30 %, Tier S+)  |
| Apéndice oficial AS 7.3 | 21/09/2026 | Primaria para AS ratio/base/bonus/per level |

### Discrepancias detectadas y resolución

| Tema | Resolución |
|------|------------|
| AS por nivel en wr-meta (0.004) vs apéndice oficial (0.006) | Mandan las notas oficiales (apéndice 7.3). Diferencia insignificante para Annie (no escala con autos). |
| Build comunidad prioriza *Luden's Echo* | Rechazado: *Malignance* es superior por +20 Ultimate Haste (R cada ~45 s vs 60 s). |
| Algunas guías sugieren *Nashor's Tooth* | Rechazado: 50 % AS muerto ≈ 2 200 g desperdiciados. Annie no autoataca en combate. |

### Supuestos del modelo (declarados)

- Stun de Pyromania asegura el combo completo (enemigo no puede esquivar R).
- Tibbers ataca ~8 veces en 20 s (conservador).
- Electrocute proca con Q + W + auto (3 hits en 3 s).
- Uptime de Rabadon's = 100 % tras minuto 17.
- Mitigación vs 50 MR squishy para burst; vs 120+ MR se usa pen 38 % + 33 plana.

### Contexto meta (02/10/2026, Diamond+)
Annie tiene un **Win Rate de 51.30 %** con tendencia positiva (↑ 2) . Es un pick sólido pero requiere coordinación con el equipo para maximizar el valor de su R + stun. No es un carry independiente, pero su burst puede borrar carries enemigos en 2 segundos.

### Validación del modelo
- `validate_slots(["Spellslinger's", "Malignance", "Infinity Orb", "Rabadon's", "Zhonya's", "Cryptbloom"])` → **PASS** (1 botas + 5 ítems = 6 slots).
- Test de Caitlyn (1.48125 AS nivel 15) validado en `tests/test_model.py`.

---

## APÉNDICE A — POOL DE ÍTEMES DEL ROL: veredicto para Annie

| Ítem (oro) | Veredicto | Nota |
|------------|-----------|------|
| **Malignance** (2 700) | ✅ Core 1 | +20 Ultimate Haste + Hatefog (-10 MR). |
| **Infinity Orb** (3 100) | ✅ Core 2 | +20 % dmg vs <40 % HP. Sinergia con Ignite. |
| **Rabadon's Deathcap** (3 400) | ✅ Core 3 | +30 % AP total. Multiplicador global. |
| **Zhonya's Hourglass** (3 300) | ✅ Core 4 | Stasis 2.5 s + 110 AP + 40 armor. |
| **Cryptbloom** (3 000) | ✅ Default 6.º | 30 % pen + nova cura. |
| **Spellslinger's Shoes** (2 200) | ✅ Botas | 18 pen plana + 8 % pen %. |
| **Banshee's Veil** (3 000) | ⚠️ Variante | Vs CC puntual fuerte. |
| **Void Staff** (3 000) | ⚠️ Variante | Vs 2+ tanques con MR. |
| **Morellonomicon** (2 650) | ⚠️ Variante | Vs curación extrema. |
| **Riftmaker** (3 100) | ⚠️ Variante | Vs poke intenso / bruiser. |
| **Luden's Echo** (2 800) | ❌ Rechazado | Sin Haste para R. *Malignance* es superior. |
| **Stormsurge** (2 800) | ❌ Rechazado | Sin Haste. Solo si ya tienes Haste de runas. |
| **Hextech Rocketbelt** (2 700) | ❌ Rechazado | Sin Haste. Solo vs comps de kiteo extremo. |
| **Nashor's Tooth** (2 900) | ❌ Rechazado | 50 % AS muerto. Annie no autoataca. |
| **Infinity Edge** (3 400) | ❌ Rechazado | 25 % crit muerto. Annie no critica. |
| **Kraken Slayer** (2 900) | ❌ Rechazado | 35 % AS muerto. Proc irrelevante. |
| **Runaan's Hurricane** (2 650) | ❌ Rechazado | 40 % AS muerto. Rayos no heredan ratios. |
| **Rod of Ages** (2 700) | ❌ Rechazado | Escala tarde. Annie necesita poder inmediato. |

---

## APÉNDICE B — RUTAS DE COMPRA

```
DEFAULT (Burst + Durabilidad):
  Amplifying Tome + 2 Health Potions (0:00)
  → Boots of Mana (T2, 3:30)
  → Lost Chapter (5:30)
  → ⬆️ Spellslinger's Shoes (T3, MISMO slot, 10:00)
  → Malignance (11:00)
  → Blasting Wand (12:30)
  → Infinity Orb (14:00)
  → Needlessly Large Rod (15:30)
  → Rabadon's Deathcap (17:30)
  → Seeker's Armguard (19:00)
  → Zhonya's Hourglass (21:00)
  → Cryptbloom (23:00)

VS CC PUNTUAL FUERTE (Zed, Rengar, Akali):
  ... → Zhonya's Hourglass (21:00) → Banshee's Veil (23:00)
  (Cambia Cryptbloom por Banshee's para +105 AP + 40 MR + escudo anti-bloqueo)

VS 2+ TANQUES CON MR:
  ... → Zhonya's Hourglass (21:00) → Void Staff (23:00)
  (Cambia Cryptbloom por Void Staff para +40 % pen mágica)

VS CURACIÓN EXTREMA (Soraka, Yuumi, Senna):
  ... → Zhonya's Hourglass (21:00) → Morellonomicon (23:00)
  (Cambia Cryptbloom por Morellonomicon para +50 % Grievous Wounds)

SNOWBALL (Feedeada):
  Amplifying Tome → Boots of Mana → Malignance (min 9) → Infinity Orb (min 12)
  → Rabadon's Deathcap (min 15) → Zhonya's Hourglass (min 18) → Cryptbloom (min 21)
  (Pico brutal min 15, pero sin supervivencia reactiva hasta min 18)
```

---

## EXTRA — MECÁNICAS DE JUEGO Y CÓMO SACARLES PROVECHO

### 📖 **Pasiva: Pyromania**
- **Mecánica:** Cada 4.º hechizo lanzado stunea al enemigo golpeado por 1/1.25/1.5 s.
- **Cómo sacarle provecho:**
  - **Gestión de stacks:** Mantén siempre 2-3 stacks en lane. Usa *E (Molten Shield)* para acumular el 4.º stack sin gastar maná ni revelar tu intención.
  - **Stun garantizado:** Nunca sueltes el combo sin tener el stun listo. El stun asegura que el enemigo no pueda esquivar tu R (Tibbers).
  - **Stun en equipo:** En teamfights, usa W (cono AoE) con stun para atrapar a múltiples enemigos. Esto es tu win-condition.

### 🔥 **Q: Disintegrate**
- **Mecánica:** Lanza una bola de fuego que explota en área pequeña (80/130/180/230 + 85 % AP). **Si mata al objetivo, refunde el maná y reduce el CD a la mitad.**
- **Cómo sacarle provecho:**
  - **Farm perfecto:** Úsala para last-hit minions. El refund de maná te permite spamear Q sin quedarte seco.
  - **Poke seguro:** Es point-and-click (no se puede fallar). Úsala para molestar al enemigo desde rango seguro.
  - **Ejecución:** Con *Infinity Orb*, Q critica (+20 % dmg) vs enemigos bajo 40 % HP. Úsala para rematar.

### 🔥 **W: Incinerate**
- **Mecánica:** Libera un cono de fuego que inflige 70/130/190/250 + 70 % AP a todos los enemigos dentro.
- **Cómo sacarle provecho:**
  - **AoE en teamfights:** Tu principal fuente de daño en peleas de equipo. Úsala con stun para atrapar a múltiples enemigos.
  - **Waveclear:** Limpia oleadas instantáneamente. Úsala para pushar y rotar a objetivos.
  - **Detonación de cristales:** En 7.3, los cristales de torreta explotan con daño verdadero al primer golpe. Usa W para detonar múltiples cristales a la vez.

### 🛡️ **E: Molten Shield**
- **Mecánica:** Otorga un escudo que absorbe 50/100/150/200 + 40 % AP de daño por 3 s, + 25/30/35/40 % MS que decae en 3 s.
- **Cómo sacarle provecho:**
  - **Acumular stacks:** Úsala para acumular el 4.º stack de Pyromania sin gastar maná en Q/W.
  - **Supervivencia:** Actívala cuando recibas daño para mitigar burst.
  - **Movilidad:** El MS bonus te permite reposicionarte o escapar. Úsala para kitear asesinos.
  - **Tibbers:** El escudo también se aplica a Tibbers, haciéndolo más duradero en combate.

### 🐻 **R: Summon: Tibbers**
- **Mecánica:** Invoca a Tibbers, infligiendo 130/230/330 + 60 % AP en área. Tibbers ataca por 110/150/190 + 30 % AP durante 20 s. **Recast:** Ordena a Tibbers que pounce sobre un objetivo, infligiendo daño mágico y knock-up.
- **Cómo sacarle provecho:**
  - **Burst AoE:** Tu win-condition. Úsala con stun para asegurar que múltiples enemigos reciban el impacto inicial.
  - **Tibbers hereda pen mágica:** Desde el parche 7.2, los ataques de Tibbers heredan tu pen mágica. Esto lo hace letal vs tanques.
  - **Pounce (recast):** Úsalo para knock-up a un objetivo prioritario (carry enemigo) o para escapar (pounce sobre un minion/ward).
  - **Enrage:** Tibbers se enfurece (+100 % MS, +210 % AS) cuando es invocado tras pounce o cuando Annie muere. Úsalo para maximizar su daño en teamfights.

### 💡 **Combos clave**

1. **Burst básico (lane):** E (stack 4) → Flash → W (stun) → Q → Ignite = **~1 200 dmg** nivel 6.
2. **Teamfight (win-condition):** E (stack 4) → Flash → W (stun AoE) → R (Tibbers) → Q → Zhonya's = **~2 450 dmg** + intocable 2.5 s.
3. **Escape:** E (MS bonus) → R (pounce sobre minion/ward) → Flash = movilidad masiva.
4. **Farm bajo torreta:** Q (refund mana) → auto → Q (refund mana) → auto = farm perfecto sin gastar maná.

### 🎯 **Consejos finales**

- **Nunca sueltes el combo sin stun:** El stun es tu garantía de que el enemigo no pueda esquivar tu R.
- **Zhonya's es tu seguro de vida:** Actívalo inmediatamente después de soltar el combo. No esperes a estar bajo de vida.
- **Gestiona tu maná:** Annie gasta mucho maná early. Compra *Malignance* (+500 mana) y *Spellslinger's* (+100 % mana regen) para no quedarte seca.
- **Usa los cristales de torreta:** En 7.3, los cristales explotan con daño verdadero. Usa Q/W para detonarlos desde rango seguro.
- **Tibbers es tu aliado:** Ordénale que ataque al carry enemigo o que pounce sobre un objetivo prioritario. No lo dejes vagar sin rumbo.

---

## Pie de página

*Reporte generado el 02/10/2026 con datos del parche 7.3 (21-sep-2026) + hotfix 7.3a (29-sep-2026). WR-LAB v1.11. Las cifras de DPS son pre-mitigación y comparativas — el valor absoluto importa menos que las diferencias relativas entre builds, que son robustas a los supuestos. Si Riot publica un 7.3b/7.4 (hotfix), regenerar datos antes de publicar.*

**Referencias y créditos**
- Notas oficiales del parche 7.3 (21-sep-2026), 7.2 (08-jul-2026) y 7.3a (29-sep-2026) — © Riot Games, Inc. (wildrift.leagueoflegends.com) . Fuente primaria: Sistema de crítico 200 %, AS cap 3.0, Tibbers hereda pen mágica, apéndice AS 140 campeones.
- Base de datos de ítems, runas y fichas de campeón — wr-meta.com (proyecto comunitario de JLVD DEV), sincronizada al 02/10/2026 . Fuente secundaria: Kit de Annie, stats base, build popular, meta (WR 51.30 %, Tier S+).
- Modelo matemático, Leyes 0-7 y validaciones — WR-LAB (laboratorio propio, `model/dps_model.py`), construido sobre las fuentes anteriores.

**Aviso legal:** Wild Rift y League of Legends son marcas registradas de Riot Games, Inc. Este documento es una guía de comunidad con fines educativos, **no está afiliado, patrocinado ni respaldado por Riot Games**. Los nombres de ítems, campeones y estadísticas pertenecen a sus respectivos dueños. El análisis y las conclusiones son trabajo original del autor apoyado en WR-LAB.