# Biofónica

Proyecto de **Ableton Live 12** para conciertos largos (&gt;15 min) con el controlador **[TouchMe](https://shop.playtronica.com/products/touchme)** de Playtronica: la piel humana (y el contacto entre personas) actúa como el “órgano” principal, sobre un fondo suave inspirado en la banda sonora de *Interestelar*.

## Contenido

| Archivo | Descripción |
| --- | --- |
| `Biofónica.als` | Live Set listo para abrir (Session View). |
| `build_biofonica.py` | Regenera el `.als` si cambias presets. |

## Pistas del Live Set

1. **TouchMe — Órgano (piel)** — Entrada MIDI del TouchMe, órgano tipo iglesia, escala pentatónica menor (La), reverb y delay. Sin clip: todo es improvisación táctil.
2. **Fondo — Pad orgánico** — Pad grueso; clip en bucle 64 compases.
3. **Fondo — Motor graves** — Sub órgano discreto.
4. **Fondo — Bruma WAV** — Capa etérea Wavetable.

Tempo **68 BPM**, tonalidad **La menor / pentatónica**. Un ciclo de fondo dura **64 compases** (~**3,8 min**); al repetirse en bucle puedes tocar **15 minutos o más** sin cortes.

## Concierto rápido (checklist)

1. Abre `Biofónica.als` en Ableton Live 12 Suite (Analog, Operator, Wavetable y Delay/Reverb del Core Library).
2. Conecta el TouchMe por USB (ver abajo).
3. **Preferencias → Enlace MIDI**: activa **Track** y **Remote** en la entrada **TouchMe** (o el nombre que muestre Windows).
4. En la pista **TouchMe**, MIDI From: **TouchMe** (puerto correcto).
5. Pulsa la **escena 1** (o lanza los tres clips de fondo a la vez).
6. **Toca**: una mano en cada terminal del TouchMe (o dos personas, una en cada extremo, tocándose la piel).
7. Para grabar: añade una pista de audio **Resampling** desde **Main**, arma y graba en Arrangement (recomendado para &gt;15 min).

---

## TouchMe — cómo funciona con la piel

El TouchMe mide conductividad entre sus dos puntas. Cuanto mayor es el contacto (manos húmedas, más área de piel, dos cuerpos en cadena), cambian **altura/timbre e intensidad** del sonido vía MIDI.

**Incluido en la caja Playtronica:** TouchMe, cable USB, **2 pinzas cocodrilo** y sobre de guardado.  
**No es sumergible.** No usar con portadores de marcapasos.

### Cableado básico (modo concierto)

```
[TouchMe USB] ──► PC (Ableton)
     │
     ├─ Terminal A ── pinza ──► (piel participante 1 / electrodos / cinta cobre)
     └─ Terminal B ── pinza ──► (piel participante 2 / tierra corporal)
```

**Dúo en escena:** cada persona sujeta un extremo del TouchMe y tocan la piel del otro (antebrazo, mano, nuca suave con consentimiento).

### Hardware de Amazon (tus enlaces)

| Producto | ASIN / enlace | Uso con *Biofónica* |
| --- | --- | --- |
| **Beurer — 16 electrodos de gel 45×45 mm** | [B07L42122D](https://www.amazon.es/dp/B07L42122D) | Zonas de contacto **amplias y estables** en brazos, espalda o torso. Solo como superficie conductora pasiva con el TouchMe. |
| **TIENFOKOTA — 2 cables 3,5 mm hembra → pinza cocodrilo (50 cm)** | [B0GF7X7CNS](https://www.amazon.es/dp/B0GF7X7CNS) | Adapta electrodos snap TENS a las pinzas Playtronica. |
| **FEPITO — cinta de cobre adhesiva conductiva** | [B08FJ6BSG7](https://www.amazon.es/dp/B08FJ6BSG7) | Circuitos corporales / escenografía conductiva. |

### MIDI en Windows

1. Conecta TouchMe y espera a que Windows instale el dispositivo.
2. Ableton → **Preferencias → Enlace MIDI** → **Track** ON en **TouchMe**.

---

## Regenerar el proyecto

```powershell
cd "D:\Dv\Repo\Ableton\Biofonica"
python build_biofonica.py
```

Requisito: **Live 12 Suite** con Core Library en `C:\ProgramData\Ableton\...`

## Créditos

Presets de **Ableton Live**. TouchMe: **[Playtronica](https://shop.playtronica.com/products/touchme)**. Sonido original inspirado en órganos cinematográficos; sin material con copyright de *Interestelar*.