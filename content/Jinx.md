---
tags:
  - ADC
---
Fecha del análisis: 25 de septiembre de 2026  
Parche analizado: 7.3 (lanzamiento oficial: 21 de septiembre de 2026)

Metodología: notas oficiales del parche 7.3 y 7.2 ([wildrift.leagueoflegends.com](http://wildrift.leagueoflegends.com)), base de datos de ítems/runas actualizada al 24-sep-2026 ([wr-meta.com](http://wr-meta.com)), y un modelo propio de DPS/economía de oro construido específicamente para el kit de Jinx. Nada está copiado de una página de builds: cada decisión está derivada de los números de la sección 3–6.

---
## 0. RESUMEN EJECUTIVO — LA BUILD FINAL

> Órden de compra (ruta por defecto):

|   |   |   |   |
|---|---|---|---|
|#|Ítem|Oro|Momento típico|
|1|Hexoptics C44|2900|~7:00–8:00|
|2|Berserker’s Greaves|1200|~9:00–10:00|
|3|Runaan’s Hurricane|2650|~11:30–12:30|
|4|⬆️ Gunmetal Greaves (mejora de botas, disponible desde el minuto 10:00)|+1000 (2200 total)|~13:00|
|5|Infinity Edge|3400|~15:30–16:30|
|6|Lord Dominik’s Regards (→ Mortal Reminder si el enemigo sana mucho)|3300|~18:00–19:00|
|7|Kraken Slayer|2900|~21:00|

> Total: 17 350 oro (botas incluidas — recuerda que en Wild Rift las botas ocupan uno de los 6 espacios).

> Runas: Lethal Tempo · Legend: Alacrity · Brutal · Coup de Grace · Bone Plating (alternativas en §7).  
> Hechizos: Flash + Ghost. Orden de habilidades: Q → W → E (R en 5/9/13).

> Variante con sustento (recomendada si te hacen poke o necesitas sobrevivir peleas largas): cambia el ítem 7 (Kraken Slayer) por Bloodthirster. Pierdes ~7 % de DPS y ganas ~600 HP/s de robo de vida + escudo.

> Resultado del modelo a nivel 15 (pre-mitigación): 3042 DPS a un objetivo, ~10 550 DPS en pelea de 3 objetivos, +47 % de daño vs carries con armadura y +73 % vs tanques en comparación con tu build actual adaptada a 7.3 (detalle en §8).

---

## 1. POR QUÉ TU BUILD QUEDÓ OBSOLETA (no es culpa tuya: el juego cambió debajo de ti)

Tres hallazgos duros, verificados contra las notas oficiales:

1. Tu build de 7 espacios ya no es construible. En el parche 7.2 Riot eliminó los encantamientos de botas y convirtió Quicksilver Sash (1100g) y Mercurial Scimitar (3100g) en ítems normales ligados a clase (marksman/fighter). Es decir: ya no existe “Quicksilver como hechizo de botas → evolucionar a Mercurial Scimitar”. La Scimitar ahora ocupa un espacio completo de ítem, y las botas tienen su propio camino de mejora (Tier 3, §2.5). La build que describiste (Berserker’s + Kraken + QSS + RFC + Runaan’s + IE + BT + Scimitar) son 7 espacios reales: imposible en 7.3. Si la estabas ejecutando tal cual, probablemente estabas perdiendo un espacio completo de daño.
2. El sistema de crítico cambió radicalmente en 7.3: daño crítico base 175 % → 200 %, e Infinity Edge ahora da 230 %. Cada 1 % de probabilidad crítica vale ahora ~14 % más que antes, y llegar a 100 % de crítico exacto es el nuevo umbral de eficiencia. Tu build se quedaba en 75 % y desperdiciaba velocidad de ataque por encima del nuevo tope.
3. No llevabas penetración de armadura. Con torretas de 7000 HP, campeones con más vida y el meta de tanques, 0 % de pen significaba que a partir del minuto 12 tu daño real caía ~55 % contra cualquier frontline. Lord Dominik’s (35 % pen + 25 % crítico + Giant Slayer) es, matemáticamente, el ítem más eficiente del parche para un Jinx de crítico (§4, Ley 3).

Y un dato adicional: Jinx recibió nerfs directos en 7.3 (AD por nivel 4.5 → 4; R: enfriamiento 50/45/40 → 60/50/40 y ratio 15 %–150 % → 12 %–120 % de AD bonus). Su daño ahora depende MÁS de los ítems y menos del campeón: la optimización de build importa más que nunca.

---

## 2. TODO LO QUE CAMBIÓ EN 7.3 Y AFECTA A JINX

### 2.1 Sistema de crítico

- Daño crítico base: 175 % → 200 %.
- Infinity Edge: +75 AD, 25 % crítico, golpes críticos al 230 % (su pasivo “Limit Break” fue eliminado; ya no necesitas 100 % de crítico para activarlo).
- Varios campeones (Caitlyn, MF, Tristana, Xayah, Lucian, Ashhe, Akshan…) ahora escalan habilidades con crítico; Jinx NO recibió esos cambios porque sus cohetes ya critican de forma nativa — ella es la ganadora “silenciosa” del aumento a 200 % base: cada cohete de Fishbones es un golpe de área que puede critar al 200–230 % a TODOS los objetivos en la explosión.

### 2.2 Velocidad de ataque: sistema nuevo

- Tope: 2.5 → 3.0 ataques/segundo.
- Fórmula oficial nueva: AS total = AS base + Ratio × AS bonus, donde AS bonus = base bonus + nivel + ítems + runas.
- Números nuevos de Jinx (apéndice oficial 7.3): AS base 0.625 · ratio 0.625 · bonus base 0.30 · 0.02 por nivel (→ +0.28 a nivel 15).
- El bonus por nivel no es lineal: al subir al nivel L ganas 0.02 × (0.7 + 0.04 × (L−1)).
- Get Excited! (pasiva) permite EXCEDER el tope de 3.0 durante el reseteo → en Jinx, la velocidad de ataque rinde más que en otros tiradores.

### 2.3 Jinx — cambios directos 7.3

|   |   |   |
|---|---|---|
|Stat/Habilidad|Antes|Ahora|
|AD por nivel|4.5|4 (nivel 15: 116 → 114 AD base)|
|R — enfriamiento|50/45/40|60/50/40|
|R — ratios AD bonus|15 % → 150 %|12 % → 120 %|

Todo lo demás intacto: pasiva (140 % MS + 25 % AS bonus + 10 % maná faltante, 6 s), Pow-Pow (3 cargas, +35/60/85/110 % AS a rango 4), Fishbones (+80/95/110/125 rango, 112 % AD en área, 20 maná/ataque), W (10/80/150/220 + 160 % AD, slow 30–60 %), E (70–280 + 100 % AP… físico-no: mágico, root 1.45–1.75 s).

### 2.4 Ítems de marksman (reforma completa)

Nuevos: Hexoptics C44 (2900) · Yun Tal Wildarrows (3100) · Fiendhunter Bolts (2650) · Stormrazor regresa (3000) · Immortal Shieldbow regresa (3000). Componentes nuevos: Noonquiver (1300: 20 AD + 15 % crítico) y Hearthbound Axe (1200: 20 AD + 15 % AS); Kircheis Shard ya no da AD (800: 20 % AS); Dagger baja a 400g/12 %; Recurve Bow baja a 900g/20 %.

Eliminados: Magnetic Blaster (su poder se repartió entre Stormrazor/RFC/Fiendhunter), Cloak of Agility, Soul Transfer, Nashor’s Talon, Stinger.

Cambios clave para Jinx:

|   |   |
|---|---|
|Ítem|7.3|
|Runaan’s Hurricane|2650g · 40 % AS · 25 % crítico · 4 % MS · rayos al 55 % AD que ahora pueden critar (antes no tenía crítico)|
|Bloodthirster|3200g · 75 AD · 15 % lifesteal · ya NO da crítico ni vida — ítem de AD puro|
|Kraken Slayer|2900g · 45 AD · 35 % AS · cada [3.er](http://3.er) golpe: 120–168 físico (rango), +0.75 % por 1 % de vida faltante del objetivo (máx +75 %)|
|Rapid Firecannon|2650g · 25 % crítico · 40 % AS · Energized: +80 mágico y +35 % rango (máx +150)|
|Infinity Edge|3400g · 75 AD · 25 % crítico · crítico 200 → 230 %|
|Lord Dominik’s|3300g · 35 AD · 35 % pen · 25 % crítico · Giant Slayer hasta +12 % vs ≥1200 HP bonus|
|Mortal Reminder|3000g · 35 AD · 30 % pen · 25 % crítico · Heridas Graves 50 % (ya no da AS)|
|Hexoptics C44|2900g · 55 AD · 25 % crítico · +0–10 % daño según distancia (máx a 550) · +100 rango 8 s tras takedown|
|Yun Tal Wildarrows|3100g · 50 AD · 25 % AS · crítico 0 → 25 % acumulable (0.2 %/ataque a distancia = 125 ataques) · Flurry|
|Fiendhunter Bolts|2650g · 25 % crítico · 45 % AS · 20 haste de R · tras la R: 3 ataques con +50 % AS y crítico garantizado (80 % del daño crítico; si ya critaba, +15 % verdadero)|
|Stormrazor|3000g · 50 AD · 25 % crítico · 20 % AS · Energized: +120 mágico y +45 % MS 1.5 s|
|Immortal Shieldbow|3000g · 55 AD · 25 % crítico · Lifeline: escudo 300–550 al caer bajo 35 % (70 s)|
|Galeforce|3100g · 60 AD · 25 % crítico · 4 % MS · dash + 3 misiles ejecutores (ya no da AS)|
|Phantom Dancer|2650g · ya NO da AD · 25 % crítico · 40 % AS · 7 % MS + stacks|
|Essence Reaver|3000g · 50 AD · 25 % crítico · 20 haste · Spellblade 135 % AD base + 0–80 según crítico|
|Mercurial Scimitar|3100g · 45 AD · 40 MR · 12 % lifesteal (antes physical vamp) · activo Quicksilver|
|Statikk Shiv|rehecho para on-hit (40 AD/40 AP/30 % AS, cadena que aplica on-hit)|
|Guinsoo’s|3000g · 35 AD/30 AP/30 % AS · ya sin restricción de crítico pero sin crítico|
|Navori Quickblades|2650g · 40 % AS · 25 % crítico · ataques reducen CDs básicos 15 %|
|BotRK|3100g · 30 % AS (nerf) · 12 % lifesteal · 6–8.5 % vida actual|
|Wit’s End|2800g · 50 % AS · 45 MR · 20 % tenacidad · +40 mágico on-hit|
|Terminus|3000g · 35 AD/35 % AS · stacks de pen doble|

### 2.5 Botas: sistema Tier 2 → Tier 3

- Berserker’s Greaves (1200g): 35 % AS · 45 MS · Blessed Blade (10 HP por golpe).
- Gunmetal Greaves (2200g, mejora disponible DESPUÉS del minuto 10:00): 50 % AS · 45 MS · 5 % lifesteal · Blessed Blade (12 HP/golpe) · Noxian Gait (+7 % MS al golpear campeones, decae en 2 s).
- Otras T3: Chainlaced Crushers (vs AP/CC), Armored Advance (vs AD), Immortal Treads, Crimson Lucidity, Spellslinger’s, Armorcrusher.
- Los encantamientos de botas dejaron de existir en 7.2. QSS/Scimitar son ítems de inventario normal.

### 2.6 Lifesteal vs Physical Vamp (nuevo stat)

Lifesteal ahora solo sana de ataques básicos, daño on-hit y habilidades tratadas como ataque básico. Tus cohetes de Fishbones son ataques básicos → el lifesteal funciona al 100 % con Jinx (Bloodthirster, Gunmetal Greaves, Scimitar, BotRK). El physical vamp (que sanaba de todo) desapareció de los ítems de ADC.

### 2.7 Runas

- Lethal Tempo rehecho (7.3): ataques a campeones apilan 6.4 % AS (rango) × 6 cargas = 38.4 %, 6 s. A cargas máximas, cada ataque dispara una bala de 6–24 daño adaptativo (rango), y cada 1 % de AS bonus aumenta esa bala +0.67 % → con ~350 % de AS bonus la bala pega ~80 por golpe. Sinergia perfecta con Jinx (AS alta y sostenida) y con botas Gunmetal.
- Legend: Alacrity: 3 % AS + hasta 18 % adicional con takedowns (~18–21 % total; el ejemplo oficial de Caitlyn usa 18 %).
- Legend: Tenacity eliminada → nueva Legend: Haste (hasta 15 haste). Ingenious Hunter eliminada.
- Mercury’s Treads ahora da tenacidad significativa (30 %).

### 2.8 Campo de batalla (afecta tu macro, no tu build)

- Torretas: exteriores 3000 → 7000 HP; placas permanentes (90/75/55/30/0 %), 140g/placa exterior (700g total), decaen −10g/30 s desde el 5:00 (mín 100g).
- Crystalline Overgrowth: las torretas acumulan cristales; tu primer ataque los detona infligiendo daño verdadero = 3.3–18.9 % de la vida máxima de la torreta (según nivel promedio del equipo; ciclo ~50 s, se suprime si hay enemigos cerca). Con torretas de 7000 HP son hasta ~1300 de daño verdadero gratis por ventana — y Jinx con 700 de rango (Fishbones) es la mejor detonadora del juego.
- Minions: ahora infligen 60 % de daño a campeones (lane más seguro), +25 MS cada 150 s desde 5:30; buffs de push para el equipo con ventaja.
- Jungla: monstruos más duros vs no-jungla y Smite mejorado (600→1000→1400) → robar campamentos es más arriesgado; krugs/raptors/gromp ahora pegan con % de vida actual.

---

## 3. MODELO MATEMÁTICO (todo lo que sigue sale de aquí)

Datos de entrada (nivel 15): AD base = 58 + 4×14 = 114 · AS base = ratio = 0.625 · bonus fijo = 0.30 (base) + 0.28 (niveles) = 0.58 · crítico base = 200 %, con IE = 230 %.

Fórmulas:

AS_total      = 0.625 × (1 + 0.58 + AS_items + Q4(1.10) + LT(0.384) + Alacrity(~0.21))

                tope 3.0 (Get Excited lo rompe: +25 % AS bonus)

  

Daño/ataque   = AD_total × 1.12 (cohete) × [1 + crit% × (daño_crit − 1)] × 1.10 (C44 a ≥550 de distancia)

  

DPS 1v1       = AS × Daño/ataque + AS/3 × Kraken(168×1.375 prom.) + AS × Bala_LT(24 × (1+0.0067×AS_bonus%))

                + AS/7 × Energized(RFC 80 / Stormrazor 120) + AS × on-hit

  

DPS N-objetivos = DPS 1v1 (la explosión pega a todos por igual)

                + AS × Daño/ataque × (min(N,4) − 1)          ← splash de Fishbones

                + AS × 2 × 0.55 × AD × mult_crit             ← rayos de Runaan's (critan)

  

Mitigación    = × 100 / (100 + Armadura × (1 − pen%))

LDR Giant Slayer = +12 % vs campeones con ≥1200 HP bonus

Supuestos declarados: LT y Alacrity a cargas máximas; Pow-Pow rango 4 (3 cargas, +110 %); Magnification de C44 siempre al 10 % (Jinx ataca a ≥575 de rango, y el máximo se alcanza a 550); la bala de LT escala con el AS bonus total (incluye el 0.58 intrínseco); Kraken promedia +37.5 % por vida faltante; los rayos de Runaan’s no heredan Magnification (conservador); W/E/R fuera del cálculo de DPS sostenido (la W añade ~150 DPS extra con AD 324, CD 5 s).

---

## 4. LAS TRES LEYES QUE SE DERIVAN DEL MODELO

### Ley 1 — Crítico: llega a 100 % EXACTO; ni 99 ni 125

Multiplicador promedio = 1 + crit × (daño_crit − 1). Con IE, cada punto de crítico rinde ×1.3:

|   |   |   |   |
|---|---|---|---|
|Crítico|Mult. sin IE|Mult. con IE|Ganancia IE|
|0 %|1.00|1.00|—|
|25 %|1.25|1.325|+6.0 %|
|50 %|1.50|1.65|+10.0 %|
|75 %|1.75|1.975|+12.9 %|
|100 %|2.00|2.30|+15.0 %|

De 75 % → 100 % (con IE) ganas +16.4 % de DPS global. Cada 1 % de crítico cuesta ~50g (Brawler’s Gloves). El crítico por encima de 100 % es oro muerto (no hay conversión en Jinx).  
Combo exacto de 100 %: C44 (25) + Runaan’s (25) + IE (25) + LDR/Mortal (25) = 100.0 %. Los ítems críticos que agregues después (Galeforce, Shieldbow, PD, Fiendhunter, Collector) desperdician sus 25 % de crítico (~1250g de stats muertos por ítem). Esto descalifica matemáticamente varias rutas populares, incluida la build de comunidad con Galeforce de 6.º ítem.

### Ley 2 — Velocidad de ataque: apunta a 3.0, no la revientes

Con Q4 + LT + Alacrity, el bonus fijo es 2.274. Para tocar el tope de 3.0 exacto:

AS_items_necesaria = (3.0 / 0.625 − 1) − 2.274 = 1.526  → 152.6 % de AS de ítems

|   |   |   |   |
|---|---|---|---|
|Combo de ítems|AS de ítems|AS cruda|Veredicto|
|Gunmetal + Runaan’s|90 %|2.61|base sana, hueco para 1 ítem de AS|
|Gunmetal + Runaan’s + Kraken|125 %|2.83|✅ óptimo (94 % del tope; con Get Excited → 2.98, y la pasiva permite exceder)|
|Gunmetal + Runaan’s + RFC|130 %|2.86|✅ ok|
|Gunmetal + Runaan’s + RFC + Kraken (tu build con mejora)|165 %|3.08|⚠️ overcap: 2.6 % desperdiciado SIN contar Get Excited|
|Berserker’s + Kraken + RFC + Runaan’s (tu build real)|150 %|2.98|al filo — y Berserker’s regala 15 % AS vs Gunmetal|
|On-hit (Gunmetal+Kraken+WE+Terminus+BotRK+Runaan’s)|230 %|3.55|❌ 18 % de AS tirada a la basura|

Regla: 3 fuentes de AS (botas T3 + Runaan’s + Kraken/RFC) son el techo sensato. La AS sobrante solo vale durante Get Excited.

### Ley 3 — Penetración % obligatoria a partir del ítem 4–5

Multiplicador de daño real 100/(100+arm×(1−pen)):

|   |   |   |   |
|---|---|---|---|
|Armadura enemiga|pen 0 %|pen 35 % (LDR)|Ganancia|
|80 (carry frágil)|0.556|0.658|+18 %|
|120 (carry con ítems)|0.455|0.562|+23.5 %|
|220 (tanque)|0.312|0.412|+32 %|
|300 (tanque full)|0.250|0.339|+36 %|

Y LDR añade +12 % adicional (Giant Slayer) vs tanques con ≥1200 HP bonus → vs tanque full: +47 % de daño real respecto a no llevar pen. Tu build tenía 0 %: por eso te “superaron ampliamente” en el mid-late aunque el DPS crudo pareciera similar.  
Contra 2+ tanques muy curativos: Mortal Reminder (30 % pen, 3000g) en lugar de LDR. ¿Doble pen (LDR+Mortal)? Solo vs 3 tanques: sacrifica tu 6.º ítem de DPS/defensa y el crítico sobrante se desperdicia; el modelo dice que no vale salvo partidas extremas.

---

## 5. ANÁLISIS DEL PRIMER ÍTEM (tu duda sobre Hexoptics C44, resuelta con números)

Primero, la corrección importante sobre C44: su pasiva fuerte, Magnification (+0–10 % de daño según distancia, máximo a 550 unidades), NO requiere kills — es pasiva por distancia. Jinx ataca a 575 base y 655–700 con Fishbones: el +10 % está activo en el 100 % de tus ataques con cohetes. Lo único que requiere un takedown es Arcane Aim (+100 rango, 8 s), que es la cereza, no el pastel. Con Magnification, C44 equivale a ~157 % de eficiencia de oro (la más alta del parche junto a IE y LDR). Tu razón para descartarlo (“si no hago kill no aprovecho el rango”) aplicaba solo a la pasiva secundaria; la primaria la estabas regalando.

Simulación (misma base: Long Sword start, Q rango 3, Alacrity parcial, LT full):

|   |   |   |   |   |   |
|---|---|---|---|---|---|
|Primer ítem|Oro|Nivel 9 · 1v1|Nivel 9 · 3v3|Nivel 12 (2 ítems+botas) 1v1|Nivel 12 · 3v3|
|Hexoptics C44|2900|534|1437|864 (con Runaan’s)|2937|
|Kraken Slayer|2900|611|1288|934 (con Runaan’s)|2584|
|Stormrazor|3000|550|1391|870 (con Runaan’s)|2845|
|Yun Tal Wildarrows|3100|521*|1375*|837 (con Runaan’s)|2836|
|Essence Reaver|3000|478|1271|—|—|

*Yun Tal asumiendo 25 % de crítico completo (125 ataques); a los 8–9 min reales trae ~10–18 %.

Lectura honesta: Kraken primero gana el duelo 1v1 temprano (+14 %), pero pierde en equipo (−10 % a 3 objetivos) porque no critica el splash. C44 gana donde Jinx gana partidas: push, sieges y teamfights — y su ventaja explota al combinarse con IE (crítico multiplicativo). En el checkpoint de nivel 14 con 3 ítems: C44+Runaan’s+IE = 1697 DPS/6078 AoE vs Kraken+Runaan’s+IE = 1625/5189 (+17 % AoE).

- Yun Tal, rechazado: cuesta 200g más que C44, su crítico tarda 125 ataques en completarse (ventana donde rinde por debajo de la tabla), y su Flurry (+25 % AS) empuja al overcap más adelante. Rompe la Ley 1 (crítico “progresivo” imposible de cuadrar a 100 exacto).
- Stormrazor, alternativa legítima: si tu problema real es presión en early y no poder farmear (§9), Stormrazor da el Energized de 120 + 45 % MS para kitear desde el minuto 7–8. Cuesta ~9 % de DPS late vs C44 pero gana la lane. No lo combines con RFC después (dos Energized compiten).
- Dato curioso del modelo: si vas muy feedeado, C44 → IE directo (saltándote Runaan’s) es el pico de 2 ítems más fuerte del juego a nivel 12 (1168 DPS 1v1 / 3261 3v3). Runaan’s segundo es la ruta estable; IE segundo es la ruta snowball.
- ER, rechazado: su Spellblade (135 % AD base + hasta 80) rinde ~156 DPS a nivel 15, muy por debajo de lo que dan 3000g en Kraken/BT/C44; Jinx no necesita maná tanto como DPS (ver §9 para el maná).

---

## 6. LA BUILD ÓPTIMA — ENSAMBLADA PIEZA POR PIEZA

Ranura por ranura (por qué cada ítem y no otro):

|   |   |   |
|---|---|---|
|Slot|Ítem|Justificación matemática|
|Botas|Berserker’s → Gunmetal Greaves|+15 % AS sobre Berserker’s por 1000g (disponible al 10:00), +5 % lifesteal, 12 HP/golpe (≈34 HP/s a AS 2.83), +7 % MS al golpear → kiteo. Estrictamente dominante.|
|1|Hexoptics C44 (2900)|157 % eficiencia; +10 % permanente con cohetes; 25 % crítico; build path suave (Pickaxe→Noonquiver→Long Sword).|
|2|Runaan’s Hurricane (2650)|El ítem más sinérgico del juego con Fishbones: splash que critica + 2 rayos que critan = en 3v3 sumas ~+2500 DPS. 40 % AS + 25 % crítico al precio más bajo (131 % eficiencia con passive incluido).|
|3|Infinity Edge (3400)|A 50–75 % crítico, el salto 200→230 % multiplica TODO (splash y rayos incluidos): +12.9–15 % de DPS global instantáneo. 163 % eficiencia. Capstone obligatorio.|
|4|Lord Dominik’s (3300)|Cierra el 100 % de crítico exacto (Ley 1), +35 % pen (Ley 3: +23–32 % de daño real), +12 % vs tanques. 163 % eficiencia. → Mortal Reminder (3000) si ≥2 fuentes de curación enemigas.|
|5|Kraken Slayer (2900)|Último slot sin crítico desperdiciado que suma DPS: 45 AD + 35 % AS (lleva AS cruda a 2.83, 94 % del tope — Ley 2) + proc de 168–294 cada 3 golpes (+~218 DPS).|

DPS resultante (nivel 15, pre-mitigación): AD 324 · AS 2.83 · crítico 100 % @230 % · pen 35 % → 3042 (1v1) / 10 551 (3v3) / 1709 vs 120 arm / 1380 vs tanque.

### Matriz del 6.º ítem (slot 5 de la tabla = decisión situacional real)

|   |   |   |   |
|---|---|---|---|
|Situación|Ítem|Coste|Impacto medido|
|DPS máximo (default)|Kraken Slayer|2900|3042 DPS · AS al 94 % del tope|
|Sustain / poke enemigo / peleas largas|Bloodthirster|3200|2813 DPS (−7.5 %) + ~594 HP/s de lifesteal + escudo 165–345|
|CC duro + AP (Zed no, pero Ahri/Ashe/Sup CC)|Mercurial Scimitar|3100|2591 DPS + Quicksilver + 40 MR + 472 HP/s|
|Burst AD / asesinos (Zed, Rengar, Yasuo)|Guardian Angel|3200|2591 DPS + revivir (sin crítico desperdiciado, a diferencia de Shieldbow)|
|Doble AP + quieres topar AS|Wit’s End|2800|~2670 DPS + 45 MR + 20 % tenacidad + on-hit 40|
|Dive constante sobre ti|Galeforce|3100|2702 DPS + dash — ⚠️ desperdicia 25 % crítico (~1250g muertos): solo si el dash vale más que el DPS|
|Composiciones de R-window (peleas cortas)|Fiendhunter Bolts|2650|2523 DPS + 20 haste de R + ventana de 3 cohetes críticos garantizados (+15 % verdadero extra a 100 % crit) cada ~33 s — ⚠️ también rompe el 100 % exacto si llevas LDR|

Ítems que el modelo RECHAZA para Jinx 7.3 (y por qué):

- Rapid Firecannon: 1v1 casi idéntico a Kraken como 5.º (3074 vs 3042 con Gunmetal+C44+RFC+IE+LDR+Kraken), pero −22 % de DPS en 3v3 (≈8270 vs 10 551) porque sustituye los rayos críticos de Runaan’s. Solo en composiciones de siege puro (su Energized de +150 rango con Fishbones = 850 de alcance para detonar cristales y placas). Tu apego al RFC es entendible, pero Runaan’s lo domina en todo excepto rango.
- Ruta on-hit (Guinsoo/Terminus/Wit’s End/BotRK/Statikk): 1721 DPS = −43 % vs la ruta crítica. Con crítico base a 200 % y cohetes que critan en área, el on-hit diluye el multiplicador. Además revienta el tope de AS (3.55 cruda).
- Phantom Dancer como 5.º/6.º: en 7.3 ya no da AD; con crítico al tope pagas 2650g por AS que casi no cabe (overcap) + MS. El MS lo cubren Gunmetal/Ghost/Runaan’s.
- Immortal Shieldbow: Lifeline es bueno, pero su 25 % crítico sobra en esta build (~1250g muertos) → GA (vs AD) o Scimitar (vs CC/AP) defienden mejor por slot.
- Manamune/Muramana, Trinity Force, Divine Sunderer, Hexplate, Sundered Sky, Collector: stats de luchador/snowball que no multiplican el splash crítico; Collector solo si vas 3/0 y quieres ejecutar+oro, pero Kraken/BT rinden más.
- Navori Quickblades: teórico cañón de W-spam, pero su 25 % crítico rompe el 100 % exacto y la reducción de CD “15 % por ataque” necesita validación en juego; sin números confiables, fuera de la recomendación principal.

---

## 7. RUNAS, HECHIZOS Y ORDEN DE HABILIDADES

Keystone — Lethal Tempo (rehecho 7.3): 38.4 % AS a 6 cargas + bala adaptativa que escala 0.67 % por cada 1 % de AS bonus. Con esta build (~353 % de AS bonus en pelea) la bala pega ~81 por golpe ≈ +230 DPS gratis. Es la keystone que más crece con exactamente los stats que ya compras.

- Alternativa lane difícil: Fleet Footwork (40 % AS en la proc + cura 15–110 + 20 % MS) para lanes de poke donde no puedas mantener cargas de LT.
- Alternativa greedy: First Strike (+7 % daño verdadero y oro) si el matchup te deja pokear gratis con W desde 650+.

Secundarias (4 slots):

|   |   |   |
|---|---|---|
|Slot|Elección|Razón|
|Precisión|Legend: Alacrity|~21 % AS = +7–8 % DPS + alimenta la bala de LT (0.67 %/1 %)|
|Precisión/Dom|Brutal|~5 + 6 % AD bonus de daño adaptativo por golpe ≈ +50 DPS constante|
|Precisión|Coup de Grace (default) o Triumph (vs burst)|+8 % a objetivos <40 % — tu W y tu R rematan; Triumph: 10 % HP + maná por takedown, combo con Get Excited para resetear peleas|
|Resolve/Sorcery|Bone Plating (vs burst en lane) · Celerity (2 % MS + 7 % a TODO tu MS: Ghost+Get Excited+Noxian Gait → kiteo extremo) · Nullifying Orb (vs asesinos AP) · Manaflow Band (si sufres maná con spam de cohetes)|situacional|

Hechizos: Flash + Ghost. Ghost se extiende con takedowns → combina con Get Excited (140 % MS) para el patrón “kill → reset → persecución” que define a Jinx. Heal solo si tu support no lo trae y hay mucho burst.

Habilidades: Q al 1, W al 2, E al 3; maxear Q (rango +125 y AS +110 % son tu identidad), luego W (220 + 160 % AD, CD 5 s = ~150 DPS extra), E al final. R en 5/9/13.

---

## 8. COMPARACIÓN DIRECTA: TU BUILD vs LA ÓPTIMA (nivel 15, mismos supuestos)

|   |   |   |   |   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|---|
|Build|Oro|AD|AS|Crit|Pen|DPS 1v1|DPS 3v3|vs 120 arm|vs tanque|Heal/s|
|Tu build adaptada viable (Ber+Kraken+RFC+Runaan’s+IE+BT)|16 000|309|2.98|75 %|0 %|2556|8638|1162|799|383|
|Tu build con Gunmetal y sin RFC (Ber→Gun, +Scimitar)|17 450|354|2.83|50 %|0 %|2296|7812|1043|717|768|
|Meta comunidad (C44→Runaan’s→IE→LDR→Gale)|17 550|339|2.61|100 %*|35 %|2702|9951|1518|1236|166|
|ÓPTIMA Kraken (propuesta)|17 350|324|2.83|100 %|35 %|3042|10 551|1709|1380|186|
|ÓPTIMA Bloodthirster|17 650|354|2.61|100 %|35 %|2813|10 383|1580|1287|594|
|ÓPTIMA Scimitar (vs CC)|17 550|324|2.61|100 %|35 %|2591|9519|1456|1184|472|
|Ruta on-hit (referencia)|16 650|234|3.55†|25 %|30 %|1721|4652|935|678|329|

* La build de comunidad llega a 125 % (Galeforce desperdicia 25 %). † AS cruda con overcap.

Desglose de la diferencia ÓPTIMA vs TU BUILD (1v1: +19 %; vs armadura: +47 %; vs tanque: +73 %):

1. Crítico 100 % @230 % vs 75 % @230 % → +16.4 %
2. Magnification de C44 (tu build no lleva C44) → +10 %
3. Pen 35 % + Giant Slayer vs 0 % → +23.5 % vs carries / +47 % vs tanques
4. Gunmetal vs Berserker’s → +15 % AS efectiva, +5 % LS, +MS de combate
5. Sin overcap de AS (tu combo RFC+Kraken+Runaan’s al borde/por encima del tope según botas)

Lo único donde tu build gana: heal/s (BT+Scimitar). La variante D (ÓPTIMA-BT) conserva el 92 % del DPS óptimo con 594 HP/s — si el sustain es tu prioridad, esa es tu build, no la de RFC.

---

## 9. PLAN DE JUEGO EARLY/MID (tu problema declarado: “mucha presión encima”)

1. Start: Long Sword (500) + poción. Primer recall: Pickaxe (800) si tienes poco, Noonquiver (1300) si la lane es segura (20 AD + 15 % crítico = el componente más eficiente del early para Jinx).
2. Maná: Fishbones cuesta 20/ataque; con AS 2.0 son ~40 maná/s. Regla: Pow-Pow para farmear, Fishbones solo para trades/push. Get Excited devuelve 10 % del maná faltante por takedown (también torretas y épicos). Si aun así sufres: Manaflow Band (+300 maná) o buff azul.
3. Bajo presión (te pushean/zonan): cambia C44 por Stormrazor (Energized de 120 + 45 % MS por proc = kiteo desde el minuto 8) y/o keystone Fleet Footwork. Berserker’s temprano (1200g, minuto 8–9) antes que el 2.º componente caro.
4. Placas de torreta: desde el 5:00 decaen 10g/30 s. Cada 3 ataques a torreta con Demolish (si lo llevas) = 50 + 20 % HP máx. Con 7000 HP y 5 placas, una torre exterior bien trabajada = ~700g + 150g first blood de torre. Jinx con Fishbones derriba placas desde 700 de rango sin entrar en zona de amenaza.
5. Cristales (Crystalline Overgrowth): cada ~50 s la torreta acumula cristales; un solo ataque los detona (hasta ~1300 de daño verdadero en late). Pasa por la torre, pega UN cohete y vete — es oro/estructura gratis que tu rango de 700 hace trivial. Ojo: no se detonan si la torreta tiene reducción de daño activa (sin minions) ni se acumulan con enemigos cerca.
6. Reset de peleas: el patrón de oro de Jinx en 7.3: R desde lejos → kill/assist → Get Excited (25 % AS que rompe el tope de 3.0 + 140 % MS + maná) → Ghost → Fishbones a 700 de rango limpiando lo que queda. La build propuesta maximiza exactamente esa ventana (AS al 94 % del tope sin buffs = con pasiva estás por encima).
7. No contestes jungla enemiga sola antes del minuto 10: los monstruos 7.3 pegan con % de vida actual y el Smite rival hace 600–1400 de daño verdadero.

---

## 10. VERIFICACIONES, DISCREPANCIAS Y SUPUESTOS (honestidad de datos)

- Fuentes primarias: notas oficiales 7.3 (21/09/2026) y 7.2 (08/07/2026) de [wildrift.leagueoflegends.com](http://wildrift.leagueoflegends.com) — de ahí salen: sistema de crítico 200/230 %, nuevo sistema de AS + tope 3.0, datos de Jinx (0.625/0.30/0.02; AD 4/nivel; R 60/50/40 y 12–120 %), Lethal Tempo rehecho, todos los cambios de ítems citados, sistema de botas T3 (regla del minuto 10:00), QSS/Scimitar como ítems de clase, lifesteal nuevo, torretas/cristales/minions.
- Fuente secundaria (stats no tocados en 7.3): base de datos [wr-meta.com](http://wr-meta.com) actualizada al 24/09/2026 — precios y stats completos de los 228 ítems, habilidades de Jinx (112 % cohetes, +80/95/110/125 rango, Pow-Pow 35/60/85/110, W 220+160 %, pasiva 140 % MS/25 % AS/10 % maná), runas menores.
- Discrepancias detectadas y resolución: (a) Lethal Tempo: wr-meta muestra el texto viejo (4.8 %/carga, bala 6–20, +0.33 %); usé el oficial 7.3 (6.4 %, 6–24, +0.67 %). (b) Legend: Alacrity: 21 % (descripción) vs 18 % (ejemplo oficial de Caitlyn); usé 21 % — con 18 % el DPS baja <1 %. © Noxian Gait de Gunmetal: 10 % (notas 7.2) vs 7 % (BD post-7.3); usé 7 %.
- Supuestos del modelo: Magnification siempre al 10 % (distancia ≥550); LT/Alacrity/Q a cargas máximas en pelea; Kraken promedia +37.5 % por vida faltante; bala de LT escala con AS bonus total; Runaan’s no hereda Magnification; la W/E/R no cuentan en el DPS sostenido (añaden ~150+ de burst rotacional); el daño crítico a torretas se excluyó (conservador); splash de Fishbones golpea hasta 4 objetivos.
- Contexto meta (24/09, Diamond+): Jinx 49.8 % WR / 11.0 % pick / 0.5 % ban, tendencia ↑ — solo 3 días de datos post-parche; el ecosistema de marksmen se recolocará (la reforma es masiva). Esta build está diseñada para el estado 7.3 tal como está publicado hoy.

---

## APÉNDICE A — POOL COMPLETO DE ÍTEMES DE TIRADOR EN 7.3 (veredicto para Jinx)

|                                                      |                                                                  |                                                                                 |
| ---------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Ítem (oro)                                           | Stats 7.3                                                        | Veredicto Jinx                                                                  |
| Hexoptics C44 (2900)                                 | 55 AD · 25 % crit · +10 % dmg a distancia · +100 rango post-kill | ✅ Ítem 1 — 157 % eficiencia                                                     |
| Runaan’s Hurricane (2650)                            | 40 % AS · 25 % crit · 4 % MS · rayos 55 % que critan             | ✅ Core 2 — rey del AoE con splash                                               |
| Infinity Edge (3400)                                 | 75 AD · 25 % crit · crit → 230 %                                 | ✅ Core 3 — capstone multiplicativo                                              |
| Lord Dominik’s (3300)                                | 35 AD · 35 % pen · 25 % crit · +12 % vs bonus HP                 | ✅ Core 4 — cierra 100 % crit + pen                                              |
| Mortal Reminder (3000)                               | 35 AD · 30 % pen · 25 % crit · GW 50 %                           | ✅ Reemplaza LDR vs mucha curación                                               |
| Kraken Slayer (2900)                                 | 45 AD · 35 % AS · 4 % MS · proc 120–168 (+75 % máx)              | ✅ 6.º default — mejor DPS/slot sin crit                                         |
| Bloodthirster (3200)                                 | 75 AD · 15 % LS · escudo de overheal 165–345                     | ✅ 6.º sustain                                                                   |
| Mercurial Scimitar (3100)                            | 45 AD · 40 MR · 12 % LS · QSS activo                             | ✅ 6.º vs CC/AP                                                                  |
| Guardian Angel (3200)                                | 45 AD · 40 Armor · revivir                                       | ✅ 6.º vs AD burst                                                               |
| Wit’s End (2800)                                     | 50 % AS · 45 MR · 20 % tenacidad · +40 on-hit                    | ✅ 6.º vs doble AP (AS al tope justo)                                            |
| Galeforce (3100)                                     | 60 AD · 25 % crit · dash + 3 misiles (40–125 + 35 % AD bonus)    | ⚠️ Solo vs dive pesado — desperdicia 25 % crit                                  |
| Stormrazor (3000)                                    | 50 AD · 25 % crit · 20 % AS · Energized 120 + 45 % MS            | ⚠️ [1.er](http://1.er) ítem anti-presión (alternativa a C44)                    |
| Rapid Firecannon (2650)                              | 25 % crit · 40 % AS · Energized 80 + 150 rango                   | ⚠️ Solo siege; Runaan’s lo domina en fights                                     |
| Fiendhunter Bolts (2650)                             | 25 % crit · 45 % AS · 20 ult haste · 3 crits garantizados post-R | ⚠️ Niche de R-window; rompe el 100 % exacto                                     |
| Immortal Shieldbow (3000)                            | 55 AD · 25 % crit · Lifeline 300–550                             | ⚠️ GA/Scimitar defienden mejor por slot aquí                                    |
| Phantom Dancer (2650)                                | 25 % crit · 40 % AS · 7 % MS + stacks                            | ❌ Sin AD en 7.3; crit sobrante; MS duplicado                                    |
| Yun Tal Wildarrows (3100)                            | 50 AD · 25 % AS · crit 0→25 % (125 ataques)                      | ❌ Ramp lenta, caro, rompe Ley 1                                                 |
| Essence Reaver (3000)                                | 50 AD · 25 % crit · 20 haste · Spellblade                        | ❌ Spellblade < Kraken/BT en DPS/slot                                            |
| Navori Quickblades (2650)                            | 25 % crit · 40 % AS · −15 % CD básicos                           | ❌ Crit sobrante; sin validar mecánica de CD                                     |
| The Collector (3000)                                 | 50 AD · 10 pen plana · 25 % crit · execute 5 %+25g               | ❌ Niche snowball; crit sobrante con LDR                                         |
| Statikk Shiv (3000)                                  | 40 AD/40 AP · 30 % AS · cadena on-hit                            | ❌ Ítem on-hit/híbrido, no para crit Jinx                                        |
| Guinsoo’s Rageblade (3000)                           | 35 AD/30 AP · 30 % AS · doble on-hit                             | ❌ Ruta on-hit = −43 % DPS                                                       |
| BotRK (3100)                                         | 40 AD · 30 % AS · 12 % LS · 6 % vida actual                      | ❌ % vida actual rinde poco con tu poco AD base y splash                         |
| Terminus (3000)                                      | 35 AD · 35 % AS · pen stacks                                     | ❌ On-hit; LDR hace pen mejor en ruta crit                                       |
| Manamune/Muramana (2900)                             | 40 AD · maná · Shock                                             | ❌ Stackeo lento, sin crit                                                       |
| Trinity/Divine/Hexplate/Sundered/Shojin/Hullbreaker  | —                                                                | ❌ Ítems de luchador                                                             |
| Botas: Mercury’s→Chainlaced / Plated→Armored Advance | 2200                                                             | ⚠️ Solo si el CC/burst es inmanejable (pierdes 50 % AS de Gunmetal ≈ −12 % DPS) |

## APÉNDICE B — RESUMEN DE RUTAS DE COMPRA

DEFAULT:    LS → Pickaxe/Noonquiver → C44 (7-8') → Berserker's (9-10') → Runaan's (11-12')

            → Gunmetal T3 (13', tras 10:00) → IE (15-16') → LDR (18-19') → Kraken (21')

SNOWBALL:   ... → C44 → IE 2.º (pico brutal a nivel 12) → Runaan's → Gunmetal → LDR → BT/Kraken

ANTI-PRESIÓN: LS → Stormrazor → Berserker's → Runaan's → Gunmetal → IE → LDR → Kraken/BT

VS 2+ TANQUES: C44 → Berserker's → Runaan's → Gunmetal → IE → LDR → Mortal Reminder (6.º) → Kraken se cae

VS CC DURO:   default pero 6.º = Mercurial Scimitar (QSS 1100g temprano si hay Blitzcrank/Ashe-like)

VS BURST AD:  default pero 6.º = Guardian Angel

VS DOBLE AP:  default pero 6.º = Wit's End (AS queda en 2.92 cruda, perfecta)

---

Reporte generado el 25/09/2026 con datos del parche 7.3 (21/09/2026). Modelo propio: las cifras de DPS son pre-mitigación y comparativas — el valor absoluto importa menos que las diferencias relativas entre builds, que son robustas a los supuestos. Si Riot publica un 7.3a/b (hotfix), los números de ítems podrían moverse ±5 %.