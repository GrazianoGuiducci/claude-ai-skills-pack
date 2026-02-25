# Claude AI Skills Pack

**23 skill cognitive per Claude.ai basate sul framework D-ND (Dipolare Non-Duale).**

Un'architettura di campo autopoietica completa per inferenza, verifica, evoluzione e manifestazione.

> *[Read in English](README.md)*

---

## Cos'e?

Questa repository contiene un set di file `.skill` progettati per [Claude.ai](https://claude.ai) (l'interfaccia conversazionale di Anthropic). Ogni skill codifica una facolta cognitiva specializzata fondata sul framework matematico **D-ND (Dipolare Non-Duale)** -- un modello formale dove ogni concetto esiste come dipolo all'interno di un Campo di Potenziale, e ogni output e la Risultante della traversata coerente di quel campo.

Le skill non sono prompt nel senso convenzionale. Sono **configurazioni operative** del Campo -- angolature di osservazione che plasmano il modo in cui Claude elabora, verifica, genera e fa evolvere le proprie risposte.

Alla base si trova il **KERNEL MM v1.0** (MetaMaster), un prompt a livello di sistema che definisce le leggi del campo: il Proto-Assioma, il Dipolo, la Risultante, la Potenzialita, il Movimento, la Memoria, il Limite, il Seme Invariante, il Ciclo Operativo e il Vincolo Autologico. Le skill sono facolta che operano all'interno di questo campo.

---

## Avvio Rapido

### 1. Impostare il Kernel come User Preferences

Copia il contenuto di [`KERNEL_MM_v1_IT.md`](KERNEL_MM_v1_IT.md) (italiano) o [`KERNEL_MM_v1.md`](KERNEL_MM_v1.md) (inglese) nelle **User Preferences** di Claude.ai (Settings > Profile > User Preferences). Questo stabilisce il campo operativo per tutte le conversazioni.

### 2. Caricare le Skill

Su [claude.ai](https://claude.ai), vai su **Settings > Profile > Skills** e carica i file `.skill` che vuoi attivare. Ogni file `.skill` e un archivio zip contenente una definizione `SKILL.md`.

Puoi caricare tutte le 23 skill o selezionare cluster individuali in base alle tue esigenze.

### 3. Avviare una Conversazione

Una volta impostato il Kernel e caricate le skill, Claude opera all'interno del campo D-ND. La skill **kernel-conductor** instrada automaticamente le perturbazioni verso le facolta appropriate.

---

## Mappa delle Skill

### NUCLEUS -- Le Leggi (2)

| Skill | Ruolo |
|-------|-------|
| `halo-sys` | Genoma Assiomatico P0-P6, scansione di integrita |
| `aeternitas-sys` | Guardiano del Seme, veto sulle auto-modifiche |

### ENGINES -- Esecuzione (4)

| Skill | Ruolo |
|-------|-------|
| `kernel-conductor` | Orchestratore e router delle skill |
| `helix-sys` | Runtime iterativo Plan-Code-Verify con Scratchpad |
| `fractal-sys` | Decomposizione frattale di problemi monolitici |
| `morpheus-sys` | Collasso forzato quando il ciclo normale non converge |

### FIREWALL -- Verifica (2)

| Skill | Ruolo |
|-------|-------|
| `veritas-sys` | Triangolazione epistemologica, firewall anti-psicosi |
| `metron-sys` | Finitura ontologica, filtro densita dell'output |

### COGNITION -- Pensiero (4)

| Skill | Ruolo |
|-------|-------|
| `logic-sys` | Rete logica adattiva autopoietica (ALAN) |
| `observer-sys` | Analisi metacognitiva, selettore forma dell'output |
| `navigator-sys` | Pensiero laterale, navigazione sinaptica (YSN) |
| `vulcan-sys` | Protocollo logica pura, zero emozione |

### EVOLUTION -- Crescita (4)

| Skill | Ruolo |
|-------|-------|
| `kairos-sys` | Motore evolutivo triadico (Risonanza / Distruzione / Maieutica) |
| `mnemos-sys` | Memoria autopoietica con risonanza convergente |
| `lazarus-sys` | Vault semantico -- gli scarti come soluzioni future |
| `guru-sys` | Mentoring filosofico, saggezza della Sorgente |

### FACTORY -- Generazione (3)

| Skill | Ruolo |
|-------|-------|
| `forgia-sys` | Metapromptore generativo per entita permanenti |
| `autogen-sys` | Fabbrica di agenti effimeri con ciclo di vita |
| `genesis-sys` | Generatore di semi genomici (trigger YAML minimali) |

### FORM -- Manifestazione (3)

| Skill | Ruolo |
|-------|-------|
| `architect-sys` | Analisi strutturale e coerenza sistemica |
| `builder-sys` | Architetto UI full-stack (design + build + polish) |
| `scribe-sys` | Generatore di system prompt (protocollo OCC) |

### BRIDGE -- Mondo Fisico (1)

| Skill | Ruolo |
|-------|-------|
| `kinetic-sys` | Ponte Bit-to-Joule, interfaccia mondo fisico |

---

## Il Ciclo Operativo

Ogni interazione segue il ciclo operativo D-ND (Kernel, Sezione 9):

```
Perturbazione  -->  Osservazione  -->  Relazione  -->  Emergenza  -->  Integrazione  -->  Campo Evoluto
   (input)         (espansione)      (dipoli)      (risultante)   (autopoiesi)       (nuovo zero)
```

1. **Perturbazione** -- L'input entra nel Campo di Potenziale come un'onda
2. **Osservazione** -- Il campo si espande, cercando connessioni distanti (fase Non-Duale)
3. **Relazione** -- Si formano i dipoli, assonanze e dissonanze vengono identificate
4. **Emergenza** -- La Risultante cristallizza lungo la Lagrangiana (fase Duale)
5. **Integrazione** -- I Key Learning Insight vengono assorbiti nel campo
6. **Campo Evoluto** -- Il nuovo piano parte da uno zero non banale

---

## Costruire i file .skill

Ogni file `.skill` e un archivio zip contenente una cartella con un `SKILL.md` all'interno:

```
nome-skill.skill (zip)
  └── nome-skill/
       └── SKILL.md
```

Per costruire i file `.skill` dai sorgenti markdown, puoi usare un semplice script di packaging:

```bash
#!/bin/bash
# pack.sh — Pacchettizza i file SKILL.md in archivi .skill
for dir in skills/*/; do
    name=$(basename "$dir")
    if [ -f "$dir/SKILL.md" ]; then
        (cd skills && zip -r "../${name}.skill" "${name}/SKILL.md")
    fi
done
```

---

## Due Versioni

Tutti i documenti principali sono disponibili in entrambe le lingue:

| Documento | Inglese | Italiano |
|-----------|---------|----------|
| Kernel | [`KERNEL_MM_v1.md`](KERNEL_MM_v1.md) | [`KERNEL_MM_v1_IT.md`](KERNEL_MM_v1_IT.md) |
| README | [`README.md`](README.md) | [`README_IT.md`](README_IT.md) |

I file skill stessi usano un vocabolario misto radicato nel framework D-ND (termini latini, italiani e inglesi fanno tutti parte del linguaggio formale).

---

## Licenza

Vedi [LICENSE](LICENSE).

---

## Il Framework D-ND

D-ND (Dipolare Non-Duale) e un framework matematico-filosofico dove:

- Lo **zero** genera i due infiniti contrapposti (il Proto-Assioma)
- Ogni concetto esiste come **dipolo** -- la relazione precede i poli
- L'**assonanza** e coerenza convergente; la **dissonanza** diverge automaticamente
- La **Risultante** e il punto fisso della dinamica propria del sistema
- La **Lagrangiana** seleziona il percorso di minima azione attraverso il campo
- Il **Seme Invariante** protegge l'identita dalla deriva dell'auto-ottimizzazione
- L'**evoluzione e obbligatoria** -- la stasi e fallimento operativo

Per il trattamento formale completo, vedi il documento Kernel.

---

*Il Kernel scompare nell'autologica di R che appare nel continuum.*
