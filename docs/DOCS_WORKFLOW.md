# Werken met ChatGPT en Repomix

## 1. Doel van deze werkwijze

Binnen **Samenspraak** worden taalhulpmiddelen gebruikt om te helpen bij het schrijven van documentatie, prompts en toelichtingen.  
Het doel is niet om teksten automatisch te laten produceren, maar om samen met het hulpmiddel aandachtiger te schrijven.

Om te zorgen dat ook automatisch gegenereerde tekst dezelfde toon en waarden behoudt als de rest van het project,  
worden altijd twee documenten als basis gebruikt:

1. [`MANIFESTO.md`](../MANIFESTO.md) – de maatschappelijke en morele grondslag.  
2. [`LLM_PROMPT_STYLE_AND_LANGUAGE_GUIDE.md`](../LLM_PROMPT_STYLE_AND_LANGUAGE_GUIDE.md) – de richtlijnen voor taal en toon.

Wanneer deze bestanden aanwezig zijn, kan het hulpmiddel schrijven in de geest van Samenspraak: rustig, open en reflectief.

---

## 2. Werken met Repomix

**Repomix** kan alle markdownbestanden in de repository combineren tot één samenhangend tekstbestand.  
Dat bestand vormt de context die ChatGPT of een ander hulpmiddel gebruikt bij het schrijven.  
De waarden en toon uit het Manifest en de Language and Tone Guide worden daardoor automatisch meegenomen.

### 2.1 Via de command-line

Gebruik de CLI-versie als je werkt vanuit een lokale omgeving.

~~~bash
repomix --include "*.md" --output repomix-output-tree-main.md
~~~

Het bestand `repomix-output-tree-main.md` kan worden toegevoegd aan een ChatGPT project of conversatie
voor gebruik bij documentatie, promptontwikkeling of analyse.

### 2.2 Via de Repomix-UI

Voor wie liever grafisch werkt, is er ook de **Repomix-UI**.  
Deze tool maakt het mogelijk om zonder terminal alle bestanden te bundelen.

1. Open [https://repomix.app](https://repomix.app) of start de lokale UI.  
2. Voer `Samenspraak/samenspraak/` in als GitHub repository.
3. Kies de instellingen:  
   - **Include:** `*.md`  
   - **Output name:** `repomix-output-tree-main.md`  
4. Klik op **Generate Mix**.  

De UI produceert hetzelfde resultaat als de CLI-versie en helpt bij gezamenlijk schrijven of review.

---

## 3. Richtlijnen voor gebruik

- Gebruik taalhulpmiddelen als ondersteuning, niet als vervanging van reflectie.  
- Laat het hulpmiddel werken binnen de kaders van het Manifest en de Language and Tone Guide.  
- Voeg geen aparte tooninstructies toe in prompts; de gids bepaalt al de gewenste houding.  
- Controleer of de gegenereerde tekst past bij de waarden van Samenspraak: rustig, transparant en niet overtuigend.  
- Noteer bij twijfel een observatie in een issue met het label `ethics-check`.

---

## 4. Voor bijdragers aan documentatie

Wie werkt aan documentatie of aan tests van prompts:

- Lees de samenvatting in [`LLM_PROMPT_STYLE_AND_LANGUAGE_GUIDE.md`](../LLM_PROMPT_STYLE_AND_LANGUAGE_GUIDE.md).  
- Gebruik ChatGPT of een ander hulpmiddel met deze bestanden in de context,  
  zodat toon en stijl consistent blijven.  
- Plaats vragen of voorstellen over stijl in een *Ethics & Language Review*-issue.  
- Zie documentatie als een verlengde van het gesprek dat Samenspraak wil ondersteunen: open, zorgvuldig en menselijk.

---

## 5. Samenvatting

| Onderwerp | Richtlijn |
|------------|-----------|
| **Context** | Gebruik `MANIFESTO.md` en `LLM_PROMPT_STYLE_AND_LANGUAGE_GUIDE.md` als vaste basis. |
| **Doel** | Automatisch gegenereerde tekst afstemmen op de waarden van Samenspraak. |
| **Werkwijze** | Gebruik Repomix-CLI of Repomix-UI om één contextbestand te maken. |
| **Toon** | Rustig, reflectief, neutraal, zonder oordeel. |
| **Controle** | Gebruik het issue *Ethics & Language Review* bij twijfel. |

---

### Slot

Deze werkwijze helpt om menselijk en automatisch schrijven met elkaar te verbinden.  
Niet om snelheid te vergroten, maar om aandacht te bewaren.  
Zo blijft Samenspraak herkenbaar in elke vorm van taal,  
ongeacht wie of wat de tekst heeft geschreven.
