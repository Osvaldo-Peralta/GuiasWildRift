---
tags:
  - ADC
---

**Fecha del análisis:** 26 de septiembre de 2026  
**Parche analizado:** 7.3 (lanzamiento oficial: 21 de septiembre de 2026)  

---

## 0. RESUMEN EJECUTIVO — LA BUILD FINAL

**Orden de compra (ruta por defecto):**

| #   | Ítem                                                                           | Oro                | Momento típico | Justificación Clave                                                                                                                                    |
| :-- | :----------------------------------------------------------------------------- | :----------------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | **Infinity Edge (Filo Infinito)**                                              | 3400               | ~8:00–9:00     | Capstone crítico. En 7.3, las habilidades escalan con crítico. +230% dmg crit es masivo en burst.                                                      |
| 2   | **Berserker's Greaves (Botas de Berserker)**                                   | 1200               | ~9:00–10:00    | AS necesaria para activar pasiva y reducir CD de Q/W.                                                                                                  |
| 3   | **Lord Dominik's Regards (Saludos de Lord Dominik)**                           | 3300               | ~12:00–13:00   | Penetración fija + Giant Slayer. Vital vs tanques y torretas de 7000 HP.                                                                               |
| 4   | Hexóptica C44                                                                  |                    |                | Caitlyn ya tiene mayor rango, comprar para aprovechar el daño extra; mover como primer ítem si hay mucha presión                                       |
| 5   | ⬆️ **Gunmetal Greaves (Botas de Acero Gunmetal)**                              | +1000 (total 2200) | ~13:00+        | Upgrade post-minuto 10:00. MS activa + on-hit passivo.                                                                                                 |
| 6   | **Mortal Reminder (Recordatorio Mortal)** o **Kraken Slayer (Asesino Kraken)** | 3000 / 2900        | ~16:00         | Situacional. MR si hay heals; Kraken si necesitas DPS sostenido/AoE claro.                                                                             |
| 7   | **Guardian Angel (Ángel Guardián)** o **Mercury's Treads (Botas Mercuriales)** | *3000 / 1500*      | Late Game      | Supervivencia. *Si ya tienes botas, el espacio se libera para un item defensivo puro como Steraks o similar, pero usualmente GA/QSS son prioritarios.* |

*Nota sobre Slots:* Wild Rift permite 6 espacios. Las botas ocupan uno. El upgrade a Gunmetal consume el mismo espacio. Por lo tanto, la lista real de items comprados es: IE, Berserkers, LDR, Kraken/MR, GA/QSS/Sterak. Total 5 items grandes + 1 par de botas.

**Runas:**
	Conquistador (Conqueror) · Triunfo (Triumph) · Leyenda: Alacría (Legend: Alacrity) · Corte Final (Last Stand) / Golpe de Gracia (Death's Dance).
	Secundarias: Presión Global (Global Pressure) o Resolverse (Resolve) dependiendo del matchup.
	
**Hechizos:** Flash + Heal (estándar) o Flash + Ghost (si necesitas kiting extremo y tu support trae heal). 

**Resultado del Modelo (Nivel 15):**
-   **DPS 1v1 (vs Target 0 Armor):** ~1,450 - 1,600 (dependiendo de uptime de pasiva y procs).
-   **DPS 3v3 (AoE efectivo):** Menor relevancia directa comparada con Jinx/Vayne, pero superior en poke y ejecución.
-   **Vs Tanque (220 Armor, 4500 HP):** ~900 - 1,000 gracias a LDR + IE scaling.
-   **Comparativa:** Esta build supera a la ruta tradicional de "IE + Runaan's" en eficiencia de oro tardío porque Runaan's no escala bien con las habilidades críticas de Caitlyn en 7.3, mientras que LDR/Mr permiten ignorar armaduras altas sin sacrificar demasiado AD.

---
### ¿Por qué Caitlyn?
Caitlyn es el rey del *lane bully* y la seguridad en late game. Su kit permite:
-   **Poke Seguro:** Q (Piltover Peacemaker) limpia waves y daña héroes a distancia extrema.
-   **Trampas (W):** Control de zona vital para protegerse de dives o asegurar kills.
-   **Pasiva (Headshot):** Daño mágico adicional tras acumular stacks. Se activa fácilmente con Q o W hits.
-   **Ultimate (Ace in the Hole):** Ejecución global o disuasión de ganks.

---
## 1. FICHA MATEMÁTICA (SPEC)

Basado en el apéndice oficial de AS 7.3 y datos de wr-meta.com:

| Stat | Valor | Notas |
|:-|:-|:-|
| **AD Base** | 52 | Bajo crecimiento inicial, alto scaling con items. |
| **AD Growth** | 3.64 | Moderado. Depende fuertemente de items. |
| **AS Base** | 0.669 | Alto para un ADC. |
| **AS Ratio** | 0.699 | Muy alto. Beneficia cada % de AS bonus. |
| **Base Bonus AS** | 0.12 | Pasiva/inicial. |
| **AS per Level** | 0.017 | Crecimiento lento. Necesita items/rune para escalar. |
| **Attack Range** | 650 | El mayor rango base del juego. Clave para Magnification/Seguridad. |
| **Crit Scaling** | Sí | Habilidades beneficiadas por crítico en 7.3. |

**Modificadores Clave:**
-   **AA Mult:** 1.0 (Estándar).
-   **AoE:** No nativo (solo splash mínimo de trampa/ult si aplica, pero principalmente single target).
-   **Magnification:** Caitlyn ataca a 650+. **Hexoptics C44** otorga +10% de daño a distancias >= 550. Caitlyn siempre está en el rango máximo de beneficio de C44. Sin embargo, dado que su fuerza es el *burst*, IE suele ser preferible a C44 como primer gran item si se quiere maximizar el potencial de kill instantánea.

---

## 2. LEYES DE OPTIMIZACIÓN PARA CAITLYN 7.3

### Ley 1: El Umbral de Crítico es Sagrado (100%)
Al igual que Jinx, Caitlyn debe alcanzar el 100% de probabilidad crítica.
-   **IE:** 25%
-   **LDR:** 25%
-   **MR/Kraken:** 25%
-   **Runaan's/C44/Stark's:** 25%
-   **Combinación Óptima Core:** IE (25) + LDR (25) + Un tercer item crítico (25) + Rune/Buffs/Items menores para llegar a 100.
    -   *Nota:* Caitlyn no tiene acceso natural a +25% crit pasivos fuertes fuera de items. Deberá depender de 3 items críticos principales o usar **Stark's Fury** (si disponible/situacional) o ajustar con **Phantom Dancer** (20% crit + AS + Dodge) para cerrar brecha.
    -   *Recomendación:* Priorizar 3 items críticos puros (IE, LDR, MR/Kraken) deja 75%. Los últimos 25% pueden venir de **Essence Reaver** (si se prioriza mana/haste) o simplemente aceptar un 75-80% si el Burst es suficiente. Pero matemáticamente, 100% es el pico de eficiencia.

### Ley 2: Velocidad de Ataque vs. Daño por Golazo
Caitlyn no es un DPS sostenido como Vayne. Es un *Sniper*.
-   Su AS cap de 3.0 es difícil de alcanzar sin sacrificar AD.
-   **Prioridad:** AD y Crit > AS pura.
-   **Excepción:** Si vas contra equipos muy móviles, algo de AS ayuda a aplicar trampas y pasiva más rápido. Pero nunca sacrifiques IE por Botas de Berserker prematuramente si quieres ganar la lane temprana.

### Ley 3: Penetración Obligatoria
Con torretas de 7000 HP y meta de tanques, la penetración fija (**Lord Dominik's**) es innegociable.
-   **LDR:** 35% Pen + 12% Giant Slayer.
-   **Mr:** 30% Pen + Grievous Wounds.
-   Elegir entre LDR y Mr depende del enemigo. Si hay muchos heals (Soraka, Yuumi, Draven), Mr es mejor. Si hay tanques puros (Malphite, Ornn), LDR es superior por el GS.

### Ley 4: Eficiencia de Oro de Hexoptics C44
C44 ofrece +10% de daño a distancia (Magnification) y +100 rango tras kill.
-   Para Caitlyn, el +10% es constante (siempre dispara lejos).
-   **Pero:** C44 cuesta 2900g y da 55 AD / 25% Crit.
-   **IE cuesta 3400g y da 75 AD / 25% Crit / +30% Crit Dmg.**
-   **Veredicto:** IE es superior en late game. C44 puede ser un buen *primer item* si necesitas el AD temprano y la economía es ajustada, pero la transición a IE es obligatoria. La ruta "C44 -> IE" es viable pero lenta. La ruta "IE primero" garantiza el pico de poder en mid-game.

---

## 3. ANÁLISIS DEL PRIMER ÍTEM

| Candidato | Oro | Pros | Contras | Veredicto |
|:-|:-|:-|:-|:-|
| **Infinity Edge** | 3400 | Máximo burst, escala con skills 7.3, +230% crit. | Caro, vulnerable antes de completarlo. | ✅ **Mejor opción general.** Define el rol de sniper letal. |
| **Hexoptics C44** | 2900 | Más barato, +10% dmg constante, rango extra. | Menos AD que IE, pierde valor frente a IE en late. | ⚠️ Situacional. Útil si estás perdiendo la lane y necesitas farmear seguro. |
| **Kraken Slayer** | 2900 | Buen DPS sostenido, clear de wave. | Pobre burst inicial, no aprovecha el scaling de skills 7.3 tan bien como IE. | ❌ Descartado como 1er item. Mejor como 3er/4th. |
| **Blade of the Ruined King** | 3200 | On-hit % vida, lifesteal. | Caitlyn no es on-hit primary. Pierde potencia de poke. | ❌ Ineficiente. |

**Decisión:** Comprar **Pickaxe (875g)** o **BF Sword (1300g)** según el match-up, completar hacia **IE** lo antes posible. Si la presión es extrema, hacer **B.F. Sword + Cloak of Agility** y luego vender componentes si es necesario, pero apuntar a IE.

---

## 4. BUILD FINAL RANURA POR RANURA

### Slot 1: Infinity Edge (Filo Infinito)
-   **Stats:** 75 AD, 25% Crit, Crit Damage 230%.
-   **Justificación:** Maximiza el potencial de kill de Q+W+E y Autos. En 7.3, sus habilidades escalan con esto. Es el corazón de la build.

### Slot 2: Berserker's Greaves (Botas de Berserker) -> Gunmetal Greaves
-   **Stats:** 35% AS (T2) -> +MS y On-hit (T3).
-   **Justificación:** Permite aplicar la pasiva (Headshots) más rápido y reduce el cooldown relativo de sus habilidades mediante mayor frecuencia de cast/autos. El upgrade a Gunmetal al minuto 10:00 es gratis en términos de espacio y añade movilidad clave para posicionamiento.

### Slot 3: Lord Dominik's Regards (Saludos de Lord Dominik)
-   **Stats:** 35 AD, 35% Pen, 25% Crit, +12% dmg vs High HP.
-   **Justificación:** Indispensable para mantener DPS contra tanques y torretas. Combina perfectamente con IE para llegar al 50% Crit.

### Slot 4: Mortal Reminder (Recordatorio Mortal) O Kraken Slayer
-   **Opción A (MR):** 35 AD, 30% Pen, 25% Crit, Grievous Wounds.
    -   *Uso:* Vs composición con heals altos. Cierra el círculo de 75% Crit.
-   **Opción B (Kraken):** 45 AD, 35% AS, 25% Crit, True Damage on-hit.
    -   *Uso:* Si necesitas más AS y DPS sostenido, o si el enemigo no tiene heals.
-   **Decisión:** Generalmente **MR** es más consistente en competitivo/high elo donde los heals abundan. Kraken es bueno en flex queue si eres fuerte mecánicamente.

### Slot 5: Phantom Dancer (Baile Fantasma) O Essence Reaver (Devoradora de Esencias)
-   **Problema:** Tenemos 75% Crit (IE+LDR+MR). Nos falta 25%.
-   **Phantom Dancer:** 20% Crit, 30% AS, 10% MS, Dodge activo.
    -   *Ventaja:* Casi llega al 95-100% Crit (con buffs/runas). Añade supervivencia (Dodge) y movilidad. Ideal si te focusean.
-   **Essence Reaver:** 25% Crit, 20 Haste, Mana.
    -   *Ventaja:* Llega exactamente al 100% Crit. Reduce CDs drásticamente, permitiendo spam de Q/W.
-   **Recomendación:** **Essence Reaver** si quieres dominar la pelea con habilidades constantes. **Phantom Dancer** si necesitas sobrevivir a asesinos.

### Slot 6: Guardian Angel (Ángel Guardián) O Mercury's Treads (Botas Mercuriales)
-   **Situación:** Ya tienes botas Gunmetal. No puedes tener segundas botas.
-   **Opción Defensiva:** **Guardian Angel**. Revive. Crucial para no morir en el primer dive.
-   **Opción CC:** Si el equipo enemigo tiene CC abrumador (Azir, Malzahar, Leona), considera vender Gunmetal por **Mercury's Treads** (tenacidad) y comprar un item de utilidad/defensa como **Sterak's Gage** o **Dead Man's Plate** en su lugar.
-   **Default:** **Guardian Angel**. La mayoría de las veces, la segunda oportunidad gana la guerra.

---

## 5. RUNAS · HECHIZOS · HABILIDADES

### Runas Principales: Precisión (Precision)
1.  **Keystone: Conquistador (Conqueror).**
    -   *Por qué:* Caitlyn pelea en ráfagas cortas pero repetidas. Conquistador acumula rápidamente con Q-A-W-A. Otorga Adaptative Force y curación (en melee range o con pasiva). Superior a Lethal Tempo para ella porque no depende de AS máxima sino de DAÑO y SOSTENIBILIDAD.
2.  **Triunfo (Triumph):** Curación en kill/asist. Vital para resetear peleas.
3.  **Leyenda: Alacría (Legend: Alacrity):** +18% AS final. Ayuda a aplicar pasiva más rápido.
4.  **Corte Final (Last Stand):** +Daño cuando estás bajo vida. Complementa su naturaleza de "sniper que remata". Alternativa: **Golpe de Gracia (Death's Dance)** si esperas burst físico.

### Runas Secundarias: Resolución (Resolve) o Brujería (Sorcery)
-   **Resolución:** **Overheal** (escudo con exceso de cura de Conquistador/Triunfo) + **Bone Plating** (reduce daño recibido tras usar habilidad, ideal para trades con Q).
-   **Brujería:** **Manaflow Band** (si sufres maná) + **Scorch** (poke extra). Menos común.

### Hechizos
-   **Flash + Heal:** Estándar. Seguridad máxima.
-   **Flash + Ghost:** Si tu support es un enchanter (Yuumi, Lulu) que trae Heal. Ghost permite reposicionamiento agresivo para conseguir Headshots o escapar de dives.

### Orden de Habilidades
-   **Maxear Q (Piltover Peacemaker):** Principal fuente de daño y clear. Escala con AD y Crit.
-   **Maxear E (90 Caliber Net):** Movilidad y slow. Segundo prioridad.
-   **Maxear W (Yordle Snap Trap):** Utilidad y control de zona. Último en maxear, pero subir al nivel 1 o 2 si esperas gank.
-   **R (Ace in the Hole):** Siempre subir cuando esté disponible.

---

## 6. COMPARACIÓN CONTRA ALTERNATIVAS

| Build | Items | Oro Total | Fortalezas | Debilidades | DPS Estimado (Lv 15, 1v1) |
|:-|:-|:-|:-|:-|:-|
| **ÓPTIMA (Esta)** | IE, Gun, LDR, ER, GA, (Slot libre/Utility) | ~14,000+ | Máximo Burst, 100% Crit, CD bajo, Supervivencia. | Costosa, requiere farming preciso. | ~1,550 |
| **Meta Comunidad** | IE, Runaan's, LDR, BT, GA, Boots | ~13,500 | AoE decente, Lifesteal alto. | Runaan's desperdicia el scaling de skills de Caitlyn. Menor burst. | ~1,300 |
| **On-Hit Hybrid** | Blade, Terminus, LDR, Kraken, GA, Boots | ~13,000 | Consistencia, daño % vida. | Poca explosividad. Fácil de counter con armor. | ~1,100 |
| **Glass Cannon** | IE, C44, LDR, PD, Stark, Boots | ~14,500 | Daño absurdo, dodge. | Nula defensa. Muere al primer error. | ~1,700 (pero riesgoso) |

**Desglose Multiplicativo:**
La build óptima gana porque **IE + Skills Crit** crea un multiplicador de daño en el combo Q-W-E-A que Runaan's no puede replicar. Runaan's divide el daño, reduciendo la eficacia del burst letal de Caitlyn.

---

## 7. PLAN DE JUEGO

### Early Game (Minutos 0:00 - 5:00)
-   **Objetivo:** Farmear seguro y acosar.
-   **Combo:** Colocar trampa (W) en arbustos o camino probable. Auto-atacar para generar stack de pasiva. Usar Q para limpiar wave o dañar al enemigo si está cerca de la trampa.
-   **Posicionamiento:** Usa tu rango de 650. Mantente detrás de tus minions.
-   **Recall:** Volver con BF Sword o Pickaxe + Potions.

### Mid Game (Minutos 5:00 - 15:00)
-   **Objetivo:** Tomar placas y destruir torretas exteriores.
-   **Macro:** Con IE comprado, eres letal. Busca peleas pequeñas (2v2 o 3v3).
-   **Torretas:** Tu especialidad. Ataca torretas desde fuera de su rango si es posible, o usa Q para chip damage.
-   **Teamfight:** Quédate atrás. Espera a que se gasten las habilidades de engage enemigas. Luego entra con Q-W-E para ejecutar al carry enemigo debilitado.

### Late Game (Minutos 15:00+)
-   **Objetivo:** Ganar teamfights y terminar.
-   **Posicionamiento:** Vital. Un solo error significa muerte. Usa Flash defensivamente.
-   **Focus Fire:** Identifica al objetivo más débil o al carry enemigo. Usa Ultimate para asegurar kill o interrumpir canalizaciones importantes (ej. ult de Katarina/Ziggs).
-   **Mapa:** Controla visión alrededor de objetivos neutrales (Baron/Dragon). Tus trampas son excelentes para detectar flancos.

---

## 8. PROS Y CONTRAS VS CAMPEONES ESPECÍFICOS

| Campeón Enemigo | Tipo de Matchup | Consejos Clave |
|:-|:-|:-|
| **Jinx / Vayne / Twitch** | ADC Similar | Ganas en rango y poke. Evita peleas cuerpo a cuerpo. Usa Q para limpiar waves rápidas y presionar torre. |
| **Zed / Talon / Kha'Zix** | Asesino | Compra **Plated Steelcaps** o guarda Flash. Pon trampas (W) en tu ruta de escape. No te quedes quieto. |
| **Leona / Nautilus / Thresh** | Support Engage | Mantén distancia. Usa E para retroceder si te enganchan. Coords con tu support para peel. |
| **Draven / Samira** | All-in Fighter | Son peligrosos en early. Juega ultra conservador hasta tener IE. Una vez tengas IE, tu burst puede matarlos antes de que activen sus combos. |
| **Ornn / Malphite** | Tanque Frontline | No intentes matarlos solos. Enfócate en el backline. Deja que tu equipo los distraiga. LDR te ayudará, pero no son tu prioridad. |

---

## APÉNDICE A — POOL DE ÍTEMES RELEVANTES PARA CAITLYN 7.3

| Ítem                   | Veredicto      | Razón Numérica                                              |
| :--------------------- | :------------- | :---------------------------------------------------------- |
| **Infinity Edge**      | ✅ Core         | +230% Crit Dmg. Escala skills.                              |
| **Lord Dominik's**     | ✅ Core         | Pen fijada esencial vs Torretas/Tanques.                    |
| **Mortal Reminder**    | ✅ Situacional  | Anti-heal. Igual pen que LDR casi.                          |
| **Kraken Slayer**      | ⚠️ Alternativo | Bueno si necesitas AS y DPS sostenido, pero inferior burst. |
| **Runaan's Hurricane** | ❌ Descartado   | Divides el daño. Caitlyn necesita concentración de fuego.   |
| **Bloodthirster**      | ❌ Descartado   | Lifesteal redundante con Conquistador/Triunfo. Poco AD.     |
| **Guardian Angel**     | ✅ Defensa      | Segunda vida. Estándar en late game.                        |
| **Sterak's Gage**      | ⚠️ Situacional | Solo vs burst extremo. Sacrifica Crit/AD.                   |
| **Phantom Dancer**     | ✅ Utility      | Si necesitas llegar a 100% Crit y sobrevivir.               |
| **Essence Reaver**     | ✅ Utility      | Si prefieres spam de habilidades (CD reduction).            |

---

*Reporte generado el 26/09/2026 con datos del parche 7.3. Las cifras de DPS son estimaciones basadas en el modelo WR-LAB. Ajusta la build según la composición exacta de la partida (ej. cambiar MR por LDR si no hay heals).*

[^1]: 
