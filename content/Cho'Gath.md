---
tags:
- Barón
- Jungla
---
**Fecha del análisis:** 26 de septiembre de 2026
**Parche analizado:** 7.3 (lanzamiento oficial: 21 de septiembre de 2026)
**Metodología:** notas oficiales del parche 7.3 y 7.2, base de datos de ítems/runas actualizada al 24-sep-2026 (wr-meta.com), y modelo propio `wr-lab/model/dps_model.py` con spec `chogath`.
**Enfoque:** Maximización de escalado infinito mediante *Feast* (R) y *Heartsteel*, convirtiendo el tamaño en daño verdadero (% vida) y durabilidad extrema para Top y Jungla.

## 0. RESUMEN EJECUTIVO

**Órden de compra (Ruta Coloso):**

| #   | Ítem                  | Oro  | Momento típico | Justificación Breve                                                                                   |
| --- | --------------------- | ---- | -------------- | ----------------------------------------------------------------------------------------------------- |
| 1   | **Heartsteel**        | 3000 | ~8:00–9:00     | Escalado infinito de HP + daño por % vida máxima. Core del build.                                     |
| 2   | **Plated Steelcaps**  | 1200 | ~9:30–10:00    | Reducción de daño de autos (bloquea 10%) esencial para lanear contra ADCs/Fighters AD.                |
| 3   | **Hollow Radiance**   | 2800 | ~12:00–13:00   | Daño mágico en área basado en HP bonus + resistencia mágica. Sinergia perfecta con Heartsteel.        |
| 4   | **Liandry's Torment** | 3000 | ~15:00–16:00   | Quemadura por % vida máxima. Multiplica el daño de E y pasiva de Heartsteel.                          |
| 5   | **Force of Nature**   | 2800 | ~18:00–19:00   | Resistencia mágica escalable + velocidad de movimiento. Durabilidad contra AP.                        |
| 6   | **Warmog's Armor**    | 2850 | ~21:00+        | Regeneración masiva fuera de combate (>950 HP bonus) para mantener presión de mapa sin volver a base. |

>**Total de oro:** ~15,650g (sin contar botas T3 si se prefiere ahorrar para un 7º slot defensivo situacional, aunque en WR son 6 slots totales).

**Runas:** Grasp of Undying · Demolish · Second Wind · Overgrowth · Transcendence · Axiom Arcanist.

**Hechizos:** Flash + Ignite (Top) / Smite + Flash (Jungla).
**Orden de habilidades:** Maxear **E (Vorpal Spikes)** primero para clear y poke, luego **Q (Rupture)** para CC, y **W (Feral Scream)** al final. R siempre que esté disponible.

**Resultado del modelo:** A nivel 15 con 6 stacks de Feast + Heartsteel completo, Cho'Gath supera los **4,500–5,000 HP**. El daño de E escala con % vida máxima del enemigo, mientras que el daño de Heartsteel y Liandry escala con tu propia vida bonus. Es una máquina de sitio y teamfight que no muere fácilmente.

## 1. CONTEXTO DEL CAMPEÓN EN ESTE PARCHE

*   **Nerfs/Buffs Directos (7.3):**
    *   **Sistema de Crítico:** Daño crítico base subió a 200% (no afecta directamente a Cho, pero sí a sus oponentes ADC).
    *   **Tope de AS:** Subió a 3.0. Cho tiene bajo ratio de AS (0.625) y bajo crecimiento (0.008), por lo que no se beneficia tanto de ítems de AS como otros fighters.
    *   **Cambios en Jungla:** El daño de Smite ahora escala con stats defensivos y ofensivos. Los monstruos grandes pegan con % de vida actual. Esto hace que Cho sea un jungler viable gracias a su alto HP y sustain pasivo.
    *   **Torretas:** 7000 HP y placas permanentes. *Demolish* es crucial para aprovechar las placas. *Crystalline Overgrowth* permite a Cho hacer daño verdadero a torres con solo un autoataque tras acumular cristales.

*   **¿Sus habilidades escalan con crítico?** No. Cho'Gath es un mago/tank híbrido. Su daño proviene de ratios AP y % de vida.

## 2. FICHA MATEMÁTICA (Spec)

*   **AD Base/Crecimiento:** 62 (+4.0 por nivel). Nivel 15: ~118 AD.
*   **AS Base/Ratio/Bonus Base/Por Nivel:** 0.625 / 0.625 / 0.28 / 0.008.
    *   *Nota:* El crecimiento de AS es muy bajo. A nivel 15, el bonus por niveles es mínimo (~0.112 total). No es un campeón de AS.
*   **Vida/Armadura/RM:**
    *   Vida Base: 690 (+128 por nivel). Nivel 15: ~2,482 HP base.
    *   Armadura Base: 46 (+4.5 por nivel).
    *   RM Base: 40 (+2 por nivel).
*   **Modificadores del Auto:**
    *   **E (Vorpal Spikes):** Los siguientes 3 ataques lanzan picos que hacen daño mágico en cono y ralentizan. El daño incluye un % de la vida máxima del objetivo (2.3–3.5% + 0.6% por stack de Feast). Esto convierte a Cho en un "tank killer" natural.
*   **Pasiva (Carnivore):** Recupera vida y maná al matar unidades. Doble si es campeón/torre/épico. Sustento clave para la línea.
*   **R (Feast):** Daño verdadero basado en % vida bonus de Cho. Si mata, gana stack permanente de HP (+80/120/160) y tamaño.

## 3. MODELO Y FÓRMULAS

El modelo para Cho'Gath no se centra en DPS de autos sostenido (como Jinx), sino en **Daño por Ventana (Burst/AoE)** y **Durabilidad Eficiente**.

*   **Daño de E (Vorpal Spikes):** `Daño_Base + (AP_Ratio) + (%_Vida_Enemigo)`.
    *   A nivel 15, rank 4: `95 + 30% AP + (3.5% + 0.6% * Stacks_Feast) * Vida_Max_Enemigo`.
    *   Contra un tanque de 4000 HP con 6 stacks de Feast: `~95 + 30% AP + (3.5 + 3.6)% * 4000 = ~95 + 30% AP + 284`. Daño significativo sin construir daño puro.
*   **Daño de Heartsteel:** `140 + 3.5% Vida_Max_Propia`.
    *   Con 4500 HP: `140 + 157.5 = ~297` daño físico adicional en el auto cargado.
*   **Mitigación de Daño:**
    *   Cho construye HP masivo. La efectividad de la armadura/RM aumenta con el HP.
    *   `Daño_Real = Daño_Bruto * (100 / (100 + Resistencia))`.
    *   Al tener mucho HP, cada punto de resistencia vale más oro.

## 4. LEYES APLICADAS A CHO'GATH

*   **Ley 1 (Crítico):** Irrelevante. Cho no usa crítico. Se descargan ítems como IE, LDR, Mortal.
*   **Ley 2 (Velocidad de Ataque):** Irrelevante. Cho no necesita AS. Ítems como Kraken, Runaan, RFC son desperdicio. Se priorizan stats de utilidad y supervivencia.
*   **Ley 3 (Penetración):** Cho hace daño mágico y verdadero. La penetración mágica (Void Staff/Cryptbloom) puede ser útil si se va por ruta AP pura, pero en esta build "Coloso", el daño porcentual (% vida) ignora resistencias en parte. Liandry aplica quemadura que también es % vida.
*   **Ley 4 (Stats Muertos):**
    *   **AD:** Poco valor. Solo sirve para last hit early.
    *   **AS:** Valor nulo.
    *   **Maná:** Útil para spam de Q/E, pero Cho tiene buen sustain de maná con pasiva y items como Frozen Heart si se necesita.
    *   **HP:** Stat rey. Cada punto de HP aumenta daño de R, Heartsteel, y durabilidad.
*   **Ley 5 (Eficiencia de Oro):**
    *   **Heartsteel (3000g):** Muy eficiente si se juega para escalar. El daño extra y el HP permanente justifican el coste.
    *   **Hollow Radiance (2800g):** Excelente eficiencia para tanques AP. Daño en área basado en HP bonus.
    *   **Liandry (3000g):** Estándar para magos de batalla. Sinergia con E y W.
*   **Ley 6 (Timing):** Heartsteel requiere tiempo para cargar. Early game Cho es débil en daño burst. Se debe jugar seguro hasta tener 1-2 stacks de Feast y Heartsteel completado.
*   **Ley 7 (Sistema de Juego):**
    *   **Crystalline Overgrowth:** Cho puede detonar cristales de torre con su rango extendido por Feast.
    *   **Jungla 7.3:** Smite escala con HP bonus. Cho con mucho HP hará más daño verdadero con Smite a objetivos épicos.

## 5. ANÁLISIS DEL PRIMER ÍTEM

| Candidato | Oro | Pros | Contras | Veredicto |
| :--- | :--- | :--- | :--- | :--- |
| **Heartsteel** | 3000 | Escalado infinito HP/Daño. Sinergia con kit. | Requiere estar cerca para cargar. Débil early. | ✅ **CORE** |
| **Liandry's** | 3000 | Daño consistente % vida. Buen clear. | Menos durabilidad. Sin escalado infinito de HP. | ⚠️ Alternativa AP |
| **Iceborn Gauntlet** | 3000 | Control de zona (slow en área). Mana. | Menos daño que Heartsteel/Liandry. | ❌ Pasivo de moda |
| **Sunfire Aegis** | 2900 | Daño en área constante. | Ya no tiene stacks de Flametouch. Heartsteel es superior. | ❌ Outdated |

**Veredicto:** **Heartsteel** es la elección obligatoria para el enfoque "Coloso". Define la identidad del build.

## 6. BUILD FINAL RANURA POR RANURA

| Slot | Ítem | Justificación Matemática |
| :--- | :--- | :--- |
| Botas | **Plated Steelcaps** | Reduce 10% daño de autos. Esencial para sobrevivir a ADCs y Fighters AD en lane/jungla. |
| 1 | **Heartsteel** | Core del build. Aumenta HP máximo y daño de autos basado en % HP. Escalado infinito. |
| 2 | **Hollow Radiance** | Daño mágico en área basado en HP bonus. Sinergia directa con Heartsteel. Aporta RM. |
| 3 | **Liandry's Torment** | Aplica quemadura % vida máxima. Sinergia con E (Vorpal Spikes) y W. Aporta HP y AP. |
| 4 | **Force of Nature** | Alta RM escalable con stacks. Movilidad para alcanzar enemigos. Sinergia con HP masivo. |
| 5 | **Warmog's Armor** | Regeneración masiva fuera de combate si tienes >950 HP bonus (fácil de lograr). Permite presión constante sin volver a base. |
| 6 (Situacional) | **Spirit Visage** | Si el equipo enemigo tiene mucha curación/AP. Amplifica la regeneración de Warmog y pasiva. |
| 6 (Situacional) | **Thornmail** | Si el enemigo tiene mucho AD/Lifesteal. Refleja daño y aplica GW. |
| 6 (Situacional) | **Frozen Heart** | Si el enemigo depende de AS (ADCs). Reduce AS enemiga en área. |

**Ítems Rechazados:**
*   **Kraken Slayer/Runaan's:** Stats muertos (AS/Crit).
*   **Infinity Edge:** Stats muertos (Crit/AD).
*   **Rabadon's Deathcap:** Demasiado frágil. Cho necesita sobrevivir para aplicar su daño porcentual.
*   **Zhonya's Hourglass:** Útil, pero Force of Nature/Warmog ofrecen más valor estadístico continuo.

## 7. RUNAS · HECHIZOS · HABILIDADES

**Runas:**
*   **Keystone:** **Grasp of Undying**. Daño mágico basado en % vida, cura y HP permanente. Sinergia perfecta con el escalado de Cho.
*   **Secundarias (Resolve):**
    *   **Demolish:** Daño extra a torres. Sinergia con Crystalline Overgrowth y el push de Cho.
    *   **Second Wind:** Sustain en lane contra poke.
    *   **Overgrowth:** HP permanente adicional. Más HP = más daño de R y Heartsteel.
*   **Secundarias (Sorcery):**
    *   **Transcendence:** Ability Haste. Cho necesita spamear Q/E.
    *   **Axiom Arcanist:** Reduce CD de R al conseguir kills/asists. Más R = más stacks de Feast = más tamaño/daño.

**Hechizos:**
*   **Top:** Flash + Ignite (para asegurar kills y aplicar GW) o Teleport (para macro/push).
*   **Jungla:** Smite + Flash.

**Orden de Habilidades:**
1.  **E (Vorpal Spikes):** Maxear primero. Daño en área, slow, y % vida del enemigo. Fundamental para clear de jungla y waveclear en lane.
2.  **Q (Rupture):** Segundo. CC principal (knock-up).
3.  **W (Feral Scream):** Último. Silencio útil, pero menos daño/clear.
4.  **R (Feast):** Siempre que esté disponible. Priorizar stacks en minions/monstruos grandes si no se puede asegurar kill en campeón.

## 8. COMPARACIÓN CONTRA LAS ALTERNATIVAS

| Build | Oro | HP Est. (Lvl 15 + 6 Stacks) | Daño Principal | Durabilidad | Claridad de Rol |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Coloso (Esta Build)** | ~15.6k | ~4,800 - 5,200 | % Vida (E, Heartsteel, Liandry) | Extrema (HP + Resistencias) | Tank Magico / Scaling |
| **AP Burst (Full AP)** | ~16k | ~3,000 | Burst Q/R (Alto ratio AP) | Baja (Frágil) | Asesino Magico |
| **Tank Puro (Sunfire/Thorns)** | ~14k | ~4,500 | Daño Fijo/Moderado | Alta (Armadura/RM) | Tanque Frontal |
| **On-Hit (Nashor/Wits)** | ~15k | ~3,500 | Daño Autoatque | Media | Fighter Hibrido |

**Desglose:** La build Coloso sacrifica burst instantáneo por daño sostenido porcentual y durabilidad inigualable. A medida que avanza la partida, Cho se vuelve más grande, duele más y es más difícil de matar. Las otras builds o son demasiado frágiles (AP) o no escalan tan bien en daño (Tank Puro).

## 9. PLAN DE JUEGO

**Early Game (Niveles 1-6):**
*   **Lane:** Usar E para farmear y pokear. Mantener distancia. Usar pasiva para recuperar vida/maná. Evitar trades largos sin Grasp cargado.
*   **Jungla:** Empezar con buff que permita clear seguro (Blue para maná/sustain o Red para daño). Usar E para clear rápido. Smite para asegurar objetivos.
*   **Objetivo:** Conseguir 1-2 stacks de Feast en minions/monstruos si no hay kills seguras. Comprar componentes de Heartsteel.

**Mid Game (Niveles 7-12):**
*   **Item Power Spike:** Al completar Heartsteel, Cho empieza a destacar. Buscar peleas pequeñas y usar Q-R para eliminar objetivos clave.
*   **Macro:** Pushear líneas con E y Demolish. Aprovechar Crystalline Overgrowth en torres.
*   **Objetivos:** Controlar Dragones/Herald con Smite y daño verdadero de R.

**Late Game (Niveles 13+):**
*   **Teamfights:** Iniciar con Q sobre múltiples enemigos o usar Flash-Q. Activar R para ejecutar al tanque/enemigo con más vida. Usar E para ralentizar y dañar en área.
*   **Posicionamiento:** Frontline. Absorber daño mientras se aplica daño porcentual.
*   **Splitpush:** Si el equipo necesita presión, Cho puede tirar torres rápidamente con Demolish + Crystalline Overgrowth + Heartsteel.

## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS

*   **Fuentes Primarias:** Notas oficiales Wild Rift 7.3 (21/09/2026). wr-meta.com (24/09/2026).
*   **Supuestos del Modelo:**
    *   Se asumen 6 stacks de Feast a nivel 15 (conservador, podría ser más).
    *   Se asume que Heartsteel está completamente cargado.
    *   El daño de E se calcula contra un objetivo de 4000 HP para demostrar la escalada.
    *   No se incluye daño de objetos activos (como Rocketbelt) para simplificar.
*   **Discrepancias:** Ninguna significativa detectada entre fuentes para Cho'Gath en 7.3.
*   **Contexto Meta:** Cho'Gath tiene un win rate sólido (~51%) en Top y Jungla. Su presencia es media-alta debido a su utilidad de CC y escalado.

## APÉNDICE A — POOL DE ÍTEMES DEL ROL: veredicto por ítem

| Ítem | Veredicto | Razón |
| :--- | :--- | :--- |
| **Heartsteel** | ✅ CORE | Escalado infinito HP/Daño. |
| **Hollow Radiance** | ✅ CORE | Daño mágico % HP bonus. |
| **Liandry's Torment** | ✅ CORE | Quemadura % vida. |
| **Force of Nature** | ✅ Situacional | Mejor RM escalable. |
| **Warmog's Armor** | ✅ Situacional | Regen masiva. |
| **Spirit Visage** | ✅ Situacional | Amplifica regen/curación. |
| **Thornmail** | ✅ Situacional | Anti-AD/Lifesteal. |
| **Frozen Heart** | ✅ Situacional | Anti-AS. |
| **Iceborn Gauntlet** | ⚠️ Alternativa | Bueno control, menos daño. |
| **Sunfire Aegis** | ❌ Rechazado | Heartsteel es superior. |
| **Rylai's Crystal Scepter** | ⚠️ Alternativa | Slow útil, pero menos daño/defensa. |
| **Demonic Embrace** | ❌ Rechazado | Item removido/no existe en WR 7.3. |
| **Kraken/Runaan/IE** | ❌ Rechazado | Stats muertos (AS/Crit). |
| **Nashor's Tooth** | ❌ Rechazado | AS innecesaria. |

## APÉNDICE B — RUTAS DE COMPRA

*   **Default (Coloso):** Heartsteel → Plated Steelcaps → Hollow Radiance → Liandry's → Force of Nature → Warmog's.
*   **Anti-AD:** Heartsteel → Plated Steelcaps → Thornmail → Frozen Heart → Force of Nature → Warmog's.
*   **Anti-AP:** Heartsteel → Mercury's Treads → Hollow Radiance → Spirit Visage → Force of Nature → Warmog's.
*   **Jungla:** Smite → Heartsteel → Plated Steelcaps/Mercury's → Hollow Radiance → Liandry's → Situacional.

---
*Reporte generado el 26/09/2026 con datos del parche 7.3. Modelo propio: las cifras de daño son estimadas basadas en ratios y % vida. El valor real depende de la composición enemiga.*