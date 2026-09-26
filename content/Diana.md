---
tags:
  - Jungla
  - Mid
---

**Fecha del análisis:** 26 de septiembre de 2026
**Parche analizado:** 7.3 (lanzamiento oficial: 21 de septiembre de 2026)

## 0. RESUMEN EJECUTIVO


 **Órden de compra (Ruta Default - Jungla/Mid):**
 
| # | Ítem | Oro | Momento típico |
|---|------|-----|----------------|
| 1 | **Hextech Alternator / Amplifying Tome** | 1100/500 | Start/Primer recall |
| 2 | **Boots of Mana** | 1200 | ~8:00–9:00 |
| 3 | **Dusk and Dawn** | 3100 | ~11:00–12:00 |
| 4 | **Infinity Orb** | 3100 | ~14:00–15:00 |
| 5 | **Nashor's Tooth** | 2900 | ~17:00–18:00 |
| 6 | **Zhonya's Hourglass** | 3300 | ~20:00+ |

**Total: ~14 700 oro** (sin contar starter item de jungla si aplica).

**Runas:**
*   **Jungla:** Conqueror · Brutal · Legend: Alacrity · Coup de Grace · Bone Plating · Relentless Hunter.
 *   **Mid:** Electrocute · Sudden Impact · Chain Assault · Eyeball Collection · Bone Plating · Transcendence.
**Hechizos:**
- Flash + Ignite (Mid) / Smite + Flash (Jungla).

**Orden de habilidades:**
```
Q > E > W (Max Q primero para clear y poke, E para movilidad/reset, W para escudo/daño en área).
```

**Resultado del modelo:** Diana no se mide solo por DPS sostenido de autos, sino por **DPS por ventana de combo**. La sinergia de *Dusk and Dawn* (Spellblade + on-hit extra) con su pasiva genera picos de daño explosivos. En comparación con builds puras de AP (Luden's), esta ruta híbrida ofrece mayor sustain, mejor clear de jungla y más daño en peleas prolongadas gracias a los efectos on-hit y la velocidad de ataque.

## 1. CONTEXTO DEL CAMPEÓN EN ESTE PARCHE

*   **Nerfs/Buffs directos:** No hubo cambios directos a las habilidades de Diana en 7.3, pero sí ajustes sistémicos cruciales.
*   **Cambios sistémicos:**
    *   **Daño Crítico Base 200%:** Aunque Diana no construye crítico tradicionalmente, ítems como *Infinity Orb* permiten que sus habilidades criten contra objetivos con poca vida, aprovechando este multiplicador.
    *   **Tope de AS 3.0:** La pasiva de Diana otorga hasta un 100% de AS. Con ítems como *Nashor's Tooth* (50%) y runas, puede acercarse al tope, haciendo que cada punto de AS sea valioso para aplicar efectos on-hit y reducir CDs de autoataques.
    *   **Ítems Nuevos/Rehechos:** *Dusk and Dawn* (3100g) es el núcleo perfecto para Diana, combinando AP, AS, Salud y un Spellblade que cura y aplica on-hits adicionales. *Nashor's Tooth* fue buffeado a 80 AP y 50% AS.

## 2. FICHA MATEMÁTICA (SPEC)

*   **AD Base/Crecimiento:** 52 (+3.64 por nivel). A nivel 15: ~106 AD.
*   **AS Base/Ratio/Bonus Base/Por Nivel:** 0.694 / 0.694 / 0.15 / 0.008.
*   **Rango:** Melee (150 unidades aprox.).
*   **Modificadores del Auto:**
    *   **Pasiva (Moonsilver Blade):** Tras usar habilidad, gana 30-100% AS por 4s. Cada 3er ataque inflige 20 + 15/nivel + 50% AP de daño mágico en área.
    *   **Self AS Buff:** Hasta 1.0 (100%) condicional tras habilidad.
*   **Recursos:** Maná (435 base + 41/nivel).
*   **Habilidades clave para el modelo:**
    *   **Q (Crescent Strike):** 60-195 + 70% AP. Aplica Moonlight.
    *   **W (Pale Cascade):** Escudo 50-110 + 40% AP. Daño en área 20-65 + 20% AP por esfera.
    *   **E (Lunar Rush):** 40-160 + 30% AP. Reset de CD si elimina Moonlight.
    *   **R (Moonfall):** 100-220 + 40% AP a 200-440 + 80% AP. Atrae enemigos.

## 3. MODELO Y FÓRMULAS

Para Diana, el modelo de DPS puro de autos es insuficiente. Se utiliza un modelo de **Ventana de Combo**:
1.  **Daño de Habilidades:** Suma de Q + W (3 esferas) + E + R (daño máximo) + Pasiva (1 proc de 3er golpe).
2.  **Daño de Autos en Ventana:** Durante la duración de la pasiva (4s) y el buff de AS, Diana realiza múltiples autos.
    *   `AS_Efectiva = min(AS_Base + Ratio * (Bonus_Items + Runas + Buff_Pasiva), 3.0)`
    *   `Daño_Auto = AD_Total + Daño_OnHit (Dusk/Nashor) + Daño_Pasiva (Cada 3er golpe)`
3.  **Sinergia Dusk and Dawn:**
    *   Spellblade: `75% AD Base + 10% AP` dañado mágico.
    *   On-Hit Extra: Aplica un efecto on-hit adicional tras el Spellblade.

**Supuestos:** Combo ideal donde se activan todos los daños. Uptime de pasiva alto en peleas.

## 4. LEYES APLICADAS A DIANA

*   **Ley 1 (Crítico):** No aplica directamente a su build principal, pero *Infinity Orb* es esencial para ejecutar objetivos bajos de vida con habilidades, aprovechando el nuevo daño crítico base de 200%.
*   **Ley 2 (Velocidad de Ataque):** Diana escala excepcionalmente bien con AS debido a su pasiva. El tope de 3.0 permite que, con *Nashor's Tooth* y *Dusk and Dawn*, alcance velocidades de ataque muy altas durante sus ventanas de daño, maximizando la aplicación de efectos on-hit y la frecuencia de la pasiva.
*   **Ley 3 (Penetración):** Contra tanques, *Void Staff* o *Cryptbloom* son necesarios. Sin embargo, el daño mixto (físico de autos, mágico de habilidades y on-hit) dificulta la mitigación enemiga.
*   **Ley 4 (Stats Muertos):** Ítems como *Rabadon's Deathcap* son menos eficientes temprano que *Dusk and Dawn* porque Diana necesita AS y Salud para sobrevivir y mantenerse en la pelea. *Luden's Echo* tiene daño en área útil, pero carece de la sinergia on-hit que explota la pasiva de Diana.

## 5. ANÁLISIS DEL PRIMER ÍTEM

| Candidato | Oro | Pros | Contras | Veredicto |
|-----------|-----|------|---------|-----------|
| **Hextech Alternator** | 1100 | Bueno para poke (Q) y clear. Componente de muchos ítems. | No ofrece AS ni sustain. | ✅ Inicio estándar. |
| **Amplifying Tome** | 500 | Barato, flexible. | Stats mínimos. | ✅ Si necesitas ahorrar para *Boots of Mana*. |
| **Lost Chapter** | 1200 | Maná y Haste. Útil si sufres de maná. | Menor daño inmediato que Alternator. | ⚠️ Solo si tienes problemas de maná. |

**Veredicto:** Iniciar con *Hextech Alternator* o *Amplifying Tome* + *Boots of Mana* es lo óptimo. *Boots of Mana* proporciona AP, penetración mágica y regeneración de maná, crucial para mantener la presión en lane o el clear en jungla.

## 6. BUILD FINAL RANURA POR RANURA

| Slot | Ítem | Justificación Matemática |
|------|------|--------------------------|
| Botas | **Boots of Mana** | AP, Penetración Mágica, Regeneración de Maná. Mejora el daño temprano y la sostenibilidad. |
| 1 | **Dusk and Dawn** | Núcleo absoluto. Combina AP, AS, Salud y Haste. El Spellblade y el on-hit extra sinergizan perfectamente con la pasiva de Diana. Cura al atacar. |
| 2 | **Infinity Orb** | Permite que las habilidades criten a enemigos con <40% HP. Con el daño crítico base de 200%, esto aumenta drásticamente el poder de ejecución de Diana. |
| 3 | **Nashor's Tooth** | 80 AP y 50% AS. El daño on-hit (15 + 20% AP bonus) se aplica frecuentemente gracias a la alta AS de la pasiva y Dusk and Dawn. |
| 4 | **Zhonya's Hourglass** | Supervivencia esencial. Diana debe entrar en medio del equipo enemigo. La estasis permite esperar cooldowns y sobrevivir burst. |
| 5 | **Void Staff** / **Cryptbloom** | Penetración mágica porcentual necesaria contra tanques. *Cryptbloom* ofrece curación al equipo si matas a alguien. |

**Matriz del último slot:**
*   vs Tanques: **Void Staff**
*   vs Burst AD: **Zhonya's** (si no está ya comprado) o **Sterak's Gage** (híbrido).
*   vs Curación: **Morellonomicon** (si el equipo no tiene otra fuente).
*   Daño Máximo: **Rabadon's Deathcap**.

**RECHAZADOS:**
*   **Luden's Echo:** Buen daño en área, pero *Dusk and Dawn* ofrece más utilidad y sinergia con el kit de Diana.
*   **Riftmaker:** El daño gradual es bueno, pero Diana busca burst y resets. *Infinity Orb* es mejor para ejecutar.
*   **Gunmetal Greaves:** Aunque dan AS, la penetración y AP de *Boots of Mana* son más valiosas para un mago/luchador AP.

## 7. RUNAS · HECHIZOS · HABILIDADES

**Keystone:**
*   **Conqueror (Jungla):** Proporciona AD/AP adaptativo y omnivamp al apilarse. Ideal para peleas prolongadas y sustain en jungla.
*   **Electrocute (Mid):** Burst adicional para asegurar kills en laning phase con el combo Q-E-W.

**Secundarias:**
*   **Precision:** Legend: Alacrity (AS extra), Coup de Grace (más daño a enemigos bajos de vida, sinergia con Infinity Orb).
*   **Domination:** Sudden Impact (penetración tras dash de E), Chain Assault (daño extra tras marcar con habilidad).
*   **Resolve:** Bone Plating (supervivencia en lane/jungla temprana).
*   **Sorcery:** Transcendence (Haste adicional), Celerity (movilidad).

**Hechizos:**
*   **Jungla:** Smite + Flash.
*   **Mid:** Flash + Ignite (para kill pressure) o Barrier (vs asesinos).

**Orden de Habilidades:**
1.  **Q (Crescent Strike):** Principal fuente de daño y clear.
2.  **E (Lunar Rush):** Movilidad y reset. Esencial para combos.
3.  **W (Pale Cascade):** Escudo y daño en área. Útil para tradeos y clear.
4.  **R (Moonfall):** Maxear cuando esté disponible.

## 8. COMPARACIÓN CONTRA LAS ALTERNATIVAS

| Build | Oro | AP | AS | Daño Combo (Estimado) | Sustain | Utilidad |
|-------|-----|----|----|-----------------------|---------|----------|
| **Optima Híbrida (Dusk/IO/Nashor)** | ~14700 | Alto | Muy Alto | Muy Alto (Burst + On-hit) | Alto (Dusk cure + Conqueror) | Media (Zhonya) |
| **Full AP Burst (Luden/Orb/Rabadon)** | ~14000 | Muy Alto | Bajo | Alto (Solo habilidades) | Bajo | Baja |
| **On-Hit Puro (Nashor/Wits End/Guinsoo)** | ~13500 | Medio | Máximo | Medio (Sostenido) | Medio | Bajo |

La build híbrida supera a la Full AP en peleas prolongadas y contra múltiples objetivos debido a la sinergia de la pasiva con los efectos on-hit y la AS. Supera a la On-Hit pura en burst y escalado de habilidades.

## 9. PLAN DE JUEGO

*   **Early (Jungla):** Comenzar con Smite. Clear eficiente usando Q para aplicar Moonlight y E para resetear. Usar W para mitigar daño de monstruos. Priorizar ganks en lanes con CC, ya que Diana necesita landing de Q o R para maximizar daño.
*   **Early (Mid):** Poke con Q. Si el enemigo queda marcado, usa E para dash y tradear con W y autos. Busca kills con Electrocute.
*   **Mid Game:** Completar *Dusk and Dawn*. Participar en objetivos. Diana es excelente en skirmishes gracias a su movilidad y daño en área. Usar R para iniciar o seguir up si el equipo tiene CC.
*   **Late Game:** Posicionamiento clave. Entrar con R para atraer múltiples enemigos, usar Zhonya si es foco, y luego limpiar con resets de E. *Infinity Orb* permite ejecutar carries enemigos bajos de vida con habilidades.

## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS

*   **Fuentes:** Notas oficiales 7.3, wr-meta.com (24/09/2026).
*   **Discrepancias:** Ninguna significativa detectada para Diana en 7.3.
*   **Supuestos:** Modelo de combo asume landing perfecto de Q y R. Daño de pasiva calculado con AP completo.
*   **Contexto Meta:** Diana es considerada fuerte en jungla y viable en mid. Su capacidad de carry depende de obtener ventajas tempranas y explotarlas con su mobility.

## APÉNDICE A — POOL DE ÍTEMES DEL ROL: veredicto por ítem

*   **Dusk and Dawn:** ✅ Core. Sinergia perfecta.
*   **Nashor's Tooth:** ✅ Core. AS y on-hit.
*   **Infinity Orb:** ✅ Esencial para execute.
*   **Zhonya's Hourglass:** ✅ Supervivencia obligatoria.
*   **Void Staff:** ✅ vs Tanques.
*   **Luden's Echo:** ⚠️ Alternativa si prefieres poke/clear rápido, pero pierde sinergia on-hit.
*   **Riftmaker:** ⚠️ Bueno para peleas largas, pero menos burst.
*   **Rabadon's Deathcap:** ✅ Late game damage.
*   **Morellonomicon:** ⚠️ Solo si hay mucha curación enemiga.
*   **Guinsoo's Rageblade:** ❌ Menos eficiente que Nashor para Diana debido a la falta de AP significativo y sinergia de Spellblade.

## APÉNDICE B — RUTAS DE COMPRA

*   **Default:** Alternator -> Boots of Mana -> Dusk and Dawn -> Infinity Orb -> Nashor's Tooth -> Zhonya's.
*   **Vs Tanques:** ... -> Void Staff antes de Nashor's.
*   **Vs Burst AD:** ... -> Zhonya's como 3er ítem.
*   **Snowball:** ... -> Rabadon's Deathcap después de Infinity Orb.